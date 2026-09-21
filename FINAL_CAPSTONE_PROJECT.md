# Final Capstone Project
# Secure AWS Cloud Architecture and Security Assessment

## 1. Project Overview

This final capstone project demonstrates the design of a secure cloud environment using Amazon Web Services (AWS). The project integrates cloud architecture, identity and access management, network security, data protection, encryption, security monitoring, logging, threat assessment, security testing, incident response, and remediation planning.

The project is designed around a representative web application that requires a secure and scalable cloud infrastructure. The architecture separates public-facing application components from sensitive internal resources and applies defense-in-depth security principles throughout the environment.

The project demonstrates how cloud security controls can be incorporated from the architecture and design stage rather than being treated only as a post-deployment activity.

---

## 2. Project Objectives

The main objectives are:

1. Design a secure AWS cloud architecture for a practical application.
2. Implement the principle of least privilege for cloud identities.
3. Design appropriate network segmentation.
4. Protect sensitive information using encryption and access controls.
5. Configure cloud logging and security monitoring.
6. Identify potential cloud security risks and misconfigurations.
7. Develop security testing and validation procedures.
8. Analyze technical and business impact.
9. Develop a structured remediation strategy.
10. Document the complete cloud security lifecycle.

---

## 3. Proposed Use Case

The proposed environment represents a web application hosted in AWS.

The application consists of:

- Public application access
- Application workloads
- Private database services
- Object storage
- Identity management
- Encryption services
- Audit logging
- Security monitoring

The architecture is designed so that users can access the application while sensitive backend resources remain protected from unnecessary internet exposure.

---

## 4. AWS Services Used

| AWS Service | Purpose | Security Role |
|---|---|---|
| Amazon VPC | Network environment | Network isolation |
| Public Subnet | Public-facing resources | Controlled external access |
| Private Subnet | Sensitive resources | Reduced exposure |
| Amazon EC2 | Application workload | Compute security |
| Amazon S3 | Object storage | Data protection |
| AWS IAM | Identity management | Authentication and authorization |
| AWS KMS | Key management | Encryption |
| AWS CloudTrail | Audit logging | Accountability |
| Amazon CloudWatch | Monitoring | Detection and alerting |
| Security Groups | Traffic control | Network security |

---

# 5. Secure Cloud Architecture

## 5.1 Logical Architecture

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
             PUBLIC SUBNET       PRIVATE SUBNET
                  |                   |
                  v                   v
            +-----------+       +-----------+
            | EC2       |       | Database  |
            | Application|      | Service   |
            +-----------+       +-----------+
                  |
                  v
            +-----------+
            | Amazon S3 |
            | Storage   |
            +-----------+

          SECURITY AND GOVERNANCE
          -----------------------
          IAM
          KMS
          CloudTrail
          CloudWatch
