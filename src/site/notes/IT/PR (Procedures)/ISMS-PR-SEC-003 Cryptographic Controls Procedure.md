---
{"dg-publish":true,"permalink":"/it/pr-procedures/isms-pr-sec-003-cryptographic-controls-procedure/","noteIcon":"lightbulb"}
---

 
**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/Information Security Officer (ISO)\|Information Security Officer (ISO)]] / [[Functions/ISMS Manager\|ISMS Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**Related Documents:**
**ISO/IEC 27001 Controls:** 8.19, 8.20, 5.36
**Tags:** #policy #compliance  #security #dmarc #email

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
To define the proper and secure use of cryptographic methods (e.g., encryption, hashing, digital signatures) to protect the confidentiality, integrity, and authenticity of data.
## **2. SCOPE**
This procedure applies to:
- All systems and applications using encryption
- All users, administrators, and developers handling cryptographic materials
- All environments (on-prem, cloud, hybrid)
## **3. APPROVED CRYPTOGRAPHIC TECHNIQUES** 

| Purpose           | Method / Algorithm | Minimum Standard       |
| ----------------- | ------------------ | ---------------------- |
| Data encryption   | AES-256            | Symmetric              |
| Data in transit   | TLS 1.2 or higher  | HTTPS, VPN             |
| Hashing           | SHA-256            | No MD5 or SHA-1        |
| Digital Signature | RSA 2048 / ECC     | With trusted CA        |
| File encryption   | GPG, 7-Zip AES-256 | For local use          |
| Email encryption  | S/MIME, PGP        | Optional per data type |
## **4. KEY MANAGEMENT PROCEDURE**
#### 4.1 Key Generation
- Keys must be generated using **secure, approved libraries/tools**
- Use hardware security modules (HSM) or encrypted storage for key generation and use
#### 4.2 Key Storage
- Keys must never be stored in plaintext
- Use secure storage mechanisms such as:
    - Password vaults
    - Encrypted key stores
    - Cloud KMS (e.g., AWS KMS, Azure Key Vault)
#### 4.3 Key Distribution
- Keys must only be distributed using secure channels (e.g., SFTP, encrypted email)
- Never share private keys over unsecured communication (email, chat, etc.
#### 4.4 Key Rotation & Expiry
- Symmetric keys: Rotate annually or upon compromise
- Asymmetric keys: Rotate every 2–3 years or per certificate expiration
- All expired or unused keys must be revoked and securely deleted
## **5. USE OF CERTIFICATES**  
- SSL/TLS certificates must be:
    - Issued by a trusted CA
    - Valid (no self-signed certs in production)
    - Monitored for expiration
- Certificate pinning may be implemented for high-risk apps
## **6. ROLES AND RESPONSIBILITIES**

| Role             | Resonsibility                                                       |
| ---------------- | ------------------------------------------------------------------- |
| [[IT/IT\|IT]]           | Approve cryptographic use, review key lifecycle, maintain standards |
| Developers       | Implement approved encryption methods in applications               |
| System Admins    | Securely store and rotate keys                                      |
| End Users        | Use encrypted communication tools responsibly                       |
| [[Functions/ISMS Manager\|ISMS Manager]] | Review compliance and update documentation annually                 |
## **7. INCIDENT HANDLING**  
- Report any compromise or suspected misuse of cryptographic keys immediately
- Keys involved in an incident must be revoked and replaced
- All key lifecycle events (creation, change, deletion) must be logged
## **8. AUDIT AND REVIEW**
- Key usage and access logs must be retained for at least 1 year
- Audit reviews must occur **annually**, or after:
    - Major system changes
    - New cryptographic technologies
    - Security incidents involving encryption
## **9. RELATED DOCUMENTS**

| Process                                           |
| ------------------------------------------------- |
| [[IT/PO (Policies)/ISMS-PO-SEC-004 Password Policy\|ISMS-PO-SEC-004 Password Policy]]               |
| [[IT/PO (Policies)/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]         |
| [[IT/PR (Procedures)/ISMS-PR-SEC-005 Password Management Procedure\|ISMS-PR-SEC-005 Password Management Procedure]] |
| Encryption Inventory Register                     |
| Key Rotation Log                                  |
| Certificate Management Tracker                    |
|                                                   |








