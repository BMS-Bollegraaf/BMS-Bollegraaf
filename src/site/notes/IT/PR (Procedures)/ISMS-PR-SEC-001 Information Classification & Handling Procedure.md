---
{"dg-publish":true,"permalink":"/it/pr-procedures/isms-pr-sec-001-information-classification-and-handling-procedure/","noteIcon":"default"}
---

 
**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Classification:**
**Related Documents:**
**ISO/IEC 27001 Controls:** 5.12, 5.13, 5.14, 8.10, 8.11
**Tags:** #policy #compliance  #security #dmarc #email

---
## **Table of Contents**  
1. [PURPOSE](#purpose)  
2. [SCOPE](#scope)  
3. [POLICY STATEMENTS](#policy statement)  
4. [ROLES AND RESPONSIBILITIES](#roles-and-responsibilities)  
5. [COMPLIANCE](#dmarc)  
6. [REVIEW](#responsibilities)  
7. [RELATED DOCUMENTS](#compliance)  
8. [CONTROLS](#registrations)  

---
## **1. PURPOSE**  
To ensure that all information processed or stored by the organization is classified, labeled, and handled appropriately to protect it from unauthorized access, disclosure, alteration, or destruction
## **2. SCOPE**
Applies to:
- All employees, contractors, and third parties
- All forms of information (electronic, physical, verbal)
- All systems, services, and storage devices processing organizational information
## **3. INFORMATOIN CLASSIFICATION LEVELS

| Classification | Description                             | Examples                                       |
| -------------- | --------------------------------------- | ---------------------------------------------- |
| Public         | Low sensitivity, can be freely shared   | Published reports, marketing materials         |
| Internal       | Business use only, moderate sensitivity | Internal memos, HR policies                    |
| Confidential   | Restricted to specific teams            | Financial reports, vendor contracts            |
| Restricted     | Critical or regulated data              | PII, credentials, customer data, trade secrets |
## **4. LABELLING REQUIREMENTS**

| **Format**     | **Labeling Requirement**                                               |
| -------------- | ---------------------------------------------------------------------- |
| Emails         | Include classification in subject line (e.g., [CONFIDENTIAL])          |
| Documents      | Header/footer must show classification level                           |
| Physical Media | Must be clearly labeled with classification stickers                   |
| Digital Files  | Use metadata, DLP tags, or filename prefix (e.g., "R_" for Restricted) |
## **5. HANDLING GUIDELINES**  

#### 5.1 Access & Sharing
- Share only with authorized individuals based on need-to-know
- Use **encryption** for sending Confidential/Restricted data
- Never share classified data over public or unencrypted channel.
#### 5.2 Storage
- Store classified data in secure locations:
    - Internal: File shares, M365, SharePoint (with access control)
    - Restricted: Encrypted vaults, protected databases
#### 5.3 Printing & Physical Handling
- Use secure print options for Confidential/Restricted documents
- Store hard copies in locked cabinets
- Shred paper when no longer needed
#### 5.4 Transfer
- Use approved tools (e.g., SFTP, encrypted email) for sensitive data transfers
- Never use unauthorized USB drives or public file-sharing platforms
#### 5.5 Disposal
- Follow the **[[IT/PR (Procedures)/ISMS-PR-SEC-009 Secure Disposal and ReUse Procedure\|ISMS-PR-SEC-009 Secure Disposal and ReUse Procedure]]**
- Wipe digital media using approved tool.
- Shred paper records or dispose via secure bins
## **6. ROLES AND RESPONSIBILITIES**

| Role               | Responsibility                                         |
| ------------------ | ------------------------------------------------------ |
| All Users          | Classify and handle information correctly              |
| Information Owners | Define classification level for assets                 |
| [[IT/IT\|IT]]             | Enforce technical controls (e.g., encryption, backups) |
| [[Functions/ISMS Manager\|ISMS Manager]]   | Monitor compliance and update classification rules     |
## **7. REVIEW**  
This procedure must be reviewed **annually**, or after:
- Changes in legal or regulatory requirements
- A security incident involving information handling
- Introduction of new information types or systems
## **8. RELATED DOCUMENTS**

| Process                                                            |
| ------------------------------------------------------------------ |
| [[IT/PO (Policies)/ISMS-PO-SEC-003 Information Classification and Handling Policy\|ISMS-PO-SEC-003 Information Classification and Handling Policy]] |
| [[IT/PR (Procedures)/ISMS-PR-SEC-009 Secure Disposal and ReUse Procedure\|ISMS-PR-SEC-009 Secure Disposal and ReUse Procedure]]            |
| [[IT/PO (Policies)/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]                          |
| Email and Communication Policy                                     |
| Data Loss Prevention Guidelines                                    |
| Classification Quick Referecence Card                              |
|                                                                    |








