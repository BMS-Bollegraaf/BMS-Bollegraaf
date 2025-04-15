---
{"dg-publish":true,"permalink":"/it/po-policies/isms-po-idm-001-active-directory-group-naming-convention-policy/","tags":["policy"]}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]] / [[IT/IT\|IT]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 

---
## **Table of Contents**  
1. [PURPOSE](#purpose)  
2. [SCOPE](#scope)  
3. [NAMING CONVENTION STRUCTURE](#naming-convention-structure)  
4. [ADDITIONAL GUIDELINES](#additional-guidelines)  
5. [COMPLIANCE](#compliance)  
6. [REVIEW](#review)  
7. [RELATED DOCUMENTS](#related-documents)  
8. [CONTROLS](#controle)  

---
## **1. PURPOSE**  
To ensure consistency, clarity, and manageability of Active Directory (AD) group names, this policy defines standardized naming conventions for AD group roles used across the organization.
## **2. SCOPE**
This policy applies to all AD security and distribution groups created, managed, or used within the organization's on-premises or hybrid environments.
 
 ## **3. NAMING CONVENTION STRUCTURE** 
All AD group names **must follow this format**:

[Environment]-[Location]-[Department/Team]-[Function]-[Access Level]-[Suffix]

##### **3.1 Components**

| Component       | Description                                                                  | Example           |     |
| --------------- | ---------------------------------------------------------------------------- | ----------------- | --- |
| Environment     | Target environment (e.g., `PRD`, `TST`, `DEV`, `ACC`)                        | `PRD`             |     |
| Location        | Site code or region (e.g., `APP`, `EMM`, `VEE`)                              | `APP`             |     |
| Department/Team | Department or team the group is associated with                              | `FIN`, `HR`, `IT` |     |
| Function        | Purpose of the group (e.g., `SAP`, `SharePoint`, `VPN`, `Fileshare`)         | `Fileshare`       |     |
| Access Level    | Access type or level (e.g., `R` for Read, `RW` for Read/Write, `F` for Full) | `RW`              |     |
| Suffix          | Type of group: `SG` (Security Group), `DG` (Distribution Group), `M365`      | `SG`              |     |
##### **Example Group Names**

- `PRD-APP-FIN-AX-R-SG`
    
- `DEV-EMM-IT-SharePoint-F-M365`
    
- `TST-VEE-HR-VPN-RW-SG`

## **4. ADDITIONAL GUIDELINES**
- Use **uppercase letters** for consistency.
- Avoid special characters except hyphens (`-`).
- Avoid using user names or personal references in group names.
- Groups for **application-based roles** should prefix the app name clearly (e.g., `PRD-APP-APPNAME-Admin-RW-SG`).
- Prefix **global or cross-location** groups with `GLB-`.

## **5. ROLES AND RESPONSIBILITIES**  

| Role               | Responsibility                                                        |
| ------------------ | --------------------------------------------------------------------- |
| [[Functions/ISMS Manager\|ISMS Manager]]   | is responsible for defining and updating naming standards.            |
| Application Owners | must request group creation following this standard                   |
| [[IT/IT\|IT]]             | are responsible for implementing the convention during group creation |
## **6. EXCEPTIONS**  
Exceptions to this policy must be reviewed and approved by the IAM team and documented in the AD Exceptions Register.
## **7. ENFORCEMENT**  
Non-compliant AD group names may be renamed or removed to maintain directory integrity and audit readiness.






