---
{"dg-publish":true,"permalink":"/it/policies/isms-po-it-011-end-user-device-security-policy/","tags":["security","policy","device"],"noteIcon":"default"}
---

(Also called: Endpoint Security Policy or Workstation Security Policy)

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 5.10, 8.1, 8.7, 8.20

---
## **1. PURPOSE**  
To ensure that all end-user devices accessing organizational data and systems are securely configured, maintained, and used in a way that minimizes the risk of data breaches, malware infections, and unauthorized access.
## **2. SCOPE**
This policy applies to:
- All desktops, laptops, tablets, smartphones, and other devices used to access or store organizational data
- All employees, contractors, and third parties using end-user devices for business purposes
- Both corporate-owned and BYOD (Bring Your Own Device) where permitted
 
## **3. POLICY STATEMENTS** 
#### 3.1 Device Configuration
- Devices must be configured using **secure baseline standards**.
- All unnecessary services, ports, and applications must be disabled or removed.
- Full-disk encryption must be enabled on all laptops and mobile devices
#### 3.2 Authentication & Access
- Devices must require **strong password** or biometric authentication.
- **Auto-lock** must be enabled after a period of inactivity (e.g., 5–10 minutes).
- Use of **admin privileges** on endpoints is restricted to IT personnel.
#### 3.3 Malware Protection
- All endpoints must have approved **anti-malware and endpoint detection & response (EDR)** solutions installed and updated automatically.
#### 3.4 Updates and Patching
- Devices must automatically receive and apply **security patches** for OS and installed software.
- Users must not delay or disable updates
#### 3.5 Data Storage and Backup
- Sensitive information must not be stored locally unless encrypted and approved.
- Backups of workstations (if required) must follow the **[[IT/Policies/ISMS-PO-IT-004 Backup and Recovery Policy\|ISMS-PO-IT-004 Backup and Recovery Policy]]**.
#### 3.6 Remote Access
- End-user devices used for remote access must meet the **[[IT/Policies/ISMS-PO-IT-010 Remote Access Policy\|ISMS-PO-IT-010 Remote Access Policy]]** requirements, including VPN and MFA use.
#### 3.7 Personal Use
- Limited personal use is permitted as long as it does not interfere with work or violate security policies.
- Users must not install unauthorized applications or connect unauthorized peripherals (e.g., USB drives).
#### 3.8 Lost or Stolen Devices
- Any loss or theft of a device must be reported **immediately** to the IT or Security team.
- IT must have the capability to perform **remote wipe** on lost/stolen devices.
#### 3.9 BYOD
- BYOD must be registered and approved by IT.
- MDM (Mobile Device Management) or containerization must be used to enforce security controls.
## **4. ROLES AND RESPONSIBILITIES**

| **Role**                               | **Responsibility**                                 |
| -------------------------------------- | -------------------------------------------------- |
| [[Functions/IT Engineer\|IT Engineer]]                        | Enforce device security controls and monitoring    |
| End Users                              | Comply with device use and protection requirements |
| [[Functions/ISO - Information Security Officer\|ISO - Information Security Officer]] | Conduct risk assessments and monitor compliance    |
| [[HR/HR\|HR]]  / Managers                     | Communicate policy during onboarding/offboarding   |
## **5. COMPLIANCE**  
Non-compliance with this policy may result in:
- Loss of access privileges
- Disciplinary action
- Financial penalties for third-party vendors (if applicable)
## **6. REVIEW**  
This policy must be reviewed **annually**, or after
- Device-related security incidents
- New device platforms are adopted
- Changes in compliance or legal requirements
## **7. RELATED DOCUMENTS**  

| Proces                                             |
| -------------------------------------------------- |
| [[IT/Policies/ISMS-PO-SEC-002 Acceptable Use Policy\|ISMS-PO-SEC-002 Acceptable Use Policy]]          |
| [[IT/Policies/ISMS-PO-IT-010 Remote Access Policy\|ISMS-PO-IT-010 Remote Access Policy]]            |
| [[IT/Policies/ISMS-PO-IT-006 Vulnerability Management Policy\|ISMS-PO-IT-006 Vulnerability Management Policy]] |
| [[IT/Procudures/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]    |
| Endpoint Security Hardening Checklist              |
| BYOD Registration Form                             |





