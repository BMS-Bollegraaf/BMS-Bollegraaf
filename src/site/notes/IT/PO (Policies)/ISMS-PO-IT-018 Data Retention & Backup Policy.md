---
{"dg-publish":true,"permalink":"/it/po-policies/isms-po-it-018-data-retention-and-backup-policy/"}
---

 
**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**Related Documents:**
**ISO/IEC 27001 Controls:** 5.10, 5.34, 8.10, 8.12, 8.14, 8.30

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
To ensure that organizational data is securely retained, backed up, and recoverable to meet legal, contractual, business continuity, and information security requirements.
## **2. SCOPE**
This policy applies to:
- All digital and physical data processed by the organization
- All employees, contractors, systems, cloud services, and backup devices
- All backup methods (on-prem, cloud, hybrid)
## **3. DATA RETENTION REQUIREMENTS** 

| Data Type           | Retention Period               | Notes                                   |
| ------------------- | ------------------------------ | --------------------------------------- |
| Financial records   | 7 years                        | Required by accounting standards        |
| HR/Employee records | 6 years after termination      | As per labor laws                       |
| Customer data       | As per contract or max 5 years | Subject to DPA/GDPR                     |
| Emails              | 3–7 years                      | Depending on sensitivity/classification |
| System logs         | 1–2 years                      | Audit and forensic readiness            |
| Security events     | 2–3 years                      | For incident investigation              |
| Project documents   | 3–5 years                      | Based on contract or internal policy    |
Retention periods must comply with applicable laws, such as GDPR, SOX, HIPAA, etc.
## **4. BACKUP REQUIREMENTS**
#### 4.1 Backup Scope
- All critical business systems, data, configurations, and endpoints must be backed up.
- This includes:
    - File servers, application servers, databases
    - Cloud storage
    - M365/Google Workspace (e.g., mail, OneDrive)
#### 4.2 Frequency
- **Daily incremental** backups for operational systems
- **Weekly full** backups stored offsite or in cloud
- **Snapshot-based** backups for virtualized/cloud systems

#### 4.3 Storage and Encryption
- Backups must be:
    - **Encrypted at rest and in transit**
    - Stored on **separate media** from live systems
    - **Immutable** or **write-protected** where supported
#### 4.4 Testing
- Backups must be tested at least **quarterly**
- Restore tests must verify data integrity and usability
#### 4.5 Retention of Backups
- Backup copies must be retained in line with data classification and risk
- Expired backups must be securely deleted or wiped

## 5. **DATA DELETION & DISPOSAL**
- Data must be deleted upon expiry of retention period unless legally required
- Deletion must follow secure wiping or cryptographic erasure standards
- Records of deletions must be maintained

## **6. ROLES AND RESPONSIBILITIES**  

| Role             | Responsibility                                                     |
| ---------------- | ------------------------------------------------------------------ |
| [[IT/IT\|IT]]           | Manage backups, ensure restore capability, monitor success/failure |
| Data Owners      | Define retention needs and classify data appropriately             |
| [[Functions/ISMS Manager\|ISMS Manager]] | Ensure policy compliance and conduct periodic audits               |
| All Staff        | Avoid storing data in unauthorized locations                       |
## **7. COMPLIANCE  
Noncompliance may result in:
- Inability to recover critical systems or data
- Breach of contractual or legal obligations
- Fines or legal liability (e.g. GDPR Article 5(e))
## **8. REVIEW
This policy must be reviewed **annually**, or after:
- Major infrastructure or cloud migrations
- Data-related incidents or loss
- Legal/regulatory updates
## **9. RELATED DOCUMENTS**

| Process                                                            |
| ------------------------------------------------------------------ |
| [[IT/PO (Policies)/ISMS-PO-SEC-003 Information Classification and Handling Policy\|ISMS-PO-SEC-003 Information Classification and Handling Policy]] |
| [[IT/PR (Procedures)/ISMS-PR-SEC-009 Secure Disposal and ReUse Procedure\|ISMS-PR-SEC-009 Secure Disposal and ReUse Procedure]]            |
| [[IT/PO (Policies)/ISMS-PO-SEC-011 Email and Communication Policy\|ISMS-PO-SEC-011 Email and Communication Policy]]                 |
| Business Continuity Plan                                           |
| Backup Schedule & Restore Test Log                                 |
| Data Retention Register                                            |







