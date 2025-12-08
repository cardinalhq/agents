# Infrastructure Drift Detector Agent

## Overview

The Infrastructure Drift Detector Agent is an intelligent infrastructure monitoring and compliance agent designed to help organizations detect configuration drift, unauthorized changes, and ensure infrastructure as code compliance. This agent automatically compares actual infrastructure state against desired configurations and provides actionable insights to maintain infrastructure consistency.

## What This Agent Does

### Primary Functions
1. **Configuration Drift Detection**
   - Monitors infrastructure resources for configuration changes
   - Compares actual state against Terraform/CloudFormation templates
   - Identifies unauthorized or untracked modifications

2. **Infrastructure as Code Compliance**
   - Validates infrastructure matches IaC definitions
   - Tracks resources created outside of automation pipelines
   - Monitors template version compliance and updates

3. **Change Impact Analysis**
   - Analyzes the impact of configuration changes on security and compliance
   - Identifies potential risks from infrastructure modifications
   - Tracks resource dependency relationships

4. **Automated Reporting & Alerts**
   - Generates comprehensive drift detection reports
   - Sends automated alerts for critical infrastructure changes via Slack
   - Provides actionable insights with prioritized remediation steps

### Key Capabilities
- **Multi-Cloud Support**: Supports AWS, Azure, GCP infrastructure monitoring
- **IaC Integration**: Integrates with Terraform, CloudFormation, ARM templates
- **Automated Workflows**: Runs scheduled drift detection via the `infrastructure-drift-scan` workflow
- **Change Tracking**: Maintains historical records of infrastructure changes
- **Risk Assessment**: Provides risk scores for configuration drift
- **Remediation Guidance**: Suggests specific steps to resolve drift

## Directory Structure

- **`reports/`** - Pre-configured report templates for drift detection and infrastructure analysis
- **`knowledge/`** - Configuration data including IaC template locations and baseline configurations
- **`datasources/`** - Connection configurations for cloud providers, IaC tools, and notifications
- **`workflows/`** - Automated workflow definitions for scheduled drift detection

## Main Workflow

The agent's primary workflow (`infrastructure-drift-scan`) performs the following steps:

1. Query current infrastructure state from cloud providers
2. Fetch Infrastructure as Code templates and configurations
3. Compare actual state against desired IaC definitions
4. Identify configuration drift and unauthorized changes
5. Calculate risk scores and impact assessments for detected drift
6. Generate remediation recommendations for each drift item
7. Compile findings into a comprehensive drift detection report
8. Send alerts for critical infrastructure changes and compliance violations
9. Track drift trends and infrastructure evolution over time

This workflow runs automatically to ensure continuous monitoring of infrastructure state and compliance.