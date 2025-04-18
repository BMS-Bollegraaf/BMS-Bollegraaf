---
{"dg-publish":true,"permalink":"/it/po-policies/isms-po-it-004-backup-and-recovery-policy/","tags":["Backup","recovery","policy"],"noteIcon":"default"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 5.30, 5.31, 8.13

---
## **Table of Contents**  
1. [PURPOSE](#purpose)  
2. [SCOPE](#scope)  
3. [POLICY STATEMENT](#policy-statement)  
4. [ROLES AND RESPONSIBILITIES](#roles-and-responsibilities)  
5. [COMPLIANCE](#compliance)  
6. [REVIEW](#review)   
7. [RELATED DOCUMENTS](#related-documents)   

---
## **1. PURPOSE**  
To ensure that critical data and systems can be recovered in the event of data loss, system failure, or disaster, and to maintain the availability and integrity of organizational information.

## **2. SCOPE**
This policy applies to:
- All production systems, servers, cloud storage, endpoints, and databases
- All business units, employees, and third-party providers responsible for data backup and recovery 
 
## **3. POLICY STATEMENTS** 

 #### 3.1 Backup Requirements
- All critical systems and data must be backed up in accordance with the **Data Classification Scheme**.
- Backups must be performed **at least daily** for critical data and systems
#### 3.2 Backup Types
- Full backups: Weekly
- Incremental or differential backups: Daily
- Snapshot/backups for virtual machines: Based on system criticality
#### 3.3 Storage and Retention
- Backups must be stored in:
    - A secure offsite location, cloud service, or secondary data center
    - An encrypted format
- Retention periods:
    - Critical business data: Minimum **90 days**
    - Legal/regulatory data: As defined in **Data Retention Policy**    
#### 3.4 Recovery
- Restoration procedures must be documented for all critical systems.
- Recovery Point Objectives (RPOs) and Recovery Time Objectives (RTOs) must be defined per system or service.
- A **test restore** must be performed and logged **at least quarterly**.
#### 3.5 Access Control
- Backup media and recovery consoles must be accessible only to authorized personnel.
- Audit logs must be enabled for all backup and restore actions.
#### 3.6 Cloud and SaaS Backups
- For cloud platforms (e.g., M365, Google Workspace), ensure that backups are:
    - Enabled and managed via native tools or third-party solutions
    - Aligned with internal retention and recovery standards



## **4. ROLES AND RESPONSIBILITIES**

| **Role**                  | **Responsibility**                                       |
| ------------------------- | -------------------------------------------------------- |
| [[Functions/IT Engineer\|IT Engineer]]           | Execute, monitor, and test backups and restores          |
| [[Functions/System Owners\|System Owners]]         | Define RTO/RPO and validate recovery capabilities        |
| [[Functions/ISMS Manager\|ISMS Manager]]          | Ensure compliance with backup policy and audit readiness |
| [[Functions/Third-Party Providers\|Third-Party Providers]] | Adhere to contractual backup and security requirements   |
## **5. COMPLIANCE**  
Non-compliance may result in loss of critical data, business disruption, or regulatory violations, and will be subject to disciplinary or contractual penalties.

## **6. REVIEW**  
This policy must be reviewed **annually** or after:

- Major system or infrastructure changes
- Backup or recovery failures
- Audit findings or legal requirement changes

## 7. RELATED DOCUMENTS  

| Proces                                                             |
| ------------------------------------------------------------------ |
| Business Continuity Plan (BCP)                                     |
| Disaster Recovery Plan (DRP)                                       |
| [[IT/PO (Policies)/ISMS-PO-SEC-003 Information Classification and Handling Policy\|ISMS-PO-SEC-003 Information Classification and Handling Policy]] |
| [[IT/PO (Policies)/ISMS-PO-IT-005 Patch Management Policy\|ISMS-PO-IT-005 Patch Management Policy]]                         |
| [[IT/PO (Policies)/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]                          |









