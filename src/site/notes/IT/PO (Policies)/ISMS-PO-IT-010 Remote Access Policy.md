---
{"dg-publish":true,"permalink":"/it/po-policies/isms-po-it-010-remote-access-policy/"}
---


**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  


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
To define rules and controls for secure remote access to organizational systems and data, minimizing the risk of unauthorized access, data leakage, and security breaches.
## **2. SCOPE**
This policy applies to:
- All employees, contractors, and third parties accessing systems from outside the organization’s network
- All devices used for remote access (company-owned or BYOD)
- All organizational systems, cloud services, and internal application
 
## **3. POLICY STATEMENTS** 
 
 #### 3.1 Access Authorization
- Remote access must be **explicitly authorized** by management and the system owner.
- Access must follow the **least privilege** principle and be time-bound where applicable.
#### 3.2 Authentication

- All remote access must use **multi-factor authentication (MFA)**.
- Strong password policies must be enforced.
- Default credentials must not be used.
#### 3.3 Secure Connection Methods
- Remote access must only be established through secure channels such as:
    - VPN (Virtual Private Network)
    - Secure cloud access gateways
    - Encrypted remote desktop or VDI platforms
#### 3.4 Device Security
- Devices used for remote access must:
    - Have updated antivirus and endpoint protection
    - Be patched regularly
    - Require local login credentials and screen lock
    - Be enrolled in a mobile device management (MDM) solution if BYOD is allowed

#### 3.5 Data Handling
- Sensitive or classified data must not be stored locally on remote devices unless encrypted and authorized.
- Data must be transmitted securely (TLS/SSL) at all times.
- Cloud storage or file sharing must be limited to approved platforms.

#### 3.6 Monitoring and Logging
- All remote sessions must be logged and monitored for suspicious activity.
- Alerts must be configured for high-risk access attempts or login failures.
#### 3.7 Third-Party Access
- Third-party vendors must:
    - Sign a Non-Disclosure Agreement (NDA)
    - Be granted access only to agreed systems
    - Be monitored during sessions where possible
#### 3.8 Incident Reporting
- Any suspected breach or unusual behavior observed during remote access must be reported immediately to IT/Security.
## **4. ROLES AND RESPONSIBILITIES**

| **Role**          | **Responsibility**                                  |
| ----------------- | --------------------------------------------------- |
| [[Functions/IT Engineer\|IT Engineer]]   | Configure and maintain secure remote access systems |
| Users             | Follow policy and report security issues            |
| [[Functions/System Owners\|System Owners]] | Approve and review remote access requests           |
| [[Functions/ISMS Manager\|ISMS Manager]]  | Oversee compliance and risk monitoring              |
## **5. COMPLIANCE**  
Non-compliance with this policy may result in access revocation, disciplinary action, or contractual consequences for third parties.
## **6. REVIEW**  
This policy must be reviewed **annually**, or:
- Following a remote access-related security incident
- After a significant change in remote access technology or usage
- In response to updated regulatory or business requirements
## **7. RELATED DOCUMENTS**  

| Proces                                             |
| -------------------------------------------------- |
| [[IT/PO (Policies)/ISMS-PO-SEC-002 Acceptable Use Policy\|ISMS-PO-SEC-002 Acceptable Use Policy]]          |
| [[IT/PO (Policies)/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]          |
| [[IT/PO (Policies)/ISMS-PO-IT-006 Vulnerability Management Policy\|ISMS-PO-IT-006 Vulnerability Management Policy]] |
| [[IT/PR (Procedures)/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]    |
| Third-Party Access Agreement Template              |
| Remote Work Guidelines                             |

## **8. CONTROLS**

| Controls                                                        |
| --------------------------------------------------------------- |
| 8.1 – Access control                                            |
| 8.20 – Use of ICT equipment outside the organization’s premises |
| 8.23 – Information security for use of cloud services           |
| 5.10 – Acceptable use of information and assets                 |








