# AIDevOps-Prompt-Library

Inital Work of Vamshi Meda - https://www.linkedin.com/in/vamshi-meda/
Prompt Library for AI infusion in DevOps
# AI DevOps Prompt Library

## 🎯 Accuracy & Reliability Guide

### Prompt Effectiveness Factors
The accuracy of AI-generated DevOps solutions depends on four critical factors:

**📊 Complexity Level**
- 🟢 **Simple (80-90% accuracy)**: Basic configurations, standard templates, common patterns
- 🟡 **Moderate (60-80% accuracy)**: Multi-service integrations, environment-specific configs
- 🔴 **Complex (40-60% accuracy)**: Custom architectures, advanced security, compliance requirements

**🔧 Technology Maturity**
- 🟢 **Well-Established (80-90% accuracy)**: Docker, Kubernetes, Jenkins, Terraform, AWS/Azure basics
- 🟡 **Moderately Established (60-80% accuracy)**: GitOps tools, service mesh, newer cloud services
- 🔴 **Cutting-Edge (40-60% accuracy)**: Latest releases, experimental features, niche tools

**🏗️ Context Specificity**
- 🟢 **Generic (70-85% accuracy)**: Standard use cases, common patterns
- 🟡 **Environment-Specific (50-75% accuracy)**: Custom requirements, specific constraints
- 🔴 **Highly Specific (30-60% accuracy)**: Unique architectures, legacy integrations, strict compliance

**📝 Prompt Quality Impact**
- 🟢 **Rich Context**: Include environment details, constraints, specific requirements
- 🟡 **Moderate Context**: Basic requirements and target platform
- 🔴 **Minimal Context**: Vague requests without specifics

### ⚠️ Critical Validation Requirements
- **Always test in non-production environments**
- **Security review mandatory for all infrastructure code**
- **Performance testing required for production deployments**
- **Compliance validation for regulated environments**

## Infrastructure as Code (IaC)

### Terraform Configuration
**🟢 Complexity: Simple-Moderate | 🟢 Technology: Well-Established**
```
Create a Terraform configuration for deploying a [application type] on [cloud provider] with the following requirements:

CONTEXT (Critical for accuracy):
- Environment: [dev/staging/prod]
- Team size: [number of developers]
- Existing infrastructure: [describe current setup]
- Compliance requirements: [HIPAA/SOC2/PCI/etc.]
- Budget constraints: [specify limits]

TECHNICAL REQUIREMENTS:
- Compute resources: [instance types, sizes, scaling requirements]
- Network configuration: [VPC/subnets, public/private, CIDR blocks]
- Security groups/firewall rules: [specific ports, source/destination IPs]
- Storage requirements: [types, sizes, backup/retention policies]
- Monitoring and logging: [CloudWatch/Azure Monitor/GCP Operations]

OPERATIONAL CONTEXT:
- State management preference: [remote backend type, team access patterns]
- Resource naming convention: [existing patterns]
- Tagging strategy: [cost center, environment, owner tags]
- Change management process: [approval workflows, review requirements]

⚠️ VALIDATION REQUIRED: Test in non-prod, review security groups, validate state backend permissions
```

### Kubernetes Manifests
**🟢 Complexity: Simple-Moderate | 🟢 Technology: Well-Established**
```
Generate Kubernetes YAML manifests for a [application type] with:

CONTEXT (Essential for accuracy):
- Kubernetes version: [1.27, 1.28, 1.29, etc.]
- Cluster environment: [managed service like EKS/GKE/AKS or self-managed]
- Namespace strategy: [single/multi-tenant, isolation requirements]
- Existing cluster setup: [ingress controller, storage classes, monitoring]
- Security requirements: [Pod Security Standards, network policies]

APPLICATION REQUIREMENTS:
- Deployment: [number] replicas, rolling update strategy
- Service configuration: [ClusterIP/NodePort/LoadBalancer] for [port/protocol]
- ConfigMap for: [specific configuration parameters and values]
- Secret for: [database credentials, API keys, certificates]
- Ingress with: [domain/path] routing, [TLS/SSL requirements]
- Resource limits: CPU [amount], Memory [amount], storage [size]

OPERATIONAL CONTEXT:
- High availability requirements: [pod disruption budgets, anti-affinity]
- Scaling requirements: [HPA metrics, min/max replicas]
- Monitoring integration: [Prometheus annotations, health check endpoints]
- Backup/disaster recovery: [persistent volume backup strategy]

⚠️ VALIDATION REQUIRED: Test resource limits, validate RBAC, security context review, ingress testing
```

### Docker Optimization
**🟡 Complexity: Moderate | 🟢 Technology: Well-Established**
```
Analyze and optimize this Dockerfile for [application type]:

CURRENT DOCKERFILE:
[PASTE COMPLETE DOCKERFILE HERE]

CONTEXT (Critical for optimization):
- Application details: [language/framework, dependencies, build process]
- Deployment target: [cloud provider, container orchestration platform]
- Performance requirements: [startup time, memory usage, image size constraints]
- Security requirements: [scanning tools, base image policies, user permissions]
- Build environment: [CI/CD platform, build frequency, caching infrastructure]

OPTIMIZATION GOALS:
- Multi-stage builds: [specific build vs runtime requirements]
- Image size target: [current size vs target size]
- Security hardening: [vulnerability scan results, compliance requirements]
- Layer caching: [build frequency, shared dependencies with other images]
- Base image constraints: [approved base images, update policies]

OPERATIONAL CONTEXT:
- Registry limitations: [private registry, bandwidth constraints]
- Deployment patterns: [blue-green, rolling updates, frequency]
- Development workflow: [local development, debugging requirements]

⚠️ VALIDATION REQUIRED: Security scan optimized image, test multi-stage build, validate runtime behavior
```

## CI/CD Pipeline Configuration

## CI/CD Pipeline Configuration

### GitHub Actions Workflow
**🟡 Complexity: Moderate | 🟢 Technology: Well-Established**
```
Create a GitHub Actions workflow for [project type] that:

CONTEXT (Essential for workflow design):
- Repository structure: [mono-repo/multi-repo, language/framework]
- Team size and workflow: [number of developers, branch strategy, review process]
- Deployment targets: [environments, infrastructure, rollback requirements]
- Security posture: [SAST/DAST tools, compliance scanning, secret management]
- Performance requirements: [build time constraints, parallel execution needs]

WORKFLOW REQUIREMENTS:
- Triggers: [push/PR events, manual dispatch, scheduled runs]
- Test environments: [OS versions, language versions, dependency matrix]
- Build process: [compilation, packaging, artifact generation]
- Container registry: [Docker Hub/ECR/GCR, image tagging strategy]
- Deployment targets: [staging/production environments, approval gates]
- Security scanning: [code analysis tools, vulnerability scanning, license checking]
- Notifications: [Slack/Teams/email, success/failure conditions]

OPERATIONAL CONTEXT:
- Secrets management: [GitHub secrets, external vaults, rotation policies]
- Environment protection: [required reviewers, wait timers, deployment branches]
- Cost considerations: [runner minutes, large file handling, caching strategy]
- Integration requirements: [external systems, APIs, databases for testing]

⚠️ VALIDATION REQUIRED: Test workflow in fork, validate secrets access, review security permissions
```

### GitHub Advanced Configurations
**🟡 Complexity: Moderate-Complex | 🟢 Technology: Well-Established**
```
Configure GitHub enterprise features for [organization/team]:

CONTEXT (Critical for enterprise setup):
- Organization size: [number of users, teams, repositories]
- Security requirements: [SSO provider, SAML/OIDC, compliance needs]
- Access patterns: [internal/external contributors, contractor access]
- Existing tools: [project management, security scanning, deployment tools]
- Governance requirements: [branch protection, required reviews, audit logging]

CONFIGURATION REQUIREMENTS:
- Repository management: [template repos, auto-archiving, naming conventions]
- Branch protection rules: [required status checks, review requirements, admin bypass]
- Security settings: [dependency alerts, secret scanning, code scanning integration]
- Organization policies: [member permissions, third-party access, IP restrictions]
- Team structure: [nested teams, permission inheritance, external collaborators]
- Compliance features: [audit log retention, data residency, export capabilities]

INTEGRATION CONTEXT:
- SSO integration: [provider details, group mapping, just-in-time provisioning]
- Webhook configurations: [external systems, payload delivery, retry policies]
- App installations: [GitHub Apps, OAuth Apps, security review requirements]
- API usage: [rate limiting, personal access tokens, organization tokens]

⚠️ VALIDATION REQUIRED: Test SSO integration, validate permission inheritance, security team review mandatory
```

### Harness CI/CD Pipeline
**🟡 Complexity: Moderate-Complex | 🟡 Technology: Moderately-Established**
```
Create a Harness pipeline for [application type] with:

CONTEXT (Essential for Harness configuration):
- Harness platform: [FirstGen/NextGen, SaaS/Self-Managed, version]
- Application architecture: [microservices/monolith, container/traditional deployment]
- Infrastructure: [Kubernetes, cloud provider, on-premise, hybrid]
- Team structure: [developers, ops, security, approval workflows]
- Existing integrations: [source control, artifact repos, monitoring tools]

PIPELINE REQUIREMENTS:
- Source integration: [GitHub/GitLab/Bitbucket, webhook triggers, branch strategies]
- Build process: [Docker builds, artifact management, caching strategies]
- Testing stages: [unit, integration, security, performance testing tools]
- Deployment strategies: [blue-green, canary, rolling, custom strategies]
- Environment promotion: [dev->staging->prod, approval gates, rollback procedures]
- Infrastructure provisioning: [Terraform integration, CloudFormation, ARM templates]

HARNESS-SPECIFIC CONTEXT:
- Delegates: [installation locations, connectivity requirements, scaling needs]
- Connectors: [cloud providers, Kubernetes clusters, artifact repositories]
- Secrets management: [Harness secrets, external vaults, rotation policies]
- Governance: [pipeline templates, policy enforcement, compliance scanning]
- Monitoring integration: [Harness CV, APM tools, log aggregation]
- GitOps integration: [Argo CD, flux, manifest management]

OPERATIONAL CONTEXT:
- Approval workflows: [manual approvals, JIRA integration, Slack notifications]
- Failure handling: [retry policies, rollback triggers, notification escalation]
- Performance requirements: [pipeline duration, parallel execution, resource limits]
- Audit and compliance: [deployment tracking, change management, reporting needs]

⚠️ VALIDATION REQUIRED: Test delegate connectivity, validate RBAC, review approval workflows, performance testing required
```

### Harness Feature Flags
**🟡 Complexity: Moderate | 🟡 Technology: Moderately-Established**
```
Configure Harness Feature Flags for [application/service]:

CONTEXT (Critical for feature flag strategy):
- Application details: [tech stack, deployment frequency, user base size]
- Release strategy: [gradual rollouts, A/B testing, emergency killswitches]
- Team workflows: [development process, testing procedures, release coordination]
- Infrastructure: [multi-region, microservices, load balancing setup]
- Monitoring capabilities: [metrics collection, alerting, user behavior tracking]

FEATURE FLAG REQUIREMENTS:
- Flag types: [boolean, string, number, JSON flags for different use cases]
- Targeting rules: [user segments, percentage rollouts, geographic targeting]
- Environment strategy: [dev/staging/prod sync, flag lifecycle management]
- SDK integration: [client-side/server-side SDKs, caching, offline support]
- Evaluation strategies: [real-time updates, polling intervals, webhook notifications]

OPERATIONAL CONTEXT:
- Governance: [flag approval workflows, naming conventions, cleanup policies]
- Monitoring integration: [flag evaluation metrics, performance impact tracking]
- Rollback procedures: [automatic rollback triggers, manual override processes]
- Team collaboration: [flag ownership, change notifications, documentation]
- Security considerations: [flag value encryption, audit logging, access controls]

⚠️ VALIDATION REQUIRED: Test flag evaluation performance, validate targeting accuracy, monitor system resource impact
```

### Harness Chaos Engineering
**🔴 Complexity: Complex | 🟡 Technology: Moderately-Established**
```
Design chaos engineering experiments using Harness Chaos Engineering for [system/service]:

CONTEXT (Critical for safe chaos engineering):
- System architecture: [detailed service dependencies, data flow, failure domains]
- Current reliability: [SLA targets, known failure modes, recent incidents]
- Monitoring coverage: [observability stack, alerting, incident response procedures]
- Team readiness: [chaos engineering experience, on-call procedures, communication plans]
- Business context: [critical business hours, maintenance windows, user impact tolerance]

CHAOS EXPERIMENT DESIGN:
- Hypothesis formation: [specific reliability assumptions to test]
- Blast radius definition: [affected services, user impact boundaries, containment strategies]
- Failure injection types: [network latency, service unavailability, resource exhaustion]
- Success criteria: [system recovery time, user experience metrics, data consistency]
- Safety measures: [circuit breakers, automatic rollback, monitoring thresholds]

HARNESS CHAOS CONTEXT:
- Experiment scheduling: [maintenance windows, automated triggers, manual execution]
- Integration setup: [Kubernetes integration, cloud provider APIs, monitoring webhooks]
- Governance controls: [approval workflows, experiment review, blast radius limits]
- Results analysis: [metrics collection, hypothesis validation, improvement recommendations]
- Automation level: [fully automated, semi-automated, manual intervention points]

⚠️ HIGH VALIDATION REQUIRED: Extensive testing in non-prod, incident response team standby, detailed rollback plans, business stakeholder approval mandatory
```

### Jenkins Pipeline
```
Write a Jenkins pipeline (Groovy) for [application type] with stages for:
- Code checkout
- Unit testing
- Static code analysis
- Docker build and push
- Deploy to [environment]
- Integration testing
- Rollback mechanism
Include parallel execution where appropriate and proper error handling.
```

### Harness GitOps Integration
**🟡 Complexity: Moderate-Complex | 🟡 Technology: Moderately-Established**
```
Configure Harness GitOps for [application/infrastructure]:

CONTEXT (Essential for GitOps setup):
- Git repository structure: [mono-repo/multi-repo, manifest organization, branching strategy]
- Kubernetes environment: [cluster setup, namespace strategy, RBAC configuration]
- Application architecture: [microservices dependencies, configuration management, secrets handling]
- Team workflow: [development process, review procedures, deployment ownership]
- Existing tools: [current CD tools, monitoring systems, security scanners]

GITOPS CONFIGURATION:
- Repository management: [manifest repos, application repos, sync strategies]
- Agent deployment: [Harness GitOps Agent installation, connectivity, permissions]
- Application definitions: [Helm charts, Kustomize, raw manifests, templating strategies]
- Sync policies: [automatic/manual sync, prune policies, self-heal configuration]
- Environment promotion: [dev->staging->prod workflows, approval gates, drift detection]
- Security integration: [policy enforcement, image scanning, admission controllers]

HARNESS GITOPS CONTEXT:
- Cluster management: [multi-cluster setup, cluster credentials, network policies]
- Application health: [health checks, sync status, resource monitoring]
- Rollback capabilities: [automatic rollback triggers, manual intervention, history retention]
- Monitoring integration: [sync metrics, application health, alert configurations]
- Access controls: [RBAC integration, user permissions, audit logging]

⚠️ VALIDATION REQUIRED: Test sync policies, validate cluster connectivity, review security policies, disaster recovery testing
```

### GitHub Enterprise Server Administration
**🔴 Complexity: Complex | 🟢 Technology: Well-Established**
```
Configure GitHub Enterprise Server for [organization]:

CONTEXT (Critical for enterprise deployment):
- Infrastructure requirements: [server specifications, network topology, storage systems]
- Scalability needs: [user count, repository count, traffic patterns, growth projections]
- Integration landscape: [LDAP/AD, SSO providers, monitoring systems, backup solutions]
- Security requirements: [network isolation, certificate management, compliance frameworks]
- Operational procedures: [maintenance windows, backup procedures, disaster recovery]

ENTERPRISE SERVER SETUP:
- Hardware/VM configuration: [CPU, memory, storage, network specifications]
- High availability: [load balancing, database clustering, file system replication]
- Authentication: [LDAP/SAML integration, user provisioning, group synchronization]
- Network configuration: [firewall rules, proxy settings, SSL/TLS termination]
- Storage management: [Git LFS, repository storage, backup strategies]
- Monitoring setup: [collectd integration, log aggregation, performance metrics]

OPERATIONAL CONTEXT:
- Backup and recovery: [scheduled backups, restore procedures, RTO/RPO requirements]
- Upgrade procedures: [maintenance scheduling, rollback plans, testing protocols]
- Security hardening: [OS configuration, service hardening, vulnerability management]
- Performance tuning: [database optimization, caching strategies, resource allocation]
- Compliance features: [audit logging, data retention, geographic restrictions]

⚠️ HIGH VALIDATION REQUIRED: Infrastructure testing, disaster recovery validation, security assessment, performance benchmarking mandatory
```

## Monitoring and Observability

### Prometheus Configuration
```
Create Prometheus configuration for monitoring [application/infrastructure] including:
- Service discovery for [targets]
- Scraping intervals and timeouts
- Recording rules for [metrics]
- Alerting rules for [conditions]
- Integration with [service mesh/exporters]
Provide example queries for common monitoring scenarios.
```

### Grafana Dashboard
```
Design a Grafana dashboard JSON for [service/application] monitoring with:
- Key performance indicators: [list KPIs]
- System metrics: CPU, memory, disk, network
- Application metrics: [specific metrics]
- Alert panels for critical thresholds
- Time range controls and refresh intervals
Include proper panel layouts and visualization types.
```

### Log Analysis
```
Create log parsing and analysis rules for [application/service] logs with:
- Log format: [specify format]
- Key fields to extract: [list fields]
- Error pattern detection
- Performance bottleneck identification
- Security event detection
Provide examples for [ELK Stack/Splunk/other tools].
```

## Security and Compliance

### Security Scanning
**🔴 Complexity: Complex | 🟡 Technology: Moderately-Established**
```
Create a security scanning pipeline for [application type] that includes:

CONTEXT (Critical for security effectiveness):
- Application stack: [languages, frameworks, dependencies, container base images]
- Regulatory requirements: [GDPR, HIPAA, PCI-DSS, SOC2, industry-specific]
- Current security posture: [existing tools, baseline security measures]
- Risk tolerance: [acceptable vulnerability levels, remediation timelines]
- Team capabilities: [security expertise, remediation workflows]

SCANNING REQUIREMENTS:
- SAST tools: [SonarQube, Checkmarx, Veracode - specify preferences/existing tools]
- DAST requirements: [application URLs, authentication methods, scan scope]
- Container scanning: [base image vulnerabilities, runtime analysis, registry integration]
- Dependency scanning: [language-specific tools, license compliance, update policies]
- Infrastructure scanning: [IaC analysis, cloud configuration, network security]
- Compliance reporting: [specific frameworks, audit requirements, reporting formats]

OPERATIONAL CONTEXT:
- CI/CD integration: [pipeline stages, failure thresholds, bypass procedures]
- Remediation workflow: [ticket creation, assignee routing, SLA requirements]
- Exception management: [risk acceptance process, temporary waivers, documentation]
- Reporting requirements: [stakeholders, frequency, dashboard needs]
- Tool integration: [SIEM systems, vulnerability management platforms]

⚠️ HIGH VALIDATION REQUIRED: Test all scanning tools, validate reporting accuracy, review exception handling, security team approval essential
```

### Access Control
```
Design RBAC (Role-Based Access Control) configuration for [platform] with:
- Roles: [list roles and responsibilities]
- Permissions: [specific permissions per role]
- Resource scoping: [namespaces/projects/environments]
- Integration with [identity provider]
- Audit logging requirements
Include principle of least privilege implementation.
```

## Automation Scripts

### Infrastructure Automation
```
Write a [Python/Bash/PowerShell] script to automate [specific task] with:
- Input parameters: [list parameters]
- Error handling and logging
- Idempotent operations
- Configuration validation
- Rollback capabilities
- Integration with [tools/APIs]
Include proper documentation and usage examples.
```

### Deployment Automation
```
Create an automated deployment script for [application] that:
- Validates deployment prerequisites
- Implements blue-green/canary deployment
- Performs health checks and smoke tests
- Handles rollback scenarios
- Updates monitoring and alerting
- Sends deployment notifications
Include environment-specific configurations.
```

## Troubleshooting and Diagnostics

### Log Analysis
**🟡 Complexity: Moderate-Complex | 🟡 Technology: Moderately-Established**
```
Analyze these [application/system] logs and identify issues:

CONTEXT (Essential for accurate analysis):
- System architecture: [microservices/monolith, load balancers, databases, caching layers]
- Normal behavior patterns: [typical traffic volumes, expected response times, regular operations]
- Recent changes: [deployments, configuration changes, infrastructure updates]
- Known issues: [existing bugs, performance bottlenecks, intermittent problems]
- Business context: [peak usage times, critical business processes, SLA requirements]

LOG DETAILS:
[PASTE COMPLETE LOG ENTRIES WITH TIMESTAMPS]

ANALYSIS REQUIREMENTS:
- Error pattern identification: [frequency analysis, correlation with system events]
- Performance bottleneck detection: [slow queries, resource contention, scaling issues]
- Security event analysis: [authentication failures, unusual access patterns, potential breaches]
- Business impact assessment: [affected users, revenue impact, service degradation]
- Root cause hypothesis: [based on timeline, system dependencies, change correlation]

OPERATIONAL CONTEXT:
- Monitoring tools available: [log aggregation platform, APM tools, infrastructure monitoring]
- Team response procedures: [escalation paths, on-call schedules, communication channels]
- Historical context: [similar past incidents, resolution patterns, preventive measures]

⚠️ VALIDATION REQUIRED: Cross-reference with multiple data sources, verify timeline accuracy, validate business impact assessment
```

### Performance Troubleshooting
```
Diagnose performance issues in [system/application] based on these symptoms:
- Symptoms: [describe symptoms]
- Metrics: [provide available metrics]
- Recent changes: [list recent changes]
- Environment: [describe environment]

Provide systematic troubleshooting steps, potential causes, and solutions.
```

### Incident Response
```
Create an incident response runbook for [type of incident] including:
- Detection and alerting procedures
- Initial response steps
- Escalation criteria and contacts
- Investigation and diagnosis steps
- Mitigation and recovery procedures
- Post-incident review process
Include communication templates and decision trees.
```

## Configuration Management

### Ansible Playbooks
```
Write an Ansible playbook to [specific task] with:
- Target hosts: [host groups]
- Required variables and defaults
- Pre-task validations
- Main tasks with proper handlers
- Post-task verifications
- Error handling and rollback
Include inventory examples and variable files.
```

### Configuration Templates
```
Create configuration templates for [service/application] supporting:
- Multiple environments: [dev/staging/prod]
- Variable substitution for [parameters]
- Conditional sections based on [criteria]
- Validation rules and constraints
- Documentation and examples
Use [Jinja2/Helm/other templating engine].
```

## Cloud Migration and Optimization

### Cloud Migration Assessment
```
Assess [current infrastructure/application] for cloud migration to [target cloud]:
- Current architecture: [describe current state]
- Requirements: [performance/security/compliance]
- Constraints: [budget/timeline/technical]

Provide migration strategy, timeline, cost estimates, and risk assessment.
```

### Cost Optimization
```
Analyze and optimize cloud costs for [infrastructure/services] with:
- Current spending: [provide cost breakdown]
- Usage patterns: [describe usage]
- Performance requirements: [specify requirements]

Recommend cost optimization strategies including rightsizing, reserved instances, and architectural changes.
```

## 🔍 Validation Framework

### Pre-Implementation Checklist
**For Simple Tasks (🟢):**
- [ ] Review generated configuration syntax
- [ ] Test in isolated environment
- [ ] Verify against documentation

**For Moderate Tasks (🟡):**
- [ ] Peer review by experienced team member
- [ ] Integration testing with existing systems
- [ ] Security scan and validation
- [ ] Performance impact assessment

**For Complex Tasks (🔴):**
- [ ] Subject matter expert review required
- [ ] Extensive testing in staging environment
- [ ] Security team approval mandatory
- [ ] Compliance validation required
- [ ] Rollback plan documented and tested

### Context Enhancement Templates

#### Environment Context Template
```
ENVIRONMENT DETAILS:
- Infrastructure: [cloud provider, regions, network topology]
- Scale: [users, transactions/day, data volume, growth rate]
- Availability requirements: [SLA, RTO, RPO, maintenance windows]
- Security posture: [compliance frameworks, existing controls, threat model]
- Team structure: [sizes, expertise levels, on-call arrangements]
- Budget constraints: [cost limits, optimization priorities]
- Technical debt: [legacy systems, upgrade needs, integration challenges]
```

#### Platform-Specific Context Templates

##### GitHub Context Template
```
GITHUB ENVIRONMENT:
- GitHub plan: [Free, Pro, Team, Enterprise Cloud, Enterprise Server]
- Organization settings: [member privileges, repository creation, outside collaborators]
- Existing integrations: [third-party apps, webhooks, API usage]
- Security posture: [2FA enforcement, SSO, IP restrictions, audit log streaming]
- Repository patterns: [naming conventions, template repos, branch protection]
- Workflow automation: [existing Actions, project management integration]
```

##### Harness Context Template
```
HARNESS ENVIRONMENT:
- Platform version: [Harness FirstGen/NextGen, SaaS/Self-Managed]
- Modules in use: [CI, CD, FF, CE, STO, CCM, SRM]
- Delegate architecture: [locations, connectivity, scaling approach]
- Integration ecosystem: [source control, cloud providers, monitoring tools]
- Governance setup: [pipeline templates, policy engines, approval workflows]
- Resource allocation: [compute resources, storage, network bandwidth]
```

#### Technology Stack Context
```
TECHNOLOGY STACK:
- Current versions: [specific versions of all major components]
- Dependencies: [databases, message queues, caching, external services]
- Development tools: [IDEs, testing frameworks, CI/CD platforms]
- Monitoring stack: [APM, logging, metrics, alerting tools]
- Security tools: [scanners, WAF, identity providers, certificate management]
- Deployment patterns: [containers, serverless, traditional VMs]
```
