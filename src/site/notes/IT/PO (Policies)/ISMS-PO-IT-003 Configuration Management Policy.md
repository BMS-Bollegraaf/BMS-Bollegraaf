---
{"dg-publish":true,"permalink":"/it/po-policies/isms-po-it-003-configuration-management-policy/"}
---


 
**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Related Documents:** [[RelatedPolicy1\|RelatedPolicy1]], [[RelatedPolicy2\|RelatedPolicy2]]  
**Tags:** #policy #compliance  #security #dmarc #email


| Proces           | Data Protection                 |
| ---------------- | ------------------------------- |
| Document         | Configuration Management Policy |
| Scope            | IT                              |
| Revision         | 0.1                             |
| Status           | Concept                         |
| Reason of Change | Setup                           |
| Owner            | Vincent Sanders                 |
| Verified by      |                                 |
| Authorized by    |                                 |


---

## **Table of Contents**  
1. [PURPOSE](#purpose)  
2. [SCOPE](#scope)  
3. [POLICY STATEMENT](#policy statement)  
4. [FLOWCHART OF THE PROCCES](#roles-and-responsibilities)  
5. [DMARC RECORD REQUIREMENTS](#dmarc)  
6. [RESPONSIBILITIES](#responsibilities)  
7. [COMPLIANCE](#compliance)  
8. [REGISTRATION](#registrations)  
9. [RELATED DOCUMENTS](#appendices) 
10. [RELATED NORMS AND STANDARDS](#appendices) 
11. [DEFINITIES](#DEFINITIES) 

---

## **1. PURPOSE**  
To define the principles and controls for managing system and software configurations to reduce risk, ensure operational stability, and maintain security baselines across the IT environment.
## **2. SCOPE**
This policy applies to:

- All IT systems, infrastructure, network devices, endpoints, applications, cloud services, and related components
- All employees, administrators, and third parties responsible for system configuration and maintenance 
 
## **3. POLICY STATEMENTS** 
 
#### 3.1 Configuration Baselines
- All systems must be configured in accordance with **predefined secure baseline configurations** (e.g., CIS Benchmarks, vendor best practices).
- Baseline configurations must be documented and reviewed periodically.

#### 3.2 Change Control
- Changes to system configurations must follow the [[IT/PO (Policies)/ISMS-PO-IT-002 Change Management Policy\|ISMS-PO-IT-002 Change Management Policy]].
- Unauthorized or unapproved changes are prohibited and must be reported.

#### 3.3 System Hardening
- Default credentials, services, ports, and unnecessary applications must be removed or disabled.
- Secure settings must be applied for OS, middleware, databases, and applications.

#### 3.4 Configuration Documentation
- Configuration of critical systems must be **documented, version-controlled**, and stored securely.
- Documentation must include system roles, services enabled, network interfaces, and access control configurations.

#### 3.5 Monitoring and Auditing
- Systems must be monitored for configuration drift using automated tools (e.g., SCCM, Ansible, or cloud-native tools).
- Configuration audits must be conducted **at least quarterly** or after significant changes.
#### 3.6 Cloud & DevOps Environments
- Infrastructure-as-Code (IaC) templates must follow security standards and be peer-reviewed.
- Cloud resource configurations must be monitored and aligned with security requirements (e.g., using CSPM tools).

#### 3.7 Backup of Configurations
- Backups of critical configuration files must be taken **regularly** and stored securely.
- Restoration procedures must be tested as part of disaster recovery planning.

## **4. ROLES AND RESPONSIBILITIES**

| **Role**                                                | **Responsibility**                                        |
| ------------------------------------------------------- | --------------------------------------------------------- |
| [[Functions/IT Engineer\|IT Engineer]]                                         | Implement and maintain SPF, DKIM and DMARC configurations |
| [[Functions/System Owners\|System Owners]]                                       | Approve configuration changes affecting their assets      |
| [[Functions/Information Security Officer (ISO)\|Information Security Officer (ISO)]] / [[Functions/IT Manager\|IT Manager]] | Review configuration standards and perform audits         |
| Developers (if applicable)                              | Follow secure configuration and deployment practices      |

## **5. COMPLIANCE**  
Failure to comply may lead to system outages, vulnerabilities, audit findings, or disciplinary action.

## **6. REVIEW**  
This policy must be reviewed **annually** or following:

- Major system or infrastructure changes
- Internal or external audit recommendations
- Security incidents or configuration breaches

## 7. RELATED DOCUMENTS  

| Proces                                      |     |
| ------------------------------------------- | --- |
| [[IT/PO (Policies)/ISMS-PO-IT-002 Change Management Policy\|ISMS-PO-IT-002 Change Management Policy]] |     |
| Asset Management Policy                     |     |
| Secure Coding Guidelines                    |     |
| Incident Response Procedure                 |     |
| [[IT/PO (Policies)/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]   |     |
| System Hardening Standards                  |     |
## 8. RELATED NORMS AND STANDARDS

| Management standards |     |     |
| -------------------- | --- | --- |
|                      |     |     |
|                      |     |     |












