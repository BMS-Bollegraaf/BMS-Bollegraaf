---
{"dg-publish":true,"permalink":"/it/po-policies/isms-po-it-022-ninja-rmm-usage-policy/","tags":["NinjaRMM","NinjaOne","policy"],"noteIcon":"default"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 

---
## **1. PURPOSE**  
To define secure, auditable, and compliant usage of **NinjaRMM (NinjaOne)** for system monitoring, patch management, endpoint control, and remote support activities.
## **2. SCOPE**
To define secure, auditable, and compliant usage of **NinjaRMM (NinjaOne)** for system monitoring, patch management, endpoint control, and remote support activities.
 
## **3. POLICY STATEMENTS** 
 NinjaRMM may be used for:
- System health and performance monitoring
- Security patch and software deployment
- Remote desktop and remote support access
- Automation of endpoint tasks (approved scripts only)
- Asset inventory, warranty, and software tracking
- Early detection and response to security threats
## **4. ACCESS CONTROL REQUIREMENTS**
- Only authorized IT personnel may access the RMM console
- All access must be:
    - **Individually assigned** (no shared logins)
    - Protected by **Multi-Factor Authentication (MFA)**
    - Assigned least privilege based on role
- Admin-level access must be approved by the **[[Functions/ISMS Manager\|ISMS Manager]]**
## **5. SECURITY & CONFIGURATION STANDARDS**  
- All endpoints enrolled must:
    - Be **corporate-owned or fully managed BYOD**
    - Have up-to-date antivirus/EDR
    - Be encrypted (BitLocker)
- NinjaRMM agents must not be removed or bypassed
- Remote file transfer must be:
    - Logged
    - Justified by ticket/change request
    - Limited to assigned devices
## **6. SCRIPTING AND AUTOMATION**  
- All scripts must be:
    - Reviewed and tested before production use
    - Stored in a central script repository
    - Approved by a technical lead or ISMS if sensitive
- Execution logs must be retained for **12 months**
## **7. MONITORING AND LOGGING**  
- All remote sessions, script actions, and alerts must be logged
- Logs must include user, date/time, action, and target system
- Logs reviewed:
    - Monthly (by [[IT/IT\|IT]] team)
    - Quarterly (by [[Functions/ISMS Manager\|ISMS Manager]] or internal auditor)
## **8. CHANGE & INCIDENT INTEGRATION**
- Any major automation or agent config changes must follow **[[IT/PR (Procedures)/ISMS-PR-IT-002 Change Management Procedure\|ISMS-PR-IT-002 Change Management Procedure]]**
- Security alerts are to be linked with **[[IT/PR (Procedures)/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]**
- RMM can be used to **quarantine or isolate compromised assets**
## **9. DEPROVISONING**
- RMM access is revoked:  
    - Within 24 hours of role or employment termination
    - If non-compliance or policy breach is detected
- Devices removed from inventory must have agent uninstalled and access revoked
## **10. ACCEPTABLE USE**
✅ Allowed:
- Approved script execution
- Remote troubleshooting with ticket reference
- Scheduled patch deployment

🚫 Not Allowed:
- Personal or non-corporate device management
- Unapproved monitoring of users
- Unsanctioned access to data or credentials

## **11.ROLES AND RESPONSIBILITIES**

| Role              | Responsibility                           |
| ----------------- | ---------------------------------------- |
| [[Functions/IT Engineer\|IT Engineer]]   | Maintain and use RMM securely            |
| [[IT/IT\|IT]]            | Review alerts, logs, and integrations    |
| [[Functions/ISMS Manager\|ISMS Manager]]  | Approve access and perform audits        |
| [[Functions/System Owners\|System Owners]] | Coordinate patching and monitoring needs |
## **12. REVIEW AND MAINTENANCE**
Reviewed **annually** or upon:
- RMM platform changes
- Access expansion
- Security incident
## **13. RELATED DOCUMENTS**

| Process                                         |
| ----------------------------------------------- |
| [[IT/PR (Procedures)/ISMS-PR-IT-002 Change Management Procedure\|ISMS-PR-IT-002 Change Management Procedure]]  |
| [[IT/PO (Policies)/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]       |
| [[IT/SOP (Standard Operating Procedure)/ISMS-SOP-IT-REMOTE Remote Access SOP\|ISMS-SOP-IT-REMOTE Remote Access SOP]]        |
| [[IT/PR (Procedures)/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]] |
| NinjaRMM Access Register                        |
| Script Approval Log                             |
| Patch Deployment Record                         |
|                                                 |








