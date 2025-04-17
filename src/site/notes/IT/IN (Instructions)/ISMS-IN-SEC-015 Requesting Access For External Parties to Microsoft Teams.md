---
{"dg-publish":true,"permalink":"/it/in-instructions/isms-in-sec-015-requesting-access-for-external-parties-to-microsoft-teams/","tags":["werkinstructie","MSTeams","access"],"noteIcon":"lightbulb"}
---

 **Effective Date:** 17-04-2025  
**Version:** 1.0  
**Last Updated:** 17-04-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 5.19, 5.20, 5.36, 8.1-8.4

---
## **Table of Contents**  
1. [PURPOSE](#purpose)  
2. [SCOPE](#scope)  
3. [REQUEST PROCEDURE](#request-procedure)  
4. [SECURITY REQUIREMENTS](#securiy-requirements)  
5. [MONITORING & REVIEW](#monitoring-review)  
6. [REVOCATION PROCEDURE](#revocation-procedure)  
7. [ROLES AND RESPONSIBILITIES](#roles-and-responsibilities)  
8. [RELATED DOCUMENTS](#related-documents)  

---
## **1. PURPOSE**  
To define the secure and authorized process for granting **external users** (third parties or guests) access to Microsoft Teams channels, files, and chat functions in alignment with the organization's ISMS controls.
## **2. SCOPE**
This instruction applies to:
- All **external parties** requesting access to Microsoft Teams
- All **employees** or teams sponsoring a guest user
- Any access to Teams content, files, SharePoint libraries, or collaboration channels
## **3. REQUEST PROCEDURE** 

| Step | Action                                                                                                                                                                                                                     |
| ---- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1    | **Employee Sponsor** submits an **External Teams Access Request** via the ITSM tool (e.g., [[IT/Applications/TOPDesk/TOPdesk\|TOPdesk]])                                                                                                                    |
| 2    | Request must include:<br>- External party’s name and company<br>- Email address (Microsoft account required)<br>- Purpose of access<br>- Duration of access (default: 30–90 days)<br>- Name of Team/Channel to be accessed |
| 3    | Request must be **approved** by: <br>- Manager<br>- **Information Owner** of the team                                                                                                                                      |
| 4    | IT grants guest access via Azure AD B2B / Teams admin center with:<br>- Limited permissions (no Team ownership)<br>- Conditional Access or MFA enforcement                                                                 |
| 5    | Sponsor notified, and access logged in **Access Control Register**                                                                                                                                                         |
| 6    | Access is automatically **reviewed or revoked at expiration**                                                                                                                                                              |
## **4. SECURITY REQUIREMENTS**
- Guests must sign an NDA or be covered under a **supplier agreement**
- Teams content classified as **Confidential or Restricted** requires encryption or read-only access
- Guests cannot invite others or create Teams
- Files shared with guests must follow **Data Classification Guidelines**
## **5. MONITORING & REVIEW**
- IT audits external Teams access **monthly**
- Logs include user email, sponsor, Team name, access dates
- Sponsor is responsible for reviewing guest access every 30–90 days
- Inactive external users are automatically removed after 30 days of inactivity
## **6. REVOCATION PROCEDURE**  
- Guest access is revoked:
    - Upon project or engagement end
    - At expiration date (automated)
    - If sponsor or owner reports policy violation
- IT revokes access and logs the action
## **7. ROLES AND RESPONSIBILITIES**  

| Role                | Responsibility                                 |
| ------------------- | ---------------------------------------------- |
| Requesting Employee | Initiate access request and own relationship   |
| Team Owner          | Approve access and monitor content exposure    |
| [[Functions/IT Support\|IT Support]]      | Provision and revoke access securely           |
| [[Functions/ISMS Manager\|ISMS Manager]]    | Audit access and ensure compliance with policy |
## **8. RELATED DOCUMENTS**

| Process                                                      |
| ------------------------------------------------------------ |
| [[IT/PO (Policies)/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]                    |
| [[IT/PR (Procedures)/ISMS-PR-SEC-014 FTP Access Procedure\|ISMS-PR-SEC-014 FTP Access Procedure]] (Similair workflow) |
| [[IT/PR (Procedures)/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]              |
| External Access Request Form                                 |
| Third Party Management Policy                                |
| NDA Template / Supplier Agreement                            |








