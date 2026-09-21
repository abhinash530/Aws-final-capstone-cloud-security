# AWS Security Controls

## 1. Purpose

This document defines the security controls for the Final Capstone AWS Cloud Security Project.

The objective is to establish preventive, detective, corrective, and governance controls that protect identities, workloads, networks, data, encryption keys, logs, and cloud infrastructure.

The controls are designed around the following principles:

- Least privilege
- Defense in depth
- Secure configuration
- Network segmentation
- Data protection
- Encryption
- Continuous monitoring
- Auditability
- Controlled administrative access
- Risk-based remediation

---

# 2. Security Control Framework

The project organizes controls into four major categories.

| Control Type | Purpose | Examples |
|---|---|---|
| Preventive | Stop security incidents before they occur | IAM, Security Groups, encryption |
| Detective | Identify suspicious activity | CloudTrail, CloudWatch |
| Corrective | Reduce impact and restore secure state | Remediation, recovery |
| Governance | Maintain security over time | Reviews, policies, documentation |

---

# 3. Identity and Access Management Controls

AWS Identity and Access Management is one of the most important security boundaries in the architecture.

## 3.1 Least Privilege

Every identity should receive only the permissions required for its intended task.

For example, an application that only needs to read objects from a specific S3 bucket should not receive unrestricted administrative permissions.

### Security Objective

Reduce the potential impact of:

- Stolen credentials
- Compromised workloads
- Insider misuse
- Configuration errors

---

## 3.2 IAM Roles

Workloads should use IAM roles where appropriate instead of relying on long-lived credentials.

Example:

```text
Application
    |
    v
IAM Role
    |
    +---- Required S3 Access
    |
    +---- Required AWS Service Access
    |
    +---- No IAM Administration
