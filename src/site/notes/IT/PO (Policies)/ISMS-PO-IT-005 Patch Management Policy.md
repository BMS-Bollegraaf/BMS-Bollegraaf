---
{"dg-publish":true,"permalink":"/it/po-policies/isms-po-it-005-patch-management-policy/","tags":["policy","patch"],"noteIcon":"default"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 5.30, 5.31, 8.13

---
## **1. PURPOSE**  
To define a standardized approach for the identification, assessment, and timely application of patches and updates to information systems to mitigate security vulnerabilities and maintain operational stability.
## **2. SCOPE**
This policy applies to all:

- IT systems, servers, endpoints, applications, and network devices
- Operating systems and third-party software used within the organization
- Employees, contractors, and IT administrators responsible for system maintenance
 
## **3. POLICY STATEMENT** 

 ### 3.1 Patch Identification
- The IT team shall monitor vendor notifications, security advisories, and threat intelligence feeds for newly released patches.
- Critical vulnerabilities (e.g., CVSS score ≥ 7.0) must be prioritized.

### 3.2 Patch Assessment
Before deployment, patches must be evaluated for:

- Security impact
- Compatibility with existing systems
- Potential disruption to business operations

### 3.3 Patch Deployment Timelines

| Risk Level | Deployment Timeline                 |
| ---------- | ----------------------------------- |
| Critical   | Within 7 calender days              |
| High       | Within 14 calender days             |
| Medium     | Within 30 calender days             |
| Low        | As scheduled in routine maintenance |
### 3.4 Testing
Non-critical patches must be tested in a staging environment before being applied to production systems.
### 3.5 Change Control
All patching activities must follow the Change Management Procedure, including:

- Risk assessment
- Scheduling
- Approval (where required)
- Rollback plan
### 3.6 Exceptions
- Any deviation from this policy (e.g., business constraint, compatibility issue) must be documented and approved by the [[Functions/Information Security Officer (ISO)\|Information Security Officer (ISO)]] with appropriate mitigation in place.
### 3.7 Logging and Monitoring
- Patching activities must be logged.
- Patch status should be monitored via a centralized dashboard or endpoint management tool.

## **4. ROLES AND RESPONSIBILITIES

| Role                                   | Responsibility                    |
| -------------------------------------- | --------------------------------- |
| [[Functions/IT Engineer\|IT Engineer]]                        | Identify, test, and apply patches |
| [[Functions/Information Security Officer (ISO)\|Information Security Officer (ISO)]] | Evaluate patch urgency and risk   |
| Asset Owners                           | Coordinate downtime for patching  |
| [[Functions/IT Manager\|IT Manager]]                         | Periodically review compliance    |

## **5.  COMPLIANCE AND ENFORCEMENT**
Failure to comply with this policy may result in increased security risk, data breaches, or disciplinary actions in line with the organization's policies.
## **6. REVIEW AND UPDATES**
This policy shall be reviewed annually or after a major security incident or significant infrastructure change.
## **7. RELATED DOCUMENTS  

| Proces                                        |
| --------------------------------------------- |
| Change Management Procedure                   |
| [[IT/PO (Policies)/ISMS-PO-SEC-007 Malware Protection Policy\|ISMS-PO-SEC-007 Malware Protection Policy]] |
| Configuration Management Policy               |
| Vulnerability Management Procedure            |
| Information Security Policy                   |











