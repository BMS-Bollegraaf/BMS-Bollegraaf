---
{"dg-publish":true,"permalink":"/it/procudures/isms-pr-sec-005-password-management-procedure/","tags":["password","procedure"],"noteIcon":"default"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/ISO - Information Security Officer\|ISO - Information Security Officer]] / [[Functions/ISMS Manager\|ISMS Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 8.3, 8.4, 5.10, 5.36

---
## **1. PURPOSE**  
To define how passwords are securely created, stored, transmitted, and changed within the organization, minimizing the risk of compromise and unauthorized access.
## **2. SCOPE**
This procedure applies to:
- All systems, platforms, and applications with user authentication
- All employees, contractors, administrators, and third parties
## **3. PASSWORDS CREATION STANDARDS** 
 
| Account Type     | Requirement                                                                             |
| ---------------- | --------------------------------------------------------------------------------------- |
| Standard User    | Minimum 12 Characters, mix op upper/lowercase, numbers, symbols, updates every 180 days |
| Privileged/Admin | Minimum 16 characters, no reuse, updated every 90 days                                  |
| Service Accounts | Managed securely, rotated every 180 days, vault-stored                                  |
| Temporary/Guest  | Expire within 48 hours or after single use                                              |
All passwords must **not include dictionary words, usernames, or obvious patterns**.

## **4. PASSWORD CHANGE REQUIREMENTS**
- **Never write down passwords or store them in plain text**
- Use only **approved password managers** (see **[[IT/Procudures/ISMS-PR-SEC-006 Password Manager Procedure\|ISMS-PR-SEC-006 Password Manager Procedure]]**)
    
- Stored passwords must be
    - Encrypted at rest
    - Accessed only by authorized roles
    - Auditable (access logs retained)
## **5. PASSWORD CHANGE REQUIREMENTS**  
- Change passwords:
    - After suspected compromise
    - Following role change or offboarding
    - When prompted by security controls
- Avoid reusing any of the **last 5 passwords**
## **6. FORGOTTEN PASSWORD & RESET PROCEDURE**  
- Users must request reset via:
    - MFA-enabled self-service portal, **or**
    - IT Helpdesk with identity verification
- IT must verify identity before issuing a reset link or temporary password
- Temporary passwords must:
    - Expire in 24 hours
    - Require immediate change on next login
## **7. PRIVILEGED ACCOUNT PASSWORDS**  
- Must be managed in a **secure vault (Keeper)**
- Rotated:
    - Monthly (high-risk)
    - After usage by multiple admins
    - Immediately after offboarding
- All privileged password access must be logged
## **8. SHARED PASSWORDS (If Absolutely Necessary)**
- Must be stored in a **controlled team vault**
- Access restricted and reviewed quarterly
- Password rotated after access changes or incidents
## **9. ROLES AND RESPONSIBILITIES**

| Role             | Responsibility                                    |
| ---------------- | ------------------------------------------------- |
| Users            | Create, store, and use passwords responsibly      |
| [[Functions/IT Support\|IT Support]]   | Enforce reset process and verify identities       |
| Admins           | Rotate, audit, and protect privileged credentials |
| [[IT/IT\|IT]]           | Monitor for leaked credentials or compromise      |
| [[Functions/ISMS Manager\|ISMS Manager]] | Audit compliance and review procedure annually    |
## **10. REVIEW & COMPLIANCE**
This procedure must be reviewed **annually**, or after:
- Major system or platform changes
- Security incidents involving credential compromise
- Regulatory or audit findings
## **11. RELATED DOCUMENTS**

| Process                                        |
| ---------------------------------------------- |
| [[IT/Policies/ISMS-PO-SEC-004 Password Policy\|ISMS-PO-SEC-004 Password Policy]]            |
| [[IT/Procudures/ISMS-PR-SEC-006 Password Manager Procedure\|ISMS-PR-SEC-006 Password Manager Procedure]] |
| [[IT/Policies/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]      |
| [[IT/Procudures/ISMS-PR-SEC-002 Acceptable Use Procedure\|ISMS-PR-SEC-002 Acceptable Use Procedure]]   |
| Password Rotation Log                          |
| Vault Setup & Access Checklist                 |
| MFA Enrollment Guide                           |




