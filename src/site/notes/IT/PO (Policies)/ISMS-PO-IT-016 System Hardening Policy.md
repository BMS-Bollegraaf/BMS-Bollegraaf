---
{"dg-publish":true,"permalink":"/it/po-policies/isms-po-it-016-system-hardening-policy/","noteIcon":"default"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Related Documents:**
**ISO/IEC 27001 Controls:** 8.9, 8.7, 5.32, 8.8
**Tags:** #policy #compliance  #security #dmarc #email

---
## **1. PURPOSE**  
To define minimum security configuration standards for all IT systems and ensure they are protected from exploitation due to unnecessary services, default settings, or insecure configurations.
## **2. SCOPE**
This policy applies to:
- All servers, workstations, laptops, mobile devices, firewalls, switches, cloud instances, and virtual machines
- Operating systems, middleware, applications, and databases
- All new deployments and existing systems under management
## **3. POLICY STATEMENTS** 
#### 3.1 Baseline Configuratio,
- All systems must be deployed using an **approved secure baseline**.
- Baselines must follow:
    - CIS Benchmarks (where available)
    - Vendor best practices
    - Regulatory and business requirements
#### 3.2 Default Settings
- Remove or disable:
    - Default accounts or credentials
    - Unused ports and protocols
    - Sample files or demo applications
- Rename default admin accounts where possible

#### 3.3 Patch and Update Management
- Systems must be patched regularly based on the **[[ISMS-PO-IT-005 Patchmanagement Policy**.
- Automated updates must be enabled where appropriate.
#### 3.4 Access Control
- Only authorized users should have system-level access.
- Root/Administrator privileges must be restricted and monitored.
- Use of **Multi-Factor Authentication (MFA)** is mandatory for administrative access.
#### 3.5 Antivirus / EDR
- All endpoints and servers must have approved anti-malware or **Endpoint Detection & Response (EDR)** tools installed and active.
#### 3.6 Logging and Monitoring
- Logging must be enabled for:
    - Login attempts
    - Privileged commands
    - System changes
- Logs must be forwarded to a **centralized logging system or SIEM**.

#### 3.7 Remote Access Hardening
- Remote access tools (e.g., RDP, SSH, VPN) must:
    - Use encryption (TLS, IPsec)
    - Require MFA
    - Be restricted by IP or time where feasible
#### 3.8 Cloud Environments
- Hardened images must be used for cloud instances (e.g., AWS AMIs, Azure VM templates).
- Public exposure of ports and services must be avoided unless explicitly approved.
## **4. ROLES AND RESPONSIBILITIES**

| **Role**          | **Responsibility**                                        |
| ----------------- | --------------------------------------------------------- |
| [[IT/IT\|IT]] / DevOps   | Implement and maintain hardened configurations            |
| [[Functions/IT Manager\|IT Manager]]    | Define baselines, audit compliance, and enforce standards |
| [[Functions/System Owners\|System Owners]] | Approve deviations and support remediation                |
| [[Functions/ISMS Manager\|ISMS Manager]]  | Monitor policy compliance and escalate risks              |
## **5. EXCEPTIONS**
All deviations from the hardening standards must be documented with:
- Justification
- Risk assessment
- Compensating controls
- Approval by the ISMS Manager
## **6. REVIEW**  
This policy must be reviewed **annually** or:
- After a major security incident
- After a change in threat landscape or regulatory environment
- After the release of new systems or platforms
## **7. RELATED DOCUMENTS**  

| Proces                                                  |
| ------------------------------------------------------- |
| [[IT/PO (Policies)/ISMS-PO-IT-005 Patch Management Policy\|ISMS-PO-IT-005 Patch Management Policy]]              |
| [[IT/PO (Policies)/ISMS-PO-IT-003 Configuration Management Policy\|ISMS-PO-IT-003 Configuration Management Policy]]      |
| [[IT/PO (Policies)/ISMS-PO-SEC-008 Logging and Monitoring Policy\|ISMS-PO-SEC-008 Logging and Monitoring Policy]]       |
| [[IT/PR (Procedures)/ISMS-PR-SEC-009 Secure Disposal and ReUse Procedure\|ISMS-PR-SEC-009 Secure Disposal and ReUse Procedure]] |
| System Hardening Checklists (Windows, Linux, Cloud)     |






