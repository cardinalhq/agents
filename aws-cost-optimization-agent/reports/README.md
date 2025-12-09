# Reports Directory

This directory contains pre-configured report templates and SQL queries that the AWS Cost Optimization Agent uses to analyze costs, utilization, and performance across various Amazon Web Services.

## Purpose

The reports directory serves as the repository for:
- **Cost Analysis Templates**: Pre-built queries for identifying spending patterns and cost optimization opportunities
- **Utilization Reports**: Templates for monitoring resource usage across EC2, RDS, Lambda, and other AWS services
- **Performance Analytics**: Reports that help identify underutilized resources and optimization potential
- **Cost Intelligence**: Comprehensive analysis of AWS billing data for cost management

## Report Categories

### Cost Analysis Reports
- Billing breakdown by account, service, and resource
- Daily, weekly, and monthly cost trend analysis
- Top cost contributors identification
- Cost projection and forecasting

### Resource Utilization Reports
- CPU, memory, and network utilization across services
- EC2 instance performance analysis
- RDS database utilization metrics
- Lambda function usage and cost efficiency

### Service-Specific Reports
- **EC2 Instances**: Instance lists, CPU utilization, performance metrics, rightsizing recommendations
- **RDS Databases**: Database performance, resource usage, optimization opportunities
- **Lambda Functions**: Execution patterns, memory usage, cost optimization
- **S3 Storage**: Storage usage analysis, lifecycle optimization opportunities
- **EBS Volumes**: Utilization patterns, resizing recommendations

## How Reports Work

1. **Template Based**: Each report is a JSON configuration containing SQL queries and metadata
2. **Automated Execution**: Reports are automatically executed by the agent's workflows
3. **Data Sources**: Reports query AWS Cost and Billing Reports and CloudWatch APIs
4. **Parameterized**: Reports include configurable thresholds, time ranges, and filters
5. **Actionable Output**: Results provide specific recommendations for cost optimization

## Integration with Workflows

These report templates are utilized by the agent's main workflow to:
- Identify underutilized AWS resources
- Calculate potential cost savings
- Generate optimization recommendations
- Provide automated alerts and insights

This directory forms the analytical foundation of the AWS Cost Optimization Agent's cost management capabilities.