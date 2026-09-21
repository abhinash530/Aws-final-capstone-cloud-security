# AWS Final Capstone Project — Project Summary

## 1. Project Title

**Secure AWS Cloud Architecture and Security Assessment**

---

## 2. Project Overview

This project is a comprehensive cloud-security capstone focused on designing, assessing, and documenting a secure Amazon Web Services (AWS) environment for a representative web application.

The project combines cloud architecture with practical cybersecurity principles including Identity and Access Management (IAM), network segmentation, data protection, encryption, logging, monitoring, threat modeling, security testing, incident response, risk assessment, and remediation.

The architecture is designed using a defense-in-depth approach. Public-facing application components are separated from sensitive backend resources, access is controlled through IAM and Security Groups, sensitive data is protected using encryption, and AWS-native logging and monitoring capabilities are incorporated to improve visibility and incident response.

---

## 3. Problem Statement

Cloud environments can become exposed to security threats because of:

- Excessive IAM permissions
- Publicly accessible storage
- Unrestricted network access
- Inadequate encryption
- Insufficient logging
- Weak monitoring
- Misconfigured cloud resources
- Poorly controlled administrative access

The purpose of this project is to design a cloud environment that addresses these risks through layered security controls and a structured security assessment process.

---

## 4. Project Objectives

The project objectives are:

1. Design a secure AWS cloud architecture.
2. Apply least-privilege identity management.
3. Implement network segmentation.
4. Protect sensitive information.
5. Apply encryption at rest and in transit.
6. Configure audit logging.
7. Design security monitoring and alerting.
8. Identify cloud security risks.
9. Develop security testing procedures.
10. Create a remediation strategy.
11. Document incident-response procedures.
12. Demonstrate practical cloud-security knowledge.

---

## 5. AWS Services and Components

| Component | Purpose |
|---|---|
| Amazon VPC | Isolated cloud network |
| Public/Application Subnet | Controlled application exposure |
| Private Subnet | Protection of sensitive resources |
| Amazon EC2 | Application workload |
| Amazon S3 | Object and data storage |
| AWS IAM | Identity and access management |
| AWS KMS | Encryption key management |
| AWS CloudTrail | Audit logging |
| Amazon CloudWatch | Monitoring and alerting |
| Security Groups | Network traffic control |

---

## 6. Security Architecture

```text
                         INTERNET
                             |
                             v
                  +----------------------+
                  | Controlled Web Entry |
                  +----------------------+
                             |
                             v
                  +----------------------+
                  |       AWS VPC        |
                  +----------------------+
                       /             \
                      /               \
                     v                 v
              APPLICATION TIER     PRIVATE DATA TIER
                   |                    |
                   v                    v
              +---------+          +---------+
              |   EC2   | -------> | Database|
              |   App   |          | Service |
              +---------+          +---------+
                   |
                   v
              +---------+
              |   S3    |
              | Storage |
              +---------+

             SECURITY SERVICES
             -----------------
             IAM
             KMS
             CloudTrail
             CloudWatch
