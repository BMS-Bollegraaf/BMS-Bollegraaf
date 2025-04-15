---
{"dg-publish":true,"permalink":"/it/pr-procedures/isms-pr-it-004-it-asset-management-procedure/"}
---

 
**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]] / [[Functions/ISMS Manager\|ISMS Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**Related Documents:**
**ISO/IEC 27001 Controls:** 5.9, 5.10, 5.11, 5.36
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
To define a secure, consistent, and auditable approach to the lifecycle management of IT assets used within the organization.
## **2. SCOPE**
This procedure applies to:
- All **IT assets** (hardware, software, cloud services, and virtual assets)
- Assets issued to **employees, contractors, or third parties**
- Assets in **use, storage, transit, and disposal phases**
## **3. ASSET LIFESTYLE PHASES** 
 
| Phase       | Key Actions                                           |
| ----------- | ----------------------------------------------------- |
| Acquisition | Procure through authorized suppliers; assign Asset ID |
| Deployment  | Label, register, assign owner, update asset register  |
| Operation   | Track usage, status, incidents, updates               |
| Transfer    | Update ownership, physical location, and register     |
| Return      | Recover upon offboarding or reassignment              |
| Disposal    | Wipe securely, decommission, and log disposal action  |
## **4. ASSET CATEGORIES**

| Type            | Examples                                                        |
| --------------- | --------------------------------------------------------------- |
| Hardware        | Laptops, desktops, servers, mobile devices, printers            |
| Software        | OS licenses, productivity suites, antivirus, SaaS subscriptions |
| Virtual         | VMs, cloud storage instances, virtual appliances                |
| Removable Media | USB drives, external HDDs, encrypted portable storage           |
| Network         | Switches, firewalls, routers, wireless AP                       |
## **5. ASSET REGISTER REQUIREMENTS**  
Each asset must be logged with:
- Unique **Asset ID**
- Type & model
- Serial number / MAC address
- Owner (user or department)
- Location
- Classification (e.g., Public / Confidential / Restricted)
- Date of acquisition / assignment
- Status (In Use / Spare / Lost / Retired)
- Notes (e.g., warranty, incidents)
Register is maintained in **[[IT/Applications/TOPDesk/TOPdesk\|TOPdesk]]**.
## **6. ASSET ASSIGEMENT & TRACKING**  
- Use **Asset Assignment Forms** for all issued hardware
- Changes (e.g., reassignments, lost assets) logged within 24 hours
- Use barcode/QR code tags for traceability
- Asset location must be updated if relocated across offices/sites
## **7. AUDITS & REVIEW**  
- Conduct **bi-annual audits** of physical and virtual assets
- Sample-check 10–20% of asset pool
- Report results in the **Asset Audit Log**
- Reconcile with user offboarding logs and disposal records
## **8. SECURITY AND CONTROL REQUIREMENTS**
- Apply **encryption** (BitLocker) to mobile endpoints
- Maintain anti-virus and MDM enrollment
- Enforce **access controls and lock screen policies**
- Disable, retire, or wipe assets within **72 hours** of return or report of loss
## **9. DISPOSAL AND DECOMMISSIONING
- Use approved **secure disposal vendors**
- Remove all company tags and securely wipe data
- Log serial number, disposal method, and date in **Disposal Register**
- Retain disposal certificates (where applicable)
## **10. ROLES AND RESPONSIBILITIES**

| Role                  | Responsibilities                                        |
| --------------------- | ------------------------------------------------------- |
| [[Functions/IT Support\|IT Support]]        | Register, assign, track, and dispose of IT assets       |
| Users                 | Use assets appropriately; report damage, loss, or theft |
| [[Functions/ISMS Manager\|ISMS Manager]]      | Oversee compliance, audits, and risk-based review       |
| [[HR/HR\|HR]] / Line manager | Coordinate asset return during offboarding              |
## **11. REVIEW & NON-COMPLIANCE**
- This procedure is reviewed **annually**, or after major incidents or audit findings
- Missing, stolen, or untracked assets will trigger incident handling per **[[IT/PR (Procedures)/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]**
## **12. RELATED DOCUMENTS**

| Process                                                 |
| ------------------------------------------------------- |
| [[IT/PR (Procedures)/ISMS-PR-IT-003 IT Asset Labeling Procedure\|ISMS-PR-IT-003 IT Asset Labeling Procedure]]          |
| [[IT/PO (Policies)/ISMS-PO-SEC-002 Acceptable Use Policy\|ISMS-PO-SEC-002 Acceptable Use Policy]]               |
| [[IT/PO (Policies)/ISMS-PO-IT-018 Data Retention & Backup Policy\|ISMS-PO-IT-018 Data Retention & Backup Policy]]       |
| Asset Register Template (Excel)                         |
| [[IT/PR (Procedures)/ISMS-PR-SEC-009 Secure Disposal and ReUse Procedure\|ISMS-PR-SEC-009 Secure Disposal and ReUse Procedure]] |
| Asset Assignment & Return Forms                         |
| [[IT/CL (Checklists)/ISMS-CL-HR-003 HR Termination Checklist\|ISMS-CL-HR-003 HR Termination Checklist]]              |






