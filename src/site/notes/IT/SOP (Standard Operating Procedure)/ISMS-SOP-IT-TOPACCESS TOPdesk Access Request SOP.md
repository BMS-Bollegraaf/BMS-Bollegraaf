---
{"dg-publish":true,"permalink":"/it/sop-standard-operating-procedure/isms-sop-it-topaccess-to-pdesk-access-request-sop/","tags":["topdesk","SOP"],"noteIcon":"lightbulb"}
---

 
**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]] / [[Functions/ISMS Manager\|ISMS Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**Related Documents:**
**ISO/IEC 27001 Controls:** 8.1, 8.2, 8.3, 8.4, 5.36

---
## **Table of Contents**  
1. [PURPOSE](#purpose)  
2. [SCOPE](#scope)  
3. [ACCESS LEVELS IN TOPDESK](#policy statement)  
4. [ROLES AND RESPONSIBILITIES](#roles-and-responsibilities)  
5. [ROLE MODIFICATION PROCEDURE](#dmarc)  
6. [ACCESS REVOCATION PROCEDURE](#responsibilities)  
7. [MONITORING & REVIEW](#compliance)  
8. [ROLE AND RESPONSIBILITIES](#registrations)
9. [RELATED DOCUMENTS](9)

---
## **1. PURPOSE**  
To establish a secure and auditable procedure for requesting, approving, assigning, modifying, and revoking access to the **TOPdesk platform** in compliance with organizational access control policies. 
## **2. SCOPE**
This SOP applies to:
- All employees, contractors, and third parties requiring access to TOPdesk
- All user roles including Requesters, Operators, Specialists, and Admins
- New accounts, role changes, and deactivations
## **3. ACCESS LEVELS IN TOPDESK** 

| Role          | Description                                      |
| ------------- | ------------------------------------------------ |
| Requester     | Submit service/incident/change requests          |
| Operator      | Handle tickets within assigned categories        |
| Specialist    | Manage workflows, templates, categories          |
| Administrator | Full access to configuration, roles, permissions |
## **4. ROLES AND RESPONSIBILITIES**

#### Step 1: **Submission**
- Complete the **TOPdesk Access Request Form** (manual or online)
- Form must include:
    - User’s full name and department
    - Requested role and justification
    - Manager’s name and approval
    - Planned start date
#### Step 2: **Approval**
- Line Manager and System Owner must approve request
- [[Functions/ISMS Manager\|ISMS Manager]] or [[Functions/IT Manager\|IT Manager]] must approve **Specialist/Admin** roles
#### Step 3: **Provisioning**
- IT Admin:
    - Creates account or modifies role in TOPdesk
    - Enforces **MFA and password policy**
    - Assigns user to appropriate categories or groups
- Provisioning logged in the **Access Control Register**
#### Step 4: **Notification**
- User receives access confirmation and link to **[[IT/PO (Policies)/ISMS-PO-SEC-002 Acceptable Use Policy\|ISMS-PO-SEC-002 Acceptable Use Policy]]**
- For elevated roles: short briefing or SOP review is required
## **5. ROLE MODIFICATION PROCEDURE**  
- Triggered by:
    - Internal transfers
    - Change of responsibilities
    - Request from Manager or ISMS audit
- Follows same approval and update process as above
## **6. ACCESS REVOCATION PROCEDURE**  

| Triger               | Action                                             |
| -------------------- | -------------------------------------------------- |
| Offboarding          | Disable access within 24 hours of last working day |
| Contract end         | Auto-expire date set at creation                   |
| Violation or abuse   | Immediate disablement; investigation by ISMS       |
| Inactivity > 90 days | Notify user; disable if no response in 7 days      |
All revocations are logged and reviewed quarterly
## **7. MONITORING & REVIEW**  
- Review access logs and usage **monthly**
- Conduct **quarterly access rights audits**
- Admin accounts are reviewed **semi-annually** for necessity and least privilege
## **8. ROLE AND RESPONSIBILITIES**

| Role             | Responsibility                              |
| ---------------- | ------------------------------------------- |
| Requester        | Submits access form accurately              |
| Manager          | Validates need and authorizes request       |
| [[Functions/IT Engineer\|IT Engineer]]  | Grants/revokes access, updates logs         |
| [[Functions/ISMS Manager\|ISMS Manager]] | Approves high-risk roles, audits compliance |
## **9. RELATED DOCUMENTS**

| Process                                                      |
| ------------------------------------------------------------ |
| [[IT/PO (Policies)/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]                    |
| [[IT/PR (Procedures)/ISMS-PR-IT-002 Change Management Procedure\|ISMS-PR-IT-002 Change Management Procedure]]               |
| [[IT/SOP (Standard Operating Procedure)/ISMS-SOP-IT-SECWR Secure Workstation & Remote Access SOP\|ISMS-SOP-IT-SECWR Secure Workstation & Remote Access SOP]] |
| [[IT/PO (Policies)/ISMS-PO-SEC-002 Acceptable Use Policy\|ISMS-PO-SEC-002 Acceptable Use Policy]]                    |
| TOPdesk Access Request Form (fillable PDF)                   |
| Access Control Register (Excel)                              |
| Role Matrix & Description Sheet                              |







