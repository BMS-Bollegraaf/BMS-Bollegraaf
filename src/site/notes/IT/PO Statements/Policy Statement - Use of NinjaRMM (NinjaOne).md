---
{"dg-publish":true,"permalink":"/it/po-statements/policy-statement-use-of-ninja-rmm-ninja-one/","tags":["statement","RMM","NinjaOne","NinjaRMM"]}
---

 **Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]] / [[Functions/ISMS Manager\|ISMS Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 5.10, 8.1, 8.23, 5.25, 5.31

---
## **Table of Contents**  
1. [PURPOSE](#purpose)  
2. [SCOPE](#scope)  
3. [POLICY STATEMENTS](#policy-statement)  
4. [ROLES AND RESPONSIBILITIES](#roles-and-responsibilities)  
5. [COMPLIANCE](#compliance)  
6. [REVIEW](#review)  
7. [RELATED DOCUMENTS](#related-documents)  
8. [CONTROLS](#controls)  

---
## **1. PURPOSE**  
To define the secure, responsible, and auditable use of **[[IT/Applications/NinjaRMM (NinjaOne)/NinjaRMM\|NinjaRMM]]** for IT systems management, endpoint security, remote access, and monitoring in alignment with ISMS requirements.
## **2. SCOPE**
To define the secure, responsible, and auditable use of **[[IT/Applications/NinjaRMM (NinjaOne)/NinjaRMM\|NinjaRMM]]** (NinjaOne) for IT systems management, endpoint security, remote access, and monitoring in alignment with ISMS requirements.
 
 ## **3. POLICY STATEMENTS** 
 NinjaRMM may be used for:
- Remote access and troubleshooting of corporate devices
- Patching and update deployment
- Endpoint health monitoring and automated remediation
- Asset tracking and inventory reporting
- Alerting for security or performance events
- Scripted tasks approved by IT leadership
## **4. ACCESS CONTROL & AUTHENICATION**
- All NinjaRMM users must use **individual accounts** with **role-based permissions**
- **Multi-Factor Authentication (MFA)** is required
- **Admin-level access** must be approved by the ISMS Manager
- Access rights are reviewed **quarterly**
## **5. MONITORING & ACTIVITY LOGGIN**  
- All remote sessions and script executions must be **logged and timestamped**
- Audit logs must be retained for **12 months** and reviewed during access audits
- Admins must not disable endpoint agents or suppress alerts without valid reason
## **6. SECURITY CONTROLS**  
- Agent software must be deployed to only **approved company-managed devices**
- Scripts must be **reviewed and tested** in sandbox environments before use
- NinjaRMM integrations (e.g., antivirus, backup, ticketing) must be authorized by IT leadership
- Remote file transfers must be approved and logged in tickets or change requests
## **7. INCIDENT RESPONSE INTEGRATION**  
- All endpoint alerts tied to potential threats must be linked to **[[IT/PR (Procedures)/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]**
- NinjaRMM is used as part of the organization’s **early-warning and containment system**
- Compromised assets should be **isolated via RMM agent** if appropriate
## **8. ASSET LIFECYCLE INTEGRATION**
- All enrolled devices must be tracked in the **IT Asset Register [[IT/Applications/TOPDesk/TOPdesk\|TOPdesk]]** 
- Devices must be **deprovisioned from RMM** upon retirement, reassignment, or disposal
- Use of NinjaRMM on BYOD is not allowed unless explicitly approved
## **9. ACCEPTABLE USE GUIDELINES**
- Do **not use** RMM access for non-business or personal troubleshooting
- Do **not share login credentials or use shared accounts**
- Do **not run scripts without documented change tickets** (unless pre-approved automation)
## **10. ROLES AND RESPONSIBILITIES**

| Role             | Resonsibility                                             |
| ---------------- | --------------------------------------------------------- |
| [[Functions/IT Engineer\|IT Engineer]]  | Use RMM platform in line with this policy, log actions    |
| [[Functions/IT Manager\|IT Manager]]   | Monitor alerts and integrate with SIEM/EDR                |
| [[Functions/ISMS Manager\|ISMS Manager]] | Conduct quarterly access reviews and policy audit         |
| End Users        | Report any suspicious RMM activity or unauthorized access |
## **11. REVIEW & UPDATES**
This policy is reviewed **annually**, or after:
- A major security incident involving RMM use
- Deployment of a new automation or RMM module
- Expansion of contractor/MSP access
## **12. RELATED DOCUMENTS**

| Process                                          |
| ------------------------------------------------ |
| [[IT/PO (Policies)/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]        |
| [[IT/PR (Procedures)/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]  |
| [[IT/PR (Procedures)/ISMS-PR-IT-004 IT Asset Management Procedure\|ISMS-PR-IT-004 IT Asset Management Procedure]] |
| [[IT/SOP (Standard Operating Procedure)/ISMS-SOP-IT-REMOTE Remote Access SOP\|ISMS-SOP-IT-REMOTE Remote Access SOP]]         |
| NinjaRMM Script Approval Log                     |
| NinjaRMM Access Request Form                     |




