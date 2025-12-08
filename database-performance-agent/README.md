# Database Performance Agent

## Overview

The Database Performance Agent is an intelligent database monitoring and optimization agent designed to help organizations monitor, analyze, and optimize their database performance across multiple database platforms. This agent automatically identifies performance bottlenecks, slow queries, and provides actionable recommendations to improve database efficiency.

## What This Agent Does

### Primary Functions
1. **Performance Monitoring**
   - Monitors database performance metrics including CPU, memory, and I/O usage
   - Tracks query execution times and identifies slow-running queries
   - Analyzes connection pool utilization and wait statistics

2. **Query Optimization Analysis**
   - Identifies inefficient queries and missing indexes
   - Analyzes query execution plans and resource consumption
   - Provides recommendations for query optimization and indexing strategies

3. **Resource Utilization Assessment**
   - Monitors database server resource utilization patterns
   - Identifies underutilized or over-provisioned database instances
   - Calculates optimal resource allocation recommendations

4. **Automated Reporting & Alerts**
   - Generates comprehensive database performance reports
   - Sends automated alerts for performance degradation via Slack
   - Provides actionable insights with prioritized optimization tasks

### Key Capabilities
- **Multi-Database Support**: Supports PostgreSQL, MySQL, SQL Server, Oracle, and more
- **Performance Metrics Integration**: Leverages database-specific monitoring tools
- **Automated Workflows**: Runs scheduled analysis via the `database-performance-analysis` workflow
- **Query Analysis**: Deep dive into slow queries and execution plans
- **Index Recommendations**: Suggests optimal indexing strategies
- **Capacity Planning**: Provides resource scaling recommendations

## Directory Structure

- **`reports/`** - Pre-configured report templates for database performance analysis
- **`knowledge/`** - Configuration data including database settings and optimization knowledge
- **`datasources/`** - Connection configurations for various databases and monitoring systems
- **`workflows/`** - Automated workflow definitions for scheduled performance analysis

## Main Workflow

The agent's primary workflow (`database-performance-analysis`) performs the following steps:

1. Query database performance metrics and system statistics
2. Analyze slow query logs and execution statistics
3. Examine index usage and table scan patterns
4. Identify resource bottlenecks and optimization opportunities
5. Generate performance tuning recommendations
6. Compile findings into a comprehensive performance report
7. Send alerts for critical performance issues
8. Track performance trends and historical patterns

This workflow runs automatically to ensure continuous monitoring and optimization of database performance.