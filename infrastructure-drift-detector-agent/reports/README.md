# Reports Directory

This directory contains pre-configured report templates and SQL queries that the Infrastructure Drift Detector Agent uses to analyze infrastructure configuration drift, compliance violations, and security posture across various cloud platforms.

## Purpose

The reports directory serves as the repository for:
- **Configuration Drift Templates**: Pre-built queries for identifying infrastructure configuration changes and deviations
- **Compliance Reports**: Templates for monitoring adherence to security policies and compliance standards
- **Security Posture Analytics**: Reports that help identify security vulnerabilities and misconfigurations
- **Infrastructure Intelligence**: Comprehensive analysis of infrastructure state for governance and compliance

## Report Categories

### Configuration Drift Reports
- Infrastructure configuration baseline comparison
- Unauthorized configuration changes detection
- Resource policy violations and deviations
- Configuration compliance scoring and trending

### Security and Compliance Reports
- Security group and firewall rule analysis
- IAM policy drift and privilege escalation detection
- Encryption configuration compliance
- Network security posture assessment

### Service-Specific Reports
- **AWS**: CloudFormation stack drift, Security Group changes, IAM policy modifications
- **Azure**: Resource Manager template drift, Network Security Group changes, RBAC modifications
- **GCP**: Deployment Manager drift, Firewall rule changes, IAM policy updates
- **Kubernetes**: Pod security policy violations, RBAC drift, network policy changes

## How Reports Work

1. **Template Based**: Each report is a JSON configuration containing queries and metadata for drift detection
2. **Automated Execution**: Reports are automatically executed by the agent's workflows
3. **Data Sources**: Reports query cloud APIs, configuration management tools, and infrastructure state
4. **Parameterized**: Reports include configurable baselines, policies, and compliance frameworks
5. **Actionable Output**: Results provide specific remediation steps for identified drift

## Integration with Workflows

These report templates are utilized by the agent's main workflow to:
- Detect infrastructure configuration drift and unauthorized changes
- Identify compliance violations and security misconfigurations
- Generate remediation recommendations and alerts
- Provide continuous infrastructure governance insights

This directory forms the analytical foundation of the Infrastructure Drift Detector Agent's governance and compliance capabilities.