# Reports Directory

This directory contains pre-configured report templates and SQL queries that the Azure Resource Monitor Agent uses to analyze resource health, performance, and utilization across various Microsoft Azure services.

## Purpose

The reports directory serves as the repository for:
- **Resource Health Templates**: Pre-built queries for monitoring resource availability and health status
- **Performance Reports**: Templates for monitoring resource performance across Azure services
- **Utilization Analytics**: Reports that help identify underutilized or overutilized resources
- **Operational Intelligence**: Comprehensive analysis of Azure resource data for optimization

## Report Categories

### Resource Health Reports
- Resource availability and uptime analysis
- Health status monitoring across subscriptions and resource groups
- Service degradation identification
- SLA compliance tracking

### Performance Analytics Reports
- CPU, memory, and disk utilization across services
- Virtual Machine performance analysis
- Azure SQL Database performance metrics
- Application performance insights

### Service-Specific Reports
- **Virtual Machines**: Instance health, performance metrics, resource utilization
- **Azure SQL Databases**: Database performance, resource usage, query optimization
- **App Services**: Application performance, scaling patterns, resource efficiency
- **Storage Accounts**: Storage utilization, performance metrics, access patterns
- **Azure Kubernetes Service**: Cluster health, node utilization, pod performance

## How Reports Work

1. **Template Based**: Each report is a JSON configuration containing KQL queries and metadata
2. **Automated Execution**: Reports are automatically executed by the agent's workflows
3. **Data Sources**: Reports query Azure Monitor, Log Analytics, and Resource Health APIs
4. **Parameterized**: Reports include configurable thresholds, time ranges, and filters
5. **Actionable Output**: Results provide specific recommendations for resource optimization

## Integration with Workflows

These report templates are utilized by the agent's main workflow to:
- Monitor Azure resource health and availability
- Identify performance bottlenecks and optimization opportunities
- Generate proactive alerts and recommendations
- Provide comprehensive resource monitoring insights

This directory forms the analytical foundation of the Azure Resource Monitor Agent's monitoring and optimization capabilities.