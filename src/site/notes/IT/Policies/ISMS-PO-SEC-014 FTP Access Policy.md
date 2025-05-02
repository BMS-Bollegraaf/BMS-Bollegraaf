---
{"dg-publish":true,"permalink":"/it/policies/isms-po-sec-014-ftp-access-policy/","tags":["policy","FTP"],"noteIcon":"default"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Managers\|IT Managers]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 

---
## **1. PURPOSE**  
To define the acceptable, secure, and monitored use of **FTP (File Transfer Protocol)** services for transferring organizational data between internal systems and external parties.
## **2. SCOPE**
This policy applies to:
- All users who request or manage access to **FTP, SFTP, or FTPS** services
- All departments and third parties exchanging files with the organization
- All FTP servers, clients, and transfer platforms hosted or used by the company
## **3. POLICY STATEMENTS** 
- Only **secure protocols** (SFTP or FTPS) are permitted; unencrypted FTP is prohibited
- All FTP accounts must be:
    - Individually assigned (no shared accounts)
    - Configured with **strong passwords** and **MFA where supported**
    - Logged and reviewed **quarterly**
- Data transfers must be:
    - **Encrypted in transit** (e.g., SFTP over SSH or FTPS over TLS)
    - Logged and monitored via FTP logs or SIEM tools
- Access to FTP servers must be **approved, time-limited**, and linked to a **business need**
- All inbound/outbound file transfers must follow **data classification and handling procedures**
- Sensitive files must be **zipped with encryption/password protection** prior to upload/download
## **4. REQUEST & APPROVAL PROCESS**

| **Step** | **Action**                                                                        |
| -------- | --------------------------------------------------------------------------------- |
| 1        | Submit an **FTP Access Request Form** (TOPdesk)                                   |
| 2        | Request must include system name, IPs, contact person, transfer schedule          |
| 3        | Approval by **IT Security + Data Owner** required                                 |
| 4        | IT issues credentials and updates **Access Register**                             |
| 5        | Access expires automatically or is reviewed after [e.g., 90 days] unless extended |
## **5. SECURITY CONTROLS**  
- Directory-level access only (chroot or jailed session)
- FTP server firewall ports must be restricted by **IP whitelisting**
- No automatic file execution on FTP upload
- Files should not persist longer than [e.g., 14 days] unless otherwise approved
- AV/malware scanning must occur on inbound files
## **6. MONITORING & LOGGING**  
- Logs must include:
    - Username
    - File name and path
    - Upload/download time
    - IP address
- Logs must be retained for **at least 90 days**
- All FTP activity must be included in **monthly ISMS monitoring reports**

## **7. THIRD-PARTY FTP ACCESS**  
- Must be governed by:
    - NDA and supplier agreement
    - Vendor risk assessment (if handling sensitive data)
- FTP access is revoked immediately after:
    - Project end
    - Contract expiration
    - Policy violation
## **8. VIOLATIONS**
Unapproved use or policy violations may result in:
- Account deactivation
- Investigation by IT Security and ISMS team
- Formal incident logged in line with **[[IT/Procudures/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]**

## **9. REVIEW & MAINTENANCE**
This policy will be reviewed **annually**, or after:
- A file transfer breach or misconfiguration
- Implementation of new FTP/SFTP platforms or processes
- Changes in supplier relationships involving file sharing
## **10. RELATED DOCUMENTS**

| Proces                                              |
| --------------------------------------------------- |
| [[IT/Policies/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]           |
| [[IT/Procudures/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]     |
| [[ISMS-FM-SEC-001 FTP Access Request Request Form\|ISMS-FM-SEC-001 FTP Access Request Request Form]] |
| Data Classification & Handling Guidelines           |
| Vendor Management Policy                            |
| Access Control Register                             |








