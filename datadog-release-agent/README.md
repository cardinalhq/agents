# Datadog Release Agent

## Overview

The Datadog Release Agent is an intelligent release monitoring agent that helps teams validate deployments by comparing logs and metrics before and after a release. This agent automatically detects anomalies, identifies regressions, and provides clear pass/fail assessments to determine release health.

## What This Agent Does

### Primary Functions
1. **Log-Based Release Validation**
   - Compares log patterns N hours before and after a release
   - Detects increases in error or warning log levels post-release
   - Identifies log patterns that stopped occurring after deployment
   - Surfaces new error patterns that emerged post-release

2. **Metrics-Based Release Validation**
   - Analyzes system metrics (CPU, memory, network, disk) before and after release
   - Monitors request rates for sustained drops post-release
   - Tracks error metrics for sustained increases
   - Evaluates latency metrics for performance regressions
   - Compares custom business metrics and SLIs across release boundaries

3. **Anomaly Detection**
   - Uses configurable thresholds (default 10% deviation for logs)
   - Applies P50/P99 comparisons for metrics (1.5x movement threshold)
   - Groups metrics by critical tags for detailed analysis
   - Identifies both increases and decreases in key indicators

4. **Release Health Assessment**
   - Provides clear thumbs up/thumbs down verdicts
   - Generates detailed reports for failed assessments
   - Includes example log lines and specific metric comparisons
   - Explains why detected changes might matter for the release

### Key Capabilities
- **Datadog Integration**: Queries logs and metrics via Datadog APIs
- **Flexible Time Windows**: Configurable pre/post release comparison periods
- **Service-Level Analysis**: Filter by service name and infrastructure tags
- **Automated Workflows**: Runs scheduled analysis via the `check-release` workflow
- **Multi-Metric Analysis**: Covers HTTP latency, request counts, error rates, and custom business metrics

## Directory Structure

- **`reports/`** - Pre-configured report templates for log searches and metric queries
- **`knowledge/`** - Operational knowledge and configuration data
- **`datasources/`** - Connection configuration for Datadog
- **`workflows/`** - Automated workflow definitions for release validation

## Main Workflow

### Check Release Workflow (`check-release`)
Comprehensive release validation that analyzes both logs and metrics:

**Log Analysis:**
1. Query logs for the service during pre-release and post-release windows
2. Count logs by level/status and check for threshold deviations (>10%) in WARN+ levels
3. Compare pattern counts before and after release
4. Identify patterns that disappeared or newly emerged post-release

**Metrics Analysis:**
5. Query system metrics (CPU, memory, network, disk) for the service
6. Analyze request metrics for sustained drops
7. Check error metrics for sustained increases
8. Evaluate latency metrics for performance regressions (P50/P99 > 1.5x movement)
9. Compare custom business metrics grouped by critical tags

**Output:**
- Clear thumbs up/thumbs down verdict for the release
- Detailed findings for any issues detected (log patterns, metric regressions)

This workflow runs on a daily schedule to support continuous release monitoring.

## Available Reports

### Log Reports
- `service-logs-search` - Search logs by service and text pattern
- `service-logs-retrieval` - Retrieve logs for a service

### Request Metrics
- `service-request-count` - Total request count for a service
- `service-request-count-by-dimension` - Request count grouped by a dimension (e.g., resource name, endpoint)
- `server-request-count` - Total request count for a server (from trace service graph)
- `client-requests-by-server` - Client requests to a server grouped by client

### Error Metrics
- `service-error-count` - Total error count for a service
- `service-error-count-by-dimension` - Error count grouped by a dimension (e.g., status code)
- `service-error-rate` - Error rate percentage for a service

### Latency Metrics
- `service-latency-percentiles` - P50 and P99 latency for a service
- `http-request-duration-average` - Average HTTP request duration
- `average-http-request-duration` - Average HTTP server request duration
- `http-duration-by-status` - HTTP duration grouped by response status code