# Azure Resource Monitor Agent

## Overview

The Azure Resource Monitor Agent is an intelligent monitoring and optimization agent designed to help organizations track, analyze, and optimize their Microsoft Azure resources. This agent automatically monitors resource health, performance, and utilization while providing actionable insights for cost optimization and performance improvement.

## What This Agent Does

### Primary Functions
1. **Resource Health Monitoring**
   - Monitors Azure resources across subscriptions and resource groups
   - Tracks resource health status and availability metrics
   - Alerts on resource failures or degraded performance

2. **Performance & Utilization Analysis**
   - Examines Azure Monitor metrics for CPU, memory, and storage utilization
   - Analyzes network performance and disk I/O metrics
   - Identifies performance bottlenecks and optimization opportunities

3. **Cost Optimization**
   - Identifies underutilized Virtual Machines, Storage Accounts, and databases
   - Calculates potential savings from rightsizing or deallocating resources
   - Provides specific recommendations for each resource optimization

4. **Automated Reporting & Alerts**
   - Generates comprehensive resource monitoring reports
   - Sends automated alerts via Teams or Slack
   - Provides actionable insights with prioritized remediation steps

### Key Capabilities
- **Azure Monitor Integration**: Leverages Azure Monitor for comprehensive metrics
- **Cost Management Integration**: Analyzes spending patterns and optimization opportunities
- **Automated Workflows**: Runs scheduled monitoring via the `azure-resource-health-check` workflow
- **Multi-Service Coverage**: Covers VMs, App Services, SQL Databases, Storage, and more
- **Health Scoring**: Provides health scores and performance ratings for resources
- **Compliance Monitoring**: Tracks resource compliance with organizational policies

## Directory Structure

- **`reports/`** - Pre-configured report templates for various Azure services and monitoring
- **`knowledge/`** - Configuration data including subscription settings and operational knowledge
- **`datasources/`** - Connection configurations for Azure Monitor, Cost Management, and notifications
- **`workflows/`** - Automated workflow definitions for scheduled resource monitoring

## Main Workflow

The agent's primary workflow (`azure-resource-health-check`) performs the following steps:

1. Query Azure Monitor for resource health and performance metrics
2. Analyze resource utilization across all subscriptions
3. Calculate performance scores and identify optimization opportunities
4. Check compliance with organizational policies and best practices
5. Generate health scores and performance recommendations
6. Compile findings into a comprehensive monitoring report
7. Send alerts for critical issues and optimization opportunities
8. Track resource trends and historical performance

This workflow runs automatically to ensure continuous monitoring and optimization of Azure resources.