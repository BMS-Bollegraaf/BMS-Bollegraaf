---
{"dg-publish":true,"permalink":"/it/pr-procedures/isms-pr-009-data-backup-and-restoration-procedure/"}
---


 
**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]] / [[Functions/ISMS Manager\|ISMS Manager]]
**Classification:**
**Related Documents:**
**ISO/IEC 27001 Controls:** 8.12, 5.31, 5.25
**Tags:** #policy #Backup

---
## **Table of Contents**  
1. [PURPOSE](#purpose)  
2. [SCOPE](#scope)  
3. [POLICY STATEMENTS](#policy statement)  
4. [ROLES AND RESPONSIBILITIES](#roles-and-responsibilities)  
5. [COMPLIANCE](#dmarc)  
6. [REVIEW](#responsibilities)  
7. [RELATED DOCUMENTS](#compliance)  
8. [CONTROLS](#registrations)  
---
## **1. PURPOSE**  
To define a structured approach to backing up and restoring data, systems, and configurations to ensure **data availability**, **business continuity**, and **protection from loss or corruption**.
## **2. SCOPE**
This procedure applies to:
- All production servers, databases, file shares, cloud services, and critical applications
- Backup media (cloud, on-prem, removable storage)
- Staff involved in configuring, managing, or validating backups
## **3. BACKUP TYPES AND FREQUENCIES**

| Type                              | Frequency                 | Retention   |
| --------------------------------- | ------------------------- | ----------- |
| Full Back-up                      | Weekly                    | 4 weeks     |
| Incremental Backup                | Daily                     | 7 days      |
| Snapshot / VM Image               | Hourly (critical systems) | 24–48 hours |
| Offsite Replication               | Daily                     | 30+ days    |
| Cloud-to-Cloud Backup (e.g. M365) | Daily                     | 90 days     |
 ## **4. BACKUP PROCEDURE**
#### 4.1 Setup
- Identify critical systems and classify data
- Configure backup policies in central platform (e.g., Veeam, Acronis, Azure)
- Encrypt backups in transit and at rest
- Store backups in **2 different physical or cloud locations**
#### 4.2 Monitoring
- Enable daily backup job notifications
- [[IT/IT\|IT]] to review **backup status reports** every morning
- Log all failures and retry within SLA
#### 4.3 Validation
- Perform **restore tests monthly** for critical systems
- Document test outcomes in the **Restore Test Log**
- Retain logs for at least 12 month.
## **5. RESTORATION PROCEDURE**  
#### When restoration is needed:
1. Submit a **Restore Request Ticket** to IT
2. Identify affected system/data and required recovery point
3. Confirm business justification and impact
4. IT retrieves data and restores to:
    - Same location (overwrite), or
    - Alternate recovery environment (sandbox/testing)
#### After restoration:
- Validate data integrity with requester
- Document restoration outcome
- Update backup register with event.
## **6. ROLES AND RESPONSIBILITY**

| Role              | Responsibilty                                                  |
| ----------------- | -------------------------------------------------------------- |
| [[IT/IT\|IT]]            | Configure and manage backups, test restorations                |
| [[Functions/System Owners\|System Owners]] | Identify recovery priorities, assist validation                |
| [[Functions/ISMS Manager\|ISMS Manager]]  | Audit backup logs, ensure retention policies align             |
| End Users         | Request restores via proper channels, verify data upon restore |
## **7. SECURITY & COMPLIANCE**  
- All backups must be **encrypted using AES-256**
- Access to backup platforms restricted to authorized personnel
- Cloud backup providers must be ISO 27001/SOC 2 certified
- Follow **GDPR/NIS2** for data retention and destruction

## **8. REVIEW & MAINTENANCE**
Procedure must be reviewed **annually**, or after:
- Significant infrastructure change
- Disaster recovery exercise
- Backup failure or audit finding
## **9. RELATED DOCUMENTS

| Process                                                                   |
| ------------------------------------------------------------------------- |
| [[IT/PO (Policies)/ISMS-PO-IT-018 Data Retention & Backup Policy\|ISMS-PO-IT-018 Data Retention & Backup Policy]]                         |
| [[IT/PR (Procedures)/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]                           |
| [[IT/PR (Procedures)/ISMS-PR-008 Business Continuity & Disaster Recovery (BC DR) Procedure\|ISMS-PR-008 Business Continuity & Disaster Recovery (BC DR) Procedure]] |
| Backup Schedule & Restore Test Log                                        |
| Restore Request Form                                                      |
| Critical Systems Register                                                 |








