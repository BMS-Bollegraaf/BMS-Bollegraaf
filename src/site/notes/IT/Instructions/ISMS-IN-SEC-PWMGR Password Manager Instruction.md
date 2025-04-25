---
{"dg-publish":true,"permalink":"/it/instructions/isms-in-sec-pwmgr-password-manager-instruction/","tags":["Instruction","password"],"noteIcon":"default"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]] / [[Functions/ISMS Manager\|ISMS Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**Related Documents:**
**ISO/IEC 27001 Controls:** 8.3,8.4, 5.10

---
## **1. PURPOSE**  
To ensure all users securely store and manage passwords by using an approved password manager in accordance with the organization's information security policies.
## **2. SCOPE**
This instruction applies to:
- All employees, contractors, and administrators
- All business systems, cloud platforms, and services with user authentication
- Individual and shared credentials
## **3. APPROVED PASSWORD MANAGER** 
 Only the following solutions may be used:

- **Keeper**
- Installed and configured by **IT Security** with enforced policies and access logging
- Integrated with **MFA** and **enterprise SSO** where applicable
## **4. USER RESPONSIBILITIES**
- Use the password manager for all **work-related accounts**
- Do not store passwords in spreadsheets, browsers, email, or notes
- Use **auto-generated strong passwords** (minimum 16 characters)
- Categorize entries (e.g., personal, team, admin) appropriately
- Never share credentials outside the vault — use “share” feature with read-only access if needed
- Do not store personal credentials in the corporate vault
## **5. SHARED CREDENTIAL MANAGEMENT**  
- Shared accounts must be stored in **team vaults** with role-based access
- Use folder naming conventions (e.g., `finance_admin`, `devops_tools`)
- Review access rights quarterly or upon team member changes
- Rotate shared passwords after:
    - Offboarding of a user
    - Role transfer
    - Account compromise
## **6. SECURITY MEASURES**  
- Master password must follow the **Password Policy** and never be reused
- Enable MFA (authenticator app or hardware key)
- Set auto-lock timeout to 5 minutes or less
- Never export vaults unless specifically authorized for migration
## **7. OFFBOARDING & DEPROVISIONING**  
- Revoke vault access upon termination or exit
- Rotate shared credentials the user had access to
- Archive and securely delete user vault content if required
## **8. AUDIT & MONITORING**
IT Security will:
- Monitor vault usage and policy compliance
- Review logs for suspicious or unauthorized actions
- Ensure data recovery is configured and tested
## **9. NON-COMPLIANCE**
Failure to follow this instruction may result in:
- Disciplinary action
- Revocation of system access
- Incident reporting as per **[[IT/PR (Procedures)/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]**
## **10. RELATED DOCUMENTS**

| Process                                           |
| ------------------------------------------------- |
| [[IT/PO (Policies)/ISMS-PO-SEC-004 Password Policy\|ISMS-PO-SEC-004 Password Policy]]               |
| [[IT/PR (Procedures)/ISMS-PR-SEC-005 Password Management Procedure\|ISMS-PR-SEC-005 Password Management Procedure]] |
| [[IT/PR (Procedures)/ISMS-PR-SEC-006 Password Manager Procedure\|ISMS-PR-SEC-006 Password Manager Procedure]]    |
| Vault Setup Checklist                             |
| Master Password Guidelines                        |
| Password Rotation Log                             |







