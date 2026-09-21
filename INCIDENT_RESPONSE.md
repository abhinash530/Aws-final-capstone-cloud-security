# AWS Cloud Security Incident Response Plan

## 1. Purpose

This document defines the incident-response framework for the Final Capstone AWS Cloud Security Project.

The purpose of this plan is to provide a structured approach for detecting, analyzing, containing, investigating, remediating, and recovering from security incidents affecting the AWS cloud environment.

The plan is designed around the following incident-response lifecycle:

1. Preparation
2. Detection
3. Triage and Analysis
4. Containment
5. Evidence Preservation
6. Eradication
7. Recovery
8. Post-Incident Review

All response activities must be performed only against AWS resources for which appropriate authorization has been obtained.

---

# 2. Incident Response Objectives

The primary objectives are:

- Detect security incidents as early as possible.
- Protect critical cloud resources.
- Limit the impact and scope of an incident.
- Preserve relevant security evidence.
- Identify the root cause.
- Remove malicious or unauthorized activity.
- Restore secure operations.
- Document the incident.
- Improve security controls after the incident.

---

# 3. Incident Response Lifecycle

```text
                 PREPARATION
                     |
                     v
                  DETECTION
                     |
                     v
                TRIAGE / ANALYSIS
                     |
                     v
                 CONTAINMENT
                     |
                     v
             EVIDENCE PRESERVATION
                     |
                     v
                 ERADICATION
                     |
                     v
                  RECOVERY
                     |
                     v
             POST-INCIDENT REVIEW
                     |
                     +------------+
                                  |
                                  v
                         SECURITY IMPROVEMENT
