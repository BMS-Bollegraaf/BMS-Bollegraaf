---
{"dg-publish":true,"permalink":"/it/pr-procedures/isms-pr-sec-012-vault-password-manager-offboarding-procedure/","tags":["procedure"],"noteIcon":"default"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/ISMS Manager\|ISMS Manager]] / [[Functions/Information Security Officer (ISO)\|Information Security Officer (ISO)]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 

---
## **1. PURPOSE**  
To ensure that access to shared or individual password vaults is **promptly and securely revoked** when an employee, contractor, or vendor is offboarded, preventing unauthorized access or credential leakage.
## **2. SCOPE**
This applies to:
- All users with access to shared team vaults or privileged credentials
- All password manager platforms (Keeper)
- All departments and third-party partners
## **3. TRIGGERS FOR OFFBOARDING** 
 - Employee resignation or termination
- Role change or department transfer
- End of vendor or contractor agreement
- Detection of security risk or policy violation
## **4. STEP-BY-STEP OFFBOARDING PROCEDURE**

| Step | Action                                                                                                                              |
| ---- | ----------------------------------------------------------------------------------------------------------------------------------- |
| 1    | **[[HR/HR\|HR]] or Manager notifies [[IT/IT\|IT]]/[[Functions/ISMS Manager\|ISMS Manager]] of departure** with offboarding date                                           |
| 2    | [[Functions/IT Support\|IT Support]] locates user in password manager and disables their account                                                          |
| 3    | If user had access to shared/team vaults:<br>• Vault access is **revoked immediately**<br>• Shared passwords are **rotated** within |
| 4    | Vault admin reviews if any credentials were added/exported by the user                                                              |
| 5    | Log offboarding action in **Vault Access Register**                                                                                 |
| 6    | ISMS Manager confirms access revocation during monthly access review                                                                |
## **5. SPECIAL CASES**  
- **Contractors**: Auto-expiry dates set at time of access grant
- **Admins**: Require second approver for revocation and rotation
- **Privileged Accounts**: Must be rotated immediately, even if inactive
## **6. DOCUMENTATION** 
Each offboarding event must include:
- User name and email
- Vault(s) accessed
- Date of revocation
- Confirmation of password rotation
- Reviewer initials
## **7. ROLES AND RESPONSIBILITIES**  

| Role                  | Resonsibilities                                   |
| --------------------- | ------------------------------------------------- |
| Line Manager / [[HR/HR\|HR]] | Initiates offboarding notification                |
| [[Functions/IT Support\|IT Support]]        | Disables vault access and rotates credentials     |
| Vault Admin / [[IT/IT\|IT]]  | Reviews access and completes logging              |
| [[Functions/ISMS Manager\|ISMS Manager]]      | Audits process and confirms access logs quarterly |
## **8. REVIEW AND COMPLIANCE**
This procedure is reviewed **annually**, or after:
- A major incident or access control audit
- Implementation of a new password manager platform
## **9. RELATED DOCUMENTS**

| Process                                           |
| ------------------------------------------------- |
| [[IT/PO (Policies)/ISMS-PO-SEC-004 Password Policy\|ISMS-PO-SEC-004 Password Policy]]               |
| [[IT/PR (Procedures)/ISMS-PR-SEC-005 Password Management Procedure\|ISMS-PR-SEC-005 Password Management Procedure]] |
| Vault Access Request Form                         |
| Vault Setup Checklist                             |
| Access Control Register                           |
| [[IT/CL (Checklists)/ISMS-CL-HR-003 HR Termination Checklist\|ISMS-CL-HR-003 HR Termination Checklist]]        |








