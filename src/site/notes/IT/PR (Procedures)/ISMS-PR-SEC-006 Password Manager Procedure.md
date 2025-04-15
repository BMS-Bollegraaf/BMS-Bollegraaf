---
{"dg-publish":true,"permalink":"/it/pr-procedures/isms-pr-sec-006-password-manager-procedure/","tags":["procedure","password"]}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/ISMS Manager\|ISMS Manager]] / [[Functions/Information Security Officer (ISO)\|Information Security Officer (ISO)]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 8.3, 8.4, 5.10, 5.36

---
## **1. PURPOSE**  
To define secure procedures for the use of password management tools within the organization, ensuring that passwords are **created, stored, shared, and accessed** in a secure, auditable, and ISO-compliant manner
## **2. SCOPE**
This procedure applies to:
- All employees and contractors managing **corporate credentials**
- All systems, services, cloud platforms, and applications
- Both **individual and shared account management** scenarios
 
 ## **3. APPROVED PASSWORD MANAGERS**
* Keeper
 
 Cloud-based solutions must be:
- Hosted in secure, compliant environments (e.g., ISO 27001, SOC 2)
- Enforced with **multi-factor authentication (MFA)**
- Capable of **team vaults, audit logs**, and **policy control**
## **4. PASSWORD VAULT SETUP**

|Step|Action|
|---|---|
|1|IT Security sets up the master vault with policies|
|2|Users are onboarded via company email and required to enable MFA|
|3|Team vaults are created per department or function (e.g., DevOps, HR, Finance)|
|4|Role-based permissions applied (read-only, admin, editor)|
|5|Vault access is audited quarterly or upon role changes|
## **5. PASSWORD CREATION STANDARDS**
- Passwords must be **auto-generated** by the password manager
- Minimum: 16+ characters, mix of upper/lowercase, numbers, symbols
- **Never reuse passwords** across systems
- Use of **passphrases** (e.g., correct-horse-battery-staple) for master passwords is encouraged
## **6. SECURE SHARING**  
- Credentials must **never be shared via email, chat, or documents**
- Use the password manager’s **secure sharing features**
- Shared credentials must be stored in **team vaults** with access logging
- When a team member leaves or changes role:
    - Access must be **revoked immediately**
    - Passwords must be **rotated if shared**
## **7. MONITORING & COMPLIANCE**  
- Access logs and password reuse warnings must be reviewed monthly
- Policy violations (e.g., weak or duplicated passwords) are flagged and reported
- Vaults are subject to **internal audits and offboarding reviews**
## **8. ROLES AND RESPONSIBILITIES**

| Role             | Responsibilities                                         |
| ---------------- | -------------------------------------------------------- |
| Users            | Use password manager for all company-related credentials |
| Managers         | Approve vault access, review role changes                |
| [[IT/IT\|IT]]           | Configure policies, monitor usage, respond to issues     |
| [[Functions/ISMS Manager\|ISMS Manager]] | Ensure compliance and document reviews                   |
## **9. OFFBOARDING PROCESS**
Upon employee departure:
- All vault access is disabled immediately
- Shared credentials are rotated within 24 hours
- Relevant access logs are archived
## **10. REVIEW AND UPDATES**
This procedure is reviewed **annually**, or:
- Following a credential compromise
- After a password manager change or upgrade
- Based on audit results or policy violations
## **11. RELATED DOCUMENTS**

| [[IT/PO (Policies)/ISMS-PO-SEC-004 Password Policy\|ISMS-PO-SEC-004 Password Policy]]          |
| -------------------------------------------- |
| [[IT/PO (Policies)/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]    |
| [[IT/PR (Procedures)/ISMS-PR-SEC-002 Acceptable Use Procedure\|ISMS-PR-SEC-002 Acceptable Use Procedure]] |
| Offboarding Checklist                        |
| Vault Access Request Form                    |
| Password Rotation Log                        |








