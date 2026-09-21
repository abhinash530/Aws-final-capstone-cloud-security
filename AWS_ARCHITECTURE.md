# AWS Secure Cloud Architecture

## 1. Architecture Overview

This document describes the secure AWS architecture proposed for the Final Capstone Project.

The architecture is designed for a representative web application that requires:

- Secure internet access
- Application workload isolation
- Private data storage
- Identity-based access control
- Encryption
- Network segmentation
- Centralized logging
- Security monitoring
- Controlled administrative access

The architecture follows a defense-in-depth approach so that multiple independent security controls protect critical resources.

---

# 2. High-Level Architecture

```text
                           INTERNET
                              |
                              v
                    +-------------------+
                    | Controlled Web    |
                    | Entry Point       |
                    +-------------------+
                              |
                              v
                +---------------------------+
                |          AWS VPC          |
                |                           |
                |   Public / Application    |
                |        Subnet(s)          |
                |            |              |
                |            v              |
                |      +------------+       |
                |      | EC2 / App  |       |
                |      | Workload   |       |
                |      +------------+       |
                |            |              |
                |            v              |
                |      Private Subnet       |
                |      +------------+       |
                |      | Database   |       |
                |      | Service    |       |
                |      +------------+       |
                |                           |
                +---------------------------+

                     |              |
                     v              v
                +---------+    +----------+
                |   S3    |    |   KMS    |
                | Storage |    | Encryption|
                +---------+    +----------+

                 SECURITY & MONITORING
                 ---------------------
                 IAM
                 CloudTrail
                 CloudWatch
