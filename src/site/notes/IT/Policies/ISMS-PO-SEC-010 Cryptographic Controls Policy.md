---
{"dg-publish":true,"permalink":"/it/policies/isms-po-sec-010-cryptographic-controls-policy/","tags":["policy","cryptographic"],"noteIcon":"default"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Managers\|IT Managers]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 8.24,8,25, 5.10, 5.23

---
## **1. PURPOSE**  
To establish requirements for the secure and consistent use of cryptographic controls to protect the confidentiality, integrity, and authenticity of sensitive and classified data.
## **2. SCOPE**
This policy applies to:
- All information classified as **Confidential** or above
- All systems, devices, applications, and services (on-prem or cloud) that store, process, or transmit such information
- All users, including employees, contractors, and third parties who handle sensitive data
 
## **3. POLICY STATEMENTS** 
#### 3.1 Use of Cryptography
- Cryptographic methods must be used to protect:
    - Data **at rest** (e.g., databases, laptops, backups)  
    - Data **in transit** (e.g., VPNs, emails, APIs)
    - Authentication and digital signatures
- Only approved algorithms and protocols (e.g., AES-256, RSA 2048, TLS 1.2/1.3) may be used.
#### 3.2 Key Management
- Cryptographic keys must be:
    - Generated using strong, standards-based methods
    - Stored securely in encrypted formats or **Hardware Security Modules (HSMs)**
    - Rotated regularly and upon personnel or system changes
    - Revoked immediately if compromise is suspected
#### 3.3 Certificate Management
- Digital certificates must be:
    - Issued by trusted Certificate Authorities (CAs)
    - Monitored and renewed prior to expiration
    - Tracked in a **Certificate Inventory Register**
#### 3.4 Cloud and SaaS Encryption
- Cloud services must:
    - Support encryption of data in transit and at rest
    - Allow customer-side key control or integration with enterprise key vaults (e.g., AWS KMS, Azure Key Vault)
#### 3.5 Storage and Backup
- Encrypted data must not be decrypted for storage in unprotected environments.
- Backups must be encrypted and stored separately from encryption keys.
#### 3.6 Roles and Access
- Access to encryption tools, keys, and certificates must be restricted and logged.
- Role-based access must be enforced for key management platforms.
#### 3.7 Incident Response
- Suspected cryptographic failures (e.g., key exposure, weak encryption use) must be reported immediately and managed under the  **[[IT/Procudures/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]**.
## **4. ROLES AND RESPONSIBILITIES**

| **Role**                               | **Responsibility**                                   |
| -------------------------------------- | ---------------------------------------------------- |
| [[Functions/ISO - Information Security Officer\|ISO - Information Security Officer]] | Define and enforce cryptographic standards           |
| [[Functions/IT Engineer\|IT Engineer]]                        | Implement and maintain encryption systems            |
| Developers                             | Apply secure cryptographic practices in applications |
| Users                                  | Protect encrypted data and report anomalies          |
| Key Custodians                         | Manage key lifecycle and access permissions          |
## **5. COMPLIANCE**  
Failure to follow this policy may result in data breaches, compliance violations, and disciplinary or legal action.
## **6. REVIEW**  
This policy shall be reviewed **annually**, or after:
- Cryptographic incidents
- Regulatory or industry standards updates (e.g., NIST, ISO)
- Changes in tools or infrastructure
## **7. RELATED DOCUMENTS**  

| Proces                                                             |
| ------------------------------------------------------------------ |
| [[IT/Policies/ISMS-PO-SEC-003 Information Classification and Handling Policy\|ISMS-PO-SEC-003 Information Classification and Handling Policy]] |
| [[IT/Policies/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]                          |
| Secure Development Policy                                          |
| [[IT/Procudures/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]                    |
| Key Inventory Register                                             |
| Certificate Monitoring Schedule                                    |








