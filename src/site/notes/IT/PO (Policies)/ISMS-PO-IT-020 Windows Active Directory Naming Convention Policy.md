---
{"dg-publish":true,"permalink":"/it/po-policies/isms-po-it-020-windows-active-directory-naming-convention-policy/","tags":["policy","reading","convention"],"noteIcon":"default"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]] [[Functions/IT Engineer\|IT Engineer]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 8.1, 8.2, 8.4, 5.36

---
## **1. PURPOSE**  
To define standardized naming conventions for all Active Directory (AD) objects to ensure clarity, consistency, ease of administration, and security compliance across the IT infrastructure.
## **2. SCOPE**
Applies to:
- All organizational units (OUs), users, groups, computers, and service accounts in Active Directory
- All environments (production, test/dev, DR) managed by IT
## **3. NAMING CONVENTOIN RULES** 

 #### 3.1 General Guidelines
- Use only **alphanumeric characters** and hyphens
- **Avoid special characters** and spaces
- Use **lowercase or PascalCase**, based on object type
- Reflect purpose, location, and/or role clearly
- Prefix or suffix objects with function and environment (e.g., `srv-`, `grp-`, `-prd`, `-tst`)
## **4. NAMING PATTERNS BY OBJECT TYPE**

#### 4.1 User Accounts

| Format                          | Description                                            |
| ------------------------------- | ------------------------------------------------------ |
| `firstnameletter.lastname`      | Standard user (e.g., `j.doe`)                          |
| `firstname.l.lastname`          | If duplicate exists (e.g., `j.l.doe`)                  |
| `svc_[system/function]`         | Service accounts (e.g., `svc_sqlbackup`)               |
| `ext_[company/initials]_[user]` | External vendors or contractors (e.g., `ext_xyz_john`) |
#### 4.2 Security Groups

| Format                                                                  | Description                |
| ----------------------------------------------------------------------- | -------------------------- |
| `grp_[location]_[role]_[type]`                                          | e.g., `grp_nyc_finance_rw` |
| `app_[appname]_[env]_[perm]`                                            | e.g., `app_sap_prd_admin`  |
| Type suffixes: `_ro` = read-only, `_rw` = read-write, `_admin` = admins |                            |
#### 4.3 Distribution Groups

|Format|Example|
|---|---|
|`dist_[department]_[location]`|`dist_marketing_london`|
|`dist_all_[region]`|`dist_all_eu`|
#### 4.4 Computers (Workstations)

| Format                      | Description    |
| --------------------------- | -------------- |
| `ws-[location]-[assetID]`   | `ws-app-43982` |
| `lpt-[dept]-[userinitials]` | `lpt-hr-jd`    |
#### 4.5 Servers

|Format|Description|
|---|---|
|`srv-[role]-[location]-[env]`|`srv-db-paris-prd`, `srv-web-ams-tst`|

#### 4.6 Organizational Units (OUs)

| Format                                   | Description            |
| ---------------------------------------- | ---------------------- |
| `OU=[Function]_[Location]_[Environment]` | `OU=HR_Appingedam_PRD` |
|                                          | `OU=Finance_Emmen_PRD` |
## **5. ENVIRONMENT SUFFIXES**  
| Code  | Meaning           |
| ----- | ----------------- |
| `prd` | Production        |
| `tst` | Testing           |
| `dev` | Development       |
| `dr`  | Disaster Recovery |
| `lab` | Lab / Training    |
| `acc` | Acceptance        |
## **6. CHANGE CONTROL**  
- Naming exceptions must be approved by [[Functions/IT Manager\|IT Manager]] or [[Functions/ISMS Manager\|ISMS Manager]]
- All changes must follow the **[[IT/PR (Procedures)/ISMS-PR-IT-002 Change Management Procedure\|ISMS-PR-IT-002 Change Management Procedure]]**
## **7. ROLES AND RESONSIBILITIES**  

| Role              | Responsibility                                         |
| ----------------- | ------------------------------------------------------ |
| [[Functions/IT Engineer\|IT Engineer]]   | Apply and enforce naming during object creation        |
| [[Functions/System Owners\|System Owners]] | Request names in line with this policy                 |
| [[Functions/ISMS Manager\|ISMS Manager]]  | Ensure compliance with ISMS naming and audit standards |
## **8. AUDIT & REVIEW**
- Perform quarterly audits of AD objects for naming consistency
- Report deviations and remediate within **5 business days**
- Review this policy **annually**, or after system changes
## **9. RELATED DOCUMENTS**

| Process                                                      |     |
| ------------------------------------------------------------ | --- |
| [[IT/PO (Policies)/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]                    |     |
| ISMS-PR-IT-002: Change Management Procedure                  |     |
| [[IT/SOP (Standard Operating Procedure)/ISMS-SOP-IT-SECWR Secure Workstation & Remote Access SOP\|ISMS-SOP-IT-SECWR Secure Workstation & Remote Access SOP]] |     |
| Active Directory Object Lifecycle Procedure                  |     |
| AD Audit & Cleanup Tracker                                   |     |




