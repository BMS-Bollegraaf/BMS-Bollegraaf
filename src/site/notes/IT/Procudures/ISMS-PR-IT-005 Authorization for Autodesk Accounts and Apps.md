---
{"dg-publish":true,"permalink":"/it/procudures/isms-pr-it-005-authorization-for-autodesk-accounts-and-apps/","tags":["procedure","access","autodesk"],"noteIcon":"default"}
---

 
**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 30-04-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Classification:** [[Classification/Internal\|Internal]]

---
## **1. PURPOSE**  
To define the secure and compliant procedure for requesting, approving, provisioning, reviewing, and revoking user access to **Autodesk Accounts** and **licensed applications**.
## **2. SCOPE**
This procedure applies to:
- All employees, contractors, and partners requiring access to Autodesk software
- All Autodesk subscriptions managed under [[Companies/Bollegraaf Recycling Solutions\|Bollegraaf Recycling Solutions]] corporate license or resellers
- All desktop, mobile, and cloud-based Autodesk products (AutoCAD, Inventor, Naviworks, BIM 360, etc.)
 
## **3. AUTHORIZATION REQUEST PROCESS** 

| Step | Action                                                                                                                                                                                              |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1    | **Employee/Manager** submits an **Autodesk Access Request Form** (e.g., via TOPdesk or manual form)                                                                                                 |
| 2    | Request must specify:<br>- Software/Product Name (AutoCAD, Revit, etc.)<br>- Intended use (Project, Department, Role)<br>- License type required (Named User / Concurrent / Specialized module)<br> |
| 3    | Request reviewed and **approved by Line Manager** and **IT License Manager**                                                                                                                        |
| 4    | IT Services assigns access via Autodesk Admin Console and licenses user                                                                                                                             |
| 5    | Update **Software Access Register** and notify the user                                                                                                                                             |
## **4. SECURITY  REQUIREMENTS**
- Access must be **linked to corporate email and identity management (e.g., Azure AD)**
- **MFA** must be enforced if Autodesk supports it
- No use of **personal Autodesk accounts** for business activities
- Only **approved devices** may install licensed Autodesk applications
- Storage of drawings and project files must comply with **Data Classification and Backup Policies**
## **5. LICENSE MANAGEMENT CONSOLE**  
- All Autodesk licenses must be tracked in the **License Inventory Register**
- License assignment and usage must be audited **quarterly**
- IT must **reclaim** licenses after:
    - Employee exit or contract end
    - Inactivity > 60 days (unless justified)
## **6. DEPROVISIONING**  
Access is revoked
- During employee offboarding process
- After project or role completion
- If policy violations or overuse of license limits occur  
    Revocation is logged, and Autodesk records updated accordingly
## **7. MONITORING AND REVIEW**  
- IT and ISMS audit Autodesk access logs **annually**
- License usage reports reviewed to prevent non-compliance (over-assignment, idle licenses)
- Non-compliant users subject to incident reporting under [[IT/Procudures/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]
## **8. ROLES AND RESPONSIBILITIES**

| Role             | Responsibility                                           |
| ---------------- | -------------------------------------------------------- |
| Requester        | Submit accurate and justified access requests            |
| Manager          | Approve based on project/business need                   |
| [[Functions/IT Engineer\|IT Engineer]]  | Provision and manage licenses securely                   |
| [[Functions/ISMS Manager\|ISMS Manager]] | Review license compliance and audit access control       |
| License Owner    | Maintain license cost, renewal, and compliance oversight |
## **9. RELATED DOCUMENTS

| [[IT/Policies/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]        |
| ------------------------------------------------ |
| [[IT/Policies/ISMS-PO-IT-015 Software Management Policy\|ISMS-PO-IT-015 Software Management Policy]]    |
| [[IT/Procudures/ISMS-PR-IT-004 IT Asset Management Procedure\|ISMS-PR-IT-004 IT Asset Management Procedure]] |
| Software Access Request Form                     |
| License Inventory Register                       |
| Offboarding Checlist (IT Deprovioning Selection) |







