# AWS Cost Optimization Agent

## Overview

The AWS Cost Optimization Agent is an intelligent cost analysis and optimization agent designed to help organizations monitor, analyze, and optimize their Amazon Web Services spending. This agent automatically identifies underutilized resources, tracks cost trends, and provides actionable recommendations to reduce cloud expenses.

## What This Agent Does

### Primary Functions
1. **Cost Analysis & Monitoring**
   - Analyzes AWS Cost Explorer data to identify top cost contributors by service and account
   - Tracks daily, weekly, and monthly spending patterns
   - Monitors cost trends across different AWS services and regions

2. **Resource Utilization Assessment**
   - Examines CloudWatch metrics to determine utilization rates
   - Calculates CPU, memory, and network utilization for EC2, RDS, and other services
   - Identifies resources with utilization below optimal thresholds

3. **Underutilization Detection**
   - Automatically detects underutilized EC2 instances, RDS databases, and other AWS resources
   - Calculates potential cost savings from rightsizing or terminating resources
   - Provides specific recommendations for each underutilized resource

4. **Automated Reporting & Alerts**
   - Generates comprehensive cost optimization reports
   - Sends automated alerts and summaries via Slack
   - Provides actionable insights with prioritized action items

### Key Capabilities
- **Cost Explorer Integration**: Queries billing data for detailed cost analysis
- **CloudWatch Integration**: Leverages CloudWatch for resource utilization metrics
- **Automated Workflows**: Runs scheduled analysis via the `aws-cost-optimization-report` workflow
- **Multi-Service Analysis**: Covers EC2, RDS, ELB, S3, Lambda, and more
- **Cost Projections**: Provides daily cost breakdowns and monthly projections
- **Remediation Guidance**: Offers specific recommendations for cost optimization

## Directory Structure

- **`reports/`** - Pre-configured report templates for various AWS services and cost analysis
- **`knowledge/`** - Configuration data including primary region settings and operational knowledge
- **`datasources/`** - Connection configurations for Cost Explorer, CloudWatch, and notification systems
- **`workflows/`** - Automated workflow definitions for scheduled cost analysis

## Main Workflow

The agent's primary workflow (`aws-cost-optimization-report`) performs the following steps:

1. Query Cost Explorer data to identify top cost contributors by service
2. Examine CloudWatch metrics for utilization rates
3. Calculate utilization percentages using CPU, memory, and network metrics
4. Identify resources with below-threshold utilization as underutilized
5. Calculate daily costs, projected monthly costs, and potential savings
6. Generate remediation recommendations for each underutilized resource
7. Compile findings into an actionable cost optimization report
8. Send summary notifications via Slack

This workflow runs automatically on a daily schedule to ensure continuous cost monitoring and optimization.