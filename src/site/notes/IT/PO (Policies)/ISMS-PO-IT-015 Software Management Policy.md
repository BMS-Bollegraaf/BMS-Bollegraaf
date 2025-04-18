---
{"dg-publish":true,"permalink":"/it/po-policies/isms-po-it-015-software-management-policy/","noteIcon":"default"}
---

 **Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]

**ISO/IEC 27001 Controls:** 5.9, 5.10, 8.9, 8.28, 8.8


---
## **Table of Contents**  
1. [PURPOSE](#purpose)  
2. [SCOPE](#scope)  
3. [POLICY STATEMENTS](#policy statement)  
4. [ROLES AND RESPONSIBILITIES](#roles-and-responsibilities)  
5. [COMPLIANCE](#dmarc)  
6. [REVIEW](#responsibilities)  
7. [RELATED DOCUMENTS](#compliance)  

---
## **1. PURPOSE**  
To ensure that all software used within the organization is secure, licensed, approved, and properly managed throughout its lifecycle to reduce risk and ensure compliance.
## **2. SCOPE**
This policy applies to:
- All software used on organizational systems (desktops, laptops, servers, mobile devices)
- All employees, contractors, and third parties
- Operating systems, applications, cloud-based tools, and development software

 ## **3. POLICY STATEMENTS** 
 
 #### 3.1 Software Acquisition and Approval
- Only software that is **approved, licensed, and aligned with business needs** may be used.
- All software acquisitions must be requested through IT or Procurement.
- **Unapproved downloads or installations are strictly prohibited**.

#### 3.2 Licensing and Compliance
- All software must be properly licensed.
- License documentation must be maintained in a **Software License Inventory**.
- The organization must not use pirated, cracked, or unlicensed software

#### 3.3 Installation and Configuration
- Only **authorized IT personnel** may install software on organizational devices.
- Default configurations must be reviewed and hardened before deployment.
- Configuration changes must follow the **[[IT/PO (Policies)/ISMS-PO-IT-002 Change Management Policy\|ISMS-PO-IT-002 Change Management Policy]]**.
#### 3.4 Software Inventory

- All installed software must be recorded in the **Software Inventory Register**, including:
    - Software name and version
    - License type and expiry
    - Device/host where installed
    - Owner or responsible party
#### 3.5 Updates and Patch Management
- All software must be updated regularly to address bugs and security vulnerabilities.
- Critical security patches must be applied within defined timeframes:
    - **Critical**: within 7 days
    - **High**: within 14 days
    - **Medium/Low**: during scheduled maintenance
#### 3.6 Unauthorized Software and Shadow IT
- Users must not install personal or unapproved software.
- IT must regularly scan systems for unauthorized software.
- Detected shadow IT must be investigated and removed unless approved retroactively
#### 3.7 Cloud and SaaS Applications
- Use of cloud apps must be authorized and recorded in a **Cloud Services Inventory**.
- Data processed by SaaS platforms must comply with **data classification** and **privacy requirements**.
#### 3.8 Secure Development Software
- Developers must use secure and approved development tools.
- Open-source components must be vetted for vulnerabilities and license compatibility.
- Repositories and build pipelines must follow the **Secure Development Policy**.
## **4. ROLES AND RESPONSIBILITIES**

| **Role**         | **Responsibility**                                 |
| ---------------- | -------------------------------------------------- |
| [[Functions/IT Manager\|IT Manager]]   | Maintain software inventory and enforce controls   |
| [[Procurement/Procurement\|Procurement]]  | Validate license agreements and purchase approvals |
| End Users        | Use software responsibly and report issues         |
| [[Functions/ISMS Manager\|ISMS Manager]] | Ensure compliance and alignment with ISO/IEC 27001 |
## **5. COMPLIANCE**  
Violations of this policy (e.g., using pirated or unapproved software) may result in:
- Disciplinary action
- Legal penalties
- Revocation of system access
## **6. REVIEW**  
This policy must be reviewed **annually**, or after:
- Major software changes or upgrades
- Audit findings or license noncompliance
- Regulatory or business requirement updates
## **7. RELATED DOCUMENTS**  

| Proces                                      |
| ------------------------------------------- |
| [[IT/PO (Policies)/ISMS-PO-SEC-002 Acceptable Use Policy\|ISMS-PO-SEC-002 Acceptable Use Policy]]   |
| [[IT/PO (Policies)/ISMS-PO-IT-002 Change Management Policy\|ISMS-PO-IT-002 Change Management Policy]] |
| [[IT/PO (Policies)/ISMS-PO-IT-005 Patch Management Policy\|ISMS-PO-IT-005 Patch Management Policy]]   |
| Software License Inventory                  |
| Cloud Services Register                     |
| Secure Coding & DevOps Guidelines           |









