# Reports Directory

This directory contains pre-configured report templates and SQL queries that the Database Performance Agent uses to analyze database performance, query optimization, and resource utilization across various database systems.

## Purpose

The reports directory serves as the repository for:
- **Performance Analysis Templates**: Pre-built queries for identifying performance bottlenecks and optimization opportunities
- **Query Analytics**: Templates for analyzing slow queries, execution plans, and optimization recommendations
- **Resource Utilization Reports**: Reports monitoring CPU, memory, I/O, and storage across database instances
- **Database Health Intelligence**: Comprehensive analysis of database metrics for performance tuning

## Report Categories

### Performance Analysis Reports
- Query performance analysis and slow query identification
- Index usage and optimization recommendations
- Lock and deadlock analysis
- Connection pool and concurrency monitoring

### Resource Utilization Reports
- CPU, memory, and disk I/O utilization patterns
- Storage growth analysis and capacity planning
- Database connection and session monitoring
- Buffer pool and cache effectiveness analysis

### Service-Specific Reports
- **PostgreSQL**: Query performance, index analysis, connection monitoring, vacuum statistics
- **MySQL**: Slow query analysis, InnoDB metrics, replication monitoring
- **SQL Server**: Query store analysis, wait statistics, index fragmentation
- **MongoDB**: Collection statistics, query profiling, replica set monitoring
- **Oracle**: AWR reports, SQL tuning advisor recommendations, tablespace analysis

## How Reports Work

1. **Template Based**: Each report is a JSON configuration containing SQL/NoSQL queries and metadata
2. **Automated Execution**: Reports are automatically executed by the agent's workflows
3. **Data Sources**: Reports query database performance views, system catalogs, and monitoring APIs
4. **Parameterized**: Reports include configurable thresholds, time ranges, and filters
5. **Actionable Output**: Results provide specific recommendations for performance optimization

## Integration with Workflows

These report templates are utilized by the agent's main workflow to:
- Identify database performance bottlenecks and optimization opportunities
- Generate query optimization recommendations
- Monitor database health and resource utilization
- Provide automated performance tuning insights

This directory forms the analytical foundation of the Database Performance Agent's optimization capabilities.