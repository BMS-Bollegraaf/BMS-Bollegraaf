---
{"dg-publish":true,"permalink":"/it/po-policies/isms-po-sec-009-identity-and-access-management-aim-policy/","tags":["policy","AIM","Identity"],"noteIcon":"default"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name] 
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 8.1, 8.2, 8.3, 8.4, 5.10

---
## **Table of Contents**  
1. [PURPOSE](#purpose)  
2. [SCOPE](#scope)  
3. [POLICY STATEMENTS](#policy-statement)  
4. [ROLES AND RESPONSIBILITIES](#roles-and-responsibilities)  
5. [COMPLIANCE](#compliance)  
6. [REVIEW](#review)  
7. [RELATED DOCUMENTS](#related-documents)  

---
## **1. PURPOSE**  
To ensure that all access to organizational systems and data is authorized, secure, role-based, and auditable by defining standardized procedures for identity creation, management, and removal.
## **2. SCOPE**
 This policy applies to:
- All employees, contractors, and third parties who require access to organizational systems
- All applications, platforms, cloud services, networks, and physical access systems
## **3. POLICY STATEMENTS** 
#### 3.1 User Identity Lifecycle
- All identities must be **uniquely assigned** and recorded in the Identity Register.
- Identity lifecycle stages include:
    - **Provisioning**: Based on formal access request and approval
    - **Modification**: Updated on role change
    - **De-provisioning**: Disabled on exit or inactivity (e.g., after 90 days)
#### 3.2 Authentication Controls
- All accounts must use strong authentication:
    - Passwords per **[[IT/PO (Policies)/ISMS-PO-SEC-004 Password Policy\|ISMS-PO-SEC-004 Password Policy]]**
    - **Multi-factor authentication (MFA)** for remote, admin, and sensitive systems
- Shared accounts are prohibited except for specific use cases (e.g., service accounts) and must be tightly controlled and logged.
#### 3.3 Role-Based Access Control (RBAC)
- Access must be granted based on defined **roles** and **least privilege** principle.
- Each role must have documented access permissions, reviewed annually.
#### 3.4 Access Reviews
- Access rights must be reviewed:
    - **Quarterly** for privileged and high-risk roles
    - **Annually** for general users
- Inactive or orphaned accounts must be flagged and removed.

#### 3.5 Privileged Access

- Admin/root-level access must:
    - Be assigned only with management approval
    - Use named (non-generic) accounts
    - Be logged and monitored (e.g., SIEM, PAM)

#### 3.6 Third-Party Access
- Access for vendors or external parties must:
    - Be time-bound and purpose-specific
    - Require signed agreements (e.g., NDA, DPA)
    - Be revoked immediately after project completion

#### 3.7 Logging and Monitoring
- All authentication attempts, access to sensitive data, and privilege escalations must be logged.
- Anomalies must trigger alerts and be investigated.
## **4. ROLES AND RESPONSIBILITIES**

| **Role**         | **Responsibility**                                              |
| ---------------- | --------------------------------------------------------------- |
| [[IT/IT\|IT]]           | Manage accounts, enforce policy, conduct reviews                |
| [[HR/HR\|HR]]           | Notify IT of onboarding, offboarding, role changes              |
| Department Heads | Approve access for team members and review role appropriateness |
| [[Functions/ISMS Manager\|ISMS Manager]] | Ensure IAM compliance and audit readiness                       |
## **5. COMPLIANCE**  
Non-compliance with this policy may result in disciplinary action, removal of access privileges, or contractual penalties.
## **6. REVIEW**  
This policy must be reviewed **annually** or when:
- A major system or access management change occurs
- New risks or audit findings are identified
- Regulatory or business requirements change
## **7. RELATED DOCUMENTS**  

| Proces                                          |
| ----------------------------------------------- |
| [[IT/PO (Policies)/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]       |
| [[IT/PO (Policies)/ISMS-PO-SEC-004 Password Policy\|ISMS-PO-SEC-004 Password Policy]]             |
| [[IT/PR (Procedures)/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]] |
| User Access Request Form                        |
| Privileged Access Register                      |
| Onboarding and Offboarding Checklists           |








