---
{"dg-publish":true,"permalink":"/it/pr-procedures/isms-pr-sec-014-ftp-access-procedure/","tags":["FTP","procedure"],"noteIcon":"lightbulb"}
---


**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/Information Security Officer (ISO)\|Information Security Officer (ISO)]] / [[Functions/ISMS Manager\|ISMS Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 8.4, 8.10, 5.36

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
To provide a secure and consistent method for **requesting, approving, granting, monitoring, and revoking** access to FTP/SFTP/FTPS services used to transfer business data.
## **2. SCOPE**
Applies to:
- All FTP, SFTP, and FTPS access used for internal or third-party file exchange
- All staff, contractors, vendors, or clients requesting access
- All servers or endpoints configured to support file transfer
## **3. ACCESS REQUEST PROCESS** 
 
| Step | Action                                                                                                                                          |
| ---- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| 1    | Requester submits the **FTP Access Request Form** via TOPdesk                                                                                   |
| 2    | Form must include:- Type of access: SFTP, FTPS, Read/Write<br>- Target system or IP<br>- File types and frequency  <br>- Business justification |
| 3    | Approvals required from:    <br>- **Data Owner** (if sensitive data involved)    <br>- **IT Security**                                          |
| 4    | IT Admin creates credentials and applies:<br><br>- Role-based Access<br>- Directory restrictions<br>- IP whitelisting                           |
| 5    | Credentials shared securely (e.g., password manager or vault invite)                                                                            |
| 6    | Access details are logged in the **Access Control Register**                                                                                    |
## **4. SECURITY CONTROLE**

- Enforce strong password policy and **MFA if supported**
- Log all connections and file transfers
- Disallow auto-execution of transferred files
- Encrypt sensitive files before transfer
- Data retention limited to [e.g., 14 days] on FTP directories
## **5. ACCESS REVIEW & LOGGING**  
- Review access logs weekly for anomalies
- Conduct **quarterly access reviews** with data owners
- Expired or inactive accounts auto-disabled after [e.g., 30 days of inactivity]
## **6. REVOCATION PROCESS**  
Access is revoked:
- Immediately upon project or contract end
- During offboarding
- Upon policy violation or investigation trigger
- Automatically after expiry (if date was specified at creation)
## **7. AUDIT AND COMPLIANCE**  
- FTP access activities are included in internal ISMS audits
- Logs retained for **at least 90 days**
- All procedures must be tested annually in ISMS process validation
## **8. ROLES AND RESPONSIBILITIES**

| Role             | Responsibility                                       |
| ---------------- | ---------------------------------------------------- |
| Requester        | Complete request accurately and follow usage rules   |
| [[Functions/Data Owner\|Data Owner]]   | Approve use if sensitive or classified data involved |
| [[Functions/IT Engineer\|IT Engineer]]  | Configure secure FTP access and monitor logs         |
| [[Functions/ISMS Manager\|ISMS Manager]] | Audit access, logs, and enforce policy controls      |
## **9. RELATED DOCUMENTS**

| Process                                         |
| ----------------------------------------------- |
| [[IT/PO (Policies)/ISMS-PO-SEC-014 FTP Access Policy\|ISMS-PO-SEC-014 FTP Access Policy]]           |
| [[IT/PO (Policies)/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]       |
| [[IT/PR (Procedures)/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]] |
| FTP Access Request Form (TOPdesk)               |
| Access Control Register                         |
| Data Classification Guidelines                  |








