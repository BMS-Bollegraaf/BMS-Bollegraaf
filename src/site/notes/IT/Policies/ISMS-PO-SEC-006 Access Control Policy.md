---
{"dg-publish":true,"permalink":"/it/policies/isms-po-sec-006-access-control-policy/","tags":["policy","access","control"],"noteIcon":"default"}
---

 **Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 8.1, 8.2, 8.3, 8.4

---
## **1. PURPOSE**  
To ensure that access to information and information systems is granted on a need-to-know basis and managed securely to protect confidentiality, integrity, and availability.
## **2. SCOPE**
This policy applies to:

- All employees, contractors, consultants, vendors, and third parties
- All systems, applications, networks, cloud services, and physical facilities handling organizational data  
 
## **3. POLICY STATEMENT** 
 ### 3.1 Access Control Principles
- Access must be based on the principles of **least privilege** and **need-to-know**.
- All access to information systems must be **authorized**, **documented**, and **reviewed periodically**
### 3.2 User registration & De-registration
- All users must be uniquely identified.
- User accounts must be created, modified, or disabled based on formal request and approval.
- Accounts must be disabled immediately upon termination or change of role.
### 3.3 Authentication Requirements
- Passwords must comply with the [[IT/Policies/ISMS-PO-SEC-004 Password Policy\|ISMS-PO-SEC-004 Password Policy]].
- Multi-factor authentication (MFA) must be implemented for remote access and privileged accounts.
- Default credentials must be changed before deployment of any system.
### 3.4 Role-Based Access Control (RBAC)
- Access rights must be assigned based on job roles.
- Role definitions must be reviewed at least annually or when roles change.
### 3.5 Privileged Access
- Elevated privileges must be tightly controlled and monitored.
- Admin accounts must not be used for regular day-to-day tasks.
- Activities performed using privileged accounts must be logged and reviewed.
### 3.6 Access Reviews
- User access rights must be reviewed **quarterly** or upon major role changes.
- Inactive accounts should be disabled after [e.g., 90] days of non-use.
### 3.7 Remote Access
- Remote access is only allowed through secure channels (e.g., VPN, MFA).
- Personal devices must meet security standards if allowed.
### 3.8 Physical Access
- Access to server rooms, data centers, and restricted areas must be controlled with key-based or biometric systems.
- Logs of physical access must be retained and reviewed periodically.

## 4. ROLES AND RESPONSIBILITIES

| **Role**        | **Responsibility**                                           |
| --------------- | ------------------------------------------------------------ |
| [[HR/HR\|HR]]          | Notify IT of staff onboarding, offboarding, and role changes |
| [[Functions/IT Engineer\|IT Engineer]] | Provision and revoke access, maintain logsats                |
| Managers        | Approve access requests for their team members               |
| Users           | Use access rights responsibly and report any anomalies       |
| [[Functions/IT Manager\|IT Manager]]  | Oversee access control compliance and audits                 |
## 5. COMPLIANCE
Violation of this policy may lead to disciplinary action, revocation of access, or legal consequences depending on the severity.
## 6. MONITORING AND LOGGING
All access to critical systems must be logged. Logs should be protected from unauthorized modification and retained for [e.g., 12 months].
## 7. REVIEW AND UPDATES
This policy shall be reviewed **annually** or in response to:

- A significant system or organizational change
- An access control incident or audit finding
## 8. RELATED DOCUMENTS  

| Proces                                    |     |
| ----------------------------------------- | --- |
| Information Security Policy (ISMS-PO-001) |     |
| [[IT/Policies/ISMS-PO-SEC-004 Password Policy\|ISMS-PO-SEC-004 Password Policy]]       |     |
| Identity and Access Management Procedure  |     |
| User Access Request Form                  |     |
| Onboarding & Offboarding Checklist        |     |












