---
{"dg-publish":true,"permalink":"/it/po-policies/isms-po-sec-012-secure-printing-policy/","tags":["policy","printing"],"noteIcon":"default"}
---

 **Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]] [[Functions/Information Security Officer (ISO)\|Information Security Officer (ISO)]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 5.10, 5.12, 7.3, 8.11, 8.30

---
## **1. PURPOSE**  
To define controls and best practices for protecting information during the printing, handling, and disposal of physical documents to reduce the risk of data leakage.
## **2. SCOPE**
This policy applies to:
- All employees, contractors, and third parties using organizational printing resources
- All multifunction printers, copiers, fax machines, and print queues
- All physical documents that contain business-related, confidential, or personal information
## **3. SECURE PRINTING CONTROLS**
#### 3.1 Print Release (Pull Printing)
- All printers must support **PIN**, **badge swipe**, or **secure release** mechanisms
- Documents are held in queue until released by the authorized user
- Default printing behavior must be **"secure release"**, not auto-print
#### 3.2 Document Classification Awareness
- Users must only print documents that comply with the **[[IT/PO (Policies)/ISMS-PO-SEC-003 Information Classification and Handling Policy\|ISMS-PO-SEC-003 Information Classification and Handling Policy]]** 
- **Restricted** and **Confidential** documents should be printed only when necessary and retrieved immediately
#### 3.3 Printer Location and Security
- Printers handling sensitive output must be:
    - Located in access-controlled or monitored areas
    - Not shared with public or visitor zones
- Unauthorized access to print trays and maintenance ports must be restricted
#### 3.4 Duplex and Black & White Defaults
- Default print settings should be:
    - **Black & white** (unless color required)
    - **Duplex** (double-sided) to reduce paper use and exposure
#### 3.5 Disposal of Printed Material
- Printed documents containing sensitive or classified information must be:
    - Disposed of using **locked shredding bins**
    - Not discarded in open waste bins or recycling containers
#### 3.6 Fax and Scanned Output Controls
- Fax or scan-to-email must be used only with approved, secure email addresses
- Received faxed documents should be removed immediately
- Scanned files must not be stored on printer hard drives longer than necessary
 
 ## **4. USER RESPONSIBILITIES**
- Check printer settings and recipient email addresses before sending
- Retrieve print jobs **immediately after release**
- Report any printer misbehavior or uncollected output to IT
- Never leave printed materials unattended or abandoned in public areas
## **5. IT RESPONSIBILITIES**  
- Configure and enforce secure printing defaults
- Monitor printer logs for unauthorized use
- Regularly purge print queues and cached files
- Maintain printer firmware and security patches
## **6. COMPLIANCE  
Violation of this policy may result in:
- Disciplinary action
- Access restrictions
- Audit findings or regulatory non-compliance (e.g., GDPR Article 32)
## **7. REVIEW**  
This policy must be reviewed **annually**, or when:
- New printing technologies are introduced
- A related incident or breach occurs
- New data protection laws are implemented
## **8. RELATED DOCUMENTS**

| Process                                                            |
| ------------------------------------------------------------------ |
| [[IT/PO (Policies)/ISMS-PO-SEC-003 Information Classification and Handling Policy\|ISMS-PO-SEC-003 Information Classification and Handling Policy]] |
| [[IT/PR (Procedures)/ISMS-PR-SEC-009 Secure Disposal and ReUse Procedure\|ISMS-PR-SEC-009 Secure Disposal and ReUse Procedure]]            |
| [[IT/PO (Policies)/ISMS-PO-SEC-011 Email and Communication Policy\|ISMS-PO-SEC-011 Email and Communication Policy]]                 |
| [[IT/PO (Policies)/ISMS-PO-SEC-002 Acceptable Use Policy\|ISMS-PO-SEC-002 Acceptable Use Policy]]                          |
| [[IT/Registers/Printer Asset Register\|Printer Asset Register]]                                         |
| Visitor Printing SOP (NOT applicable)                              |
| [[IT/IN (Instructions)/ISMS-IN-SEC-012 Secure Printing\|ISMS-IN-SEC-012 Secure Printing]]                    |








