---
{"dg-publish":true,"permalink":"/it/procudures/isms-pr-010-data-restoration-procedure/","tags":["restore","procedure"],"noteIcon":"default"}
---

 **Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Managers\|IT Managers]] / [[Functions/ISMS Manager\|ISMS Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**Related Documents:**
**ISO/IEC 27001 Controls:** 8.12, 5.25, 5.31

---
## **1. PURPOSE**  
To provide a clear and secure process for restoring data from backups in the event of accidental deletion, data corruption, system failure, or other business disruptions.
## **2. SCOPE**
This procedure applies to:
- All critical systems listed in the **Critical Systems Register**
- All organizational backups managed by IT
- All restoration events triggered by users, incidents, or audits
## **3. WHEN TO TRIGGER A RESTORE** 
 - File, email, or database accidentally deleted
- Data corruption due to software failure
- Malicious activity (e.g., ransomware)
- During recovery testing or audit requests
## **4. REQUESTING A DATA RESTORE**

| Step | Action                                                                                      |
| ---- | ------------------------------------------------------------------------------------------- |
| 1    | Submit a **Restore Request Form** or ticket to IT                                           |
| 2    | Include the system name, file/data details, date/time of last known good state, and urgency |
| 3    | Request reviewed by [[IT/IT\|IT]] + [[Functions/System Owners\|System Owners]]                                              |
| 4    | Approval documented for audit trail                                                         |
## **5. RESTORE EXECUTION PROCESS**  

| Step | Action                                                                                   |
| ---- | ---------------------------------------------------------------------------------------- |
| 1    | Identify and retrieve correct backup version                                             |
| 2    | Restore data to target environment:Original location (overwrite), or                     |
| 3    | Validate restoration success with requester                                              |
| 4    | Document outcome and close request                                                       |
| 5    | If restoration fails, escalate to backup vendor or initiate disaster recovery procedures |
## **6. RESTORE AND ACCESS CONTROL**  
- Restore jobs can only be performed by authorized **[[IT/IT\|IT]]
- Access to restored files must be reviewed and logged
- Sensitive data must only be restored to **approved systems**
## **7. LOGGING AND DOCUMENTATION**  
- Each restore event must be recorded in the **Restore Test Log**
- Log includes:
    - Date/time of request and restore
    - Requestor and approver
    - System and data description
    - Success/failure and follow-up actions
## **8. TESTING AND VALIDATION**
- Restoration tests must be:
    - Conducted monthly for critical systems
    - Logged with screenshots or verification checks
- Failed tests must trigger a **backup escalation review**
## **9. ROLES AND RESPONSIBILITIES**

| Role              | Responsebility                              |
| ----------------- | ------------------------------------------- |
| Requester         | Submit complete restore request             |
| [[Functions/IT Support\|IT Support]]    | Assess, perform, and validate restore       |
| [[Functions/System Owners\|System Owners]] | Approve request, assist with validation     |
| [[Functions/ISMS Manager\|ISMS Manager]]  | Audit restore logs and review test outcomes |
## **10. REVIEW AND MAINTANCE**
Procedure reviewed **annually**, or after:
- Major IT infrastructure change
- Incident involving data loss or corruption
- Failed restoration audit
## **11.RELATED DOCUMENTS**

| Process                                               |
| ----------------------------------------------------- |
| [[IT/Procudures/ISMS-PR-009 Data Backup and Restoration Procedure\|ISMS-PR-009 Data Backup and Restoration Procedure]] |
| Critical Systems Register                             |
| Restore Request Form (fillable PDF)                   |
| Restore Test Log                                      |
| [[IT/Procudures/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]       |








