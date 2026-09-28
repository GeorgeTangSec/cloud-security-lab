# Cloud Security Engineering Lab

Hands-on cloud security engineering portfolio focused on designing, deploying, securing, monitoring, and automating enterprise AWS environments.

This repository documents practical cloud security work across Linux, Git, AWS Organizations, IAM, Terraform, networking, centralized logging, threat detection, incident response, DevSecOps, Kubernetes, and AI-assisted security operations.

## Flagship Project

### FortressCloud — Enterprise AWS Multi-Account Security Foundation

FortressCloud is an enterprise-style AWS security architecture built across 7 Organizational Units and 16 AWS accounts.

The environment is designed to demonstrate centralized governance, separation of duties, security monitoring, logging, network isolation, policy enforcement, infrastructure as code, and scalable cloud-security operations.
## Enterprise Architecture Scope

FortressCloud is designed as a multi-account AWS environment that separates security, infrastructure, production, non-production, testing, and isolated workloads.

The environment includes:

- 1 AWS Organizations Management Account
- 7 Organizational Units (OUs)
- 15 Member Accounts
- 16 Total AWS Accounts
- Centralized security monitoring
- Centralized logging and audit capabilities
- Dedicated networking and shared-services accounts
- Production and non-production workload separation
- Service Control Policy (SCP) testing
- Quarantine capability for suspended or compromised accounts
## AWS Organization Structure

| Location | AWS Account | Purpose |
|---|---|---|
| Root | Management Account | AWS Organizations administration and organization-wide governance |
| Security OU | Security Tooling Account | Centralized Security Hub, GuardDuty, and security operations |
| Security OU | Log Archive Account | Centralized storage and protection of organization-wide security logs |
| Security OU | Audit & Compliance Account | Independent security auditing, compliance validation, and evidence collection |
| Infrastructure OU | Network Account | Centralized cloud networking and connectivity services |
| Infrastructure OU | Shared Services Account | Shared enterprise services used across AWS workloads |
| Infrastructure OU | Identity Services Account | Centralized identity and access-related services |
| Production OU | Production Application Account | Hosts production application workloads |
| Production OU | Production Data Account | Isolates production databases and sensitive data services |
| Production OU | Production Platform Account | Hosts shared production platform services |
| Non-Production OU | Development Account | Application and infrastructure development |
| Non-Production OU | Testing Account | Security, application, and integration testing |
| Non-Production OU | Staging Account | Pre-production validation before production deployment |
| Sandbox OU | Sandbox Account | Controlled experimentation and learning |
| Policy-Staging OU | SCP Testing Account | Tests Service Control Policies before wider deployment |
| Suspended OU | Quarantine Account | Isolates suspended, compromised, or restricted accounts |
## Project Status

**Status:** In Progress

FortressCloud is being built incrementally as a hands-on enterprise cloud security lab.

The organizational structure above represents the target architecture. As each component is deployed, this repository will be updated with:

- Terraform configuration
- AWS console screenshots
- Architecture diagrams
- Security control evidence
- Testing results
- Validation outputs
- Lessons learned
## Business Problem

Large organizations often operate many AWS accounts across development, production, security, networking, and shared-service environments.

Without centralized governance, this can lead to:

- Inconsistent security controls
- Excessive permissions
- Weak account separation
- Logging gaps
- Limited visibility across environments
- Misconfigured cloud resources
- Difficult compliance auditing
- Slower incident investigation and response

## Project Objectives

FortressCloud is designed to demonstrate how an enterprise AWS organization can be structured and secured using centralized governance and security controls.

Key objectives include:

- Build a scalable multi-account AWS organization
- Separate security, infrastructure, production, and non-production workloads
- Apply organization-wide security guardrails using Service Control Policies
- Centralize security logging and monitoring
- Establish secure identity and access patterns
- Deploy infrastructure using Terraform
- Validate security controls through testing and evidence
- Create a foundation for future threat detection, vulnerability management, DevSecOps, and AI-assisted security projects
## Planned Technology Stack

### AWS Governance, Identity & SSO
- AWS Organizations
- Organizational Units (OUs)
- Service Control Policies (SCPs)
- AWS Identity and Access Management (IAM)
- AWS IAM Identity Center (formerly AWS SSO)
- Cross-account Single Sign-On (SSO)
- Permission Sets
- Multi-Factor Authentication (MFA)

### Security & Compliance
- AWS Security Hub
- Amazon GuardDuty
- AWS Config
- AWS CloudTrail
- IAM Access Analyzer
- Amazon Inspector

### Networking
- Amazon VPC
- Public and Private Subnets
- Route Tables
- Internet Gateway
- NAT Gateway
- Security Groups
- Network ACLs

### Infrastructure as Code
- Terraform
- Git
- GitHub

### Monitoring & Logging
- Amazon CloudWatch
- AWS CloudTrail
- Amazon S3
- Centralized Log Archive

### Automation & Security Engineering
- Bash
- Python
- AWS CLI
- GitHub Actions
## Architecture & Evidence

FortressCloud will include professional architecture documentation and implementation evidence for each major component.

### Architecture Documentation
- AWS Organizations hierarchy
- Organizational Units and account structure
- Centralized security architecture
- Centralized logging architecture
- Identity and SSO access model
- Network architecture
- Security monitoring and incident response flow

### Implementation Evidence
- AWS console screenshots
- Terraform deployment output
- Security Hub findings
- GuardDuty findings
- AWS Config compliance evidence
- CloudTrail logging evidence
- IAM Identity Center configuration
- SCP testing and validation
- Cross-account security monitoring
- Network and VPC configuration evidence
## Repository Structure

```text
cloud-security-lab/
├── README.md
├── architecture/
│   ├── diagrams/
│   └── design-notes/
├── screenshots/
│   ├── organizations/
│   ├── identity-sso/
│   ├── security-monitoring/
│   ├── logging/
│   ├── networking/
│   └── terraform/
├── terraform/
│   ├── organizations/
│   ├── iam/
│   ├── networking/
│   ├── security/
│   └── logging/
├── scripts/
│   ├── bash/
│   └── python/
├── policies/
│   ├── scp/
│   └── iam/
├── evidence/
│   ├── security-controls/
│   ├── validation/
│   └── testing/
└── docs/
    ├── implementation-notes/
    └── lessons-learned/
## Security Design Principles

FortressCloud is designed around enterprise cloud security principles including:

- Least privilege access
- Separation of duties
- Defense in depth
- Zero Trust access principles
- Centralized logging and monitoring
- Multi-factor authentication
- Account and workload isolation
- Secure-by-default configurations
- Infrastructure as Code
- Continuous security validation
- Policy-based governance
- Human approval for high-impact security actions
## Cloud Security Portfolio Roadmap

This repository will evolve through four connected enterprise cloud security projects.

### 1. FortressCloud — Enterprise AWS Security Foundation
Build the multi-account AWS organization, identity model, networking, governance, centralized logging, security controls, and Terraform foundation.

### 2. SentinelAI — Threat Detection & Incident Response
Build centralized security monitoring, SIEM workflows, automated detection, investigation, incident response, and AI-assisted security operations across the AWS organization.

### 3. CloudRiskAI — Vulnerability & Exposure Management
Build organization-wide vulnerability management, attack-path analysis, exposure assessment, risk prioritization, and AI-assisted remediation guidance.

### 4. SecureSphere — EKS DevSecOps & Container Security
Deploy and secure containerized workloads using Docker, Kubernetes, Amazon EKS, CI/CD security controls, runtime monitoring, and software supply-chain protections.

