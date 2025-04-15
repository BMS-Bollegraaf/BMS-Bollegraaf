---
{"dg-publish":true,"permalink":"/it/pr-procedures/isms-pr-it-003-it-asset-labeling-procedure/"}
---

 
**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]] / [[Functions/ISMS Manager\|ISMS Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**Related Documents:**
**ISO/IEC 27001 Controls:** 5.9, 5.10, 5.11, 8.10, 5.36
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
To establish a standardized process for **labeling and identifying IT assets** (e.g., laptops, servers, removable media) to enable tracking, assignment, recovery, and compliance with information security and audit requirements.
## **2. SCOPE**
Applies to:
- All physical and virtual IT assets (laptops, desktops, servers, printers, mobile devices, removable media)
- IT-owned hardware used by employees, contractors, or vendors
- On-premise and remote assets issued or tracked by the organization
## **3. LABELING STANDARDS** 

| Asset Type            | Label Content                                         |
| --------------------- | ----------------------------------------------------- |
| Laptops / Desktops    | Asset ID, company name, barcode/QR code               |
| Servers / Racks       | Asset ID, hostname, data center ID                    |
| Mobile Devices        | Asset ID, user initials, department (if space allows) |
| USB / External Drives | Asset ID, encryption status                           |
| Network Devices       | Asset ID, rack location (if applicable)               |
| Virtual Assets (VMs)  | Logical Asset ID in CMDB + VM name tag                |
## **4. ASSET ID FORMAT**

Format: `ASSET-[TypeCode]-[LocationCode]-[SequentialNumber]`

**Examples:**
- `ASSET-LTP-APP-00321` – Laptop assigned in Appingedam
- `ASSET-SRV-EMM-00110` – Server in Emmen data center
- `ASSET-USB-REM-00245` – Removable encrypted USB

**Type Codes:**
- `LTA` = Laptop
- `DTP` = Desktop
- `SRV` = Server
- `MOB` = Mobile
- `USB` = External media
- `PRN` = Printer
- `VM` = Virtual Machine
## **5. LABELING PROCEDURE**  

#### Step 1: **Asset Registration**
- Asset details recorded in the **Asset [[IT/Applications/TOPDesk/TOPdesk\|TOPdesk]] Register** before issuance
- Includes model, serial number, assigned user, location, classificatio

#### Step 2: **Label Creation**
- Generate unique Asset ID
- Print using tamper-evident, weather-resistant labels (barcode/QR optional)
#### Step 3: **Physical Label Placement**
- Laptops: Top Right Cover
- Desktops: front or side panel
- Servers: rack faceplate
- USBs: adhesive tag or pre-printed shell
- Mobile devices: rear casing
#### Step 4: **System Tagging**
- Enter Asset ID in:
    - MDM / endpoint manager (Intune)
    - CMDB or inventory platform [[IT/Applications/TOPDesk/TOPdesk\|TOPdesk]]
## **6. REPLACEMENT, TRANSFERS & DISPOSAL**
- Transferred assets retain the same Asset ID (unless reimaged or wiped)
- Damaged or missing labels must be replaced immediately
- Label must be destroyed or removed before **secure disposal**
## **7. AUDIT AND VERIFICATION**  
- Conduct physical inventory **bi-annually** or per audit schedule
- Match physical label with Asset Register entry
- Report discrepancies in the **Asset Audit Log**
## **8. ROLES AND RESPONSIBILITIES**

| Role             | Resonsibilities                            |
| ---------------- | ------------------------------------------ |
| [[Functions/IT Support\|IT Support]]   | Apply labels and update register           |
| [[IT/IT\|IT]]           | Maintain inventory and ID structure        |
| Users            | Do not remove, alter, or deface asset tags |
| [[Functions/ISMS Manager\|ISMS Manager]] | Audit labeling process and compliance      |
## **9. NON -COMPLIANCE**
- Missing or unlabeled assets may trigger access suspension or investigation
- Any deliberate tampering must be reported to ISMS and HR
## **10. RELATED DOCUMENTS**

| Process                                                 |
| ------------------------------------------------------- |
| [[IT/PO (Policies)/ISMS-PO-IT-018 Data Retention & Backup Policy\|ISMS-PO-IT-018 Data Retention & Backup Policy]]       |
| [[IT/PR (Procedures)/ISMS-PR-IT-004 IT Asset Management Procedure\|ISMS-PR-IT-004 IT Asset Management Procedure]]        |
| Asset Register Template                                 |
| [[IT/PR (Procedures)/ISMS-PR-SEC-009 Secure Disposal and ReUse Procedure\|ISMS-PR-SEC-009 Secure Disposal and ReUse Procedure]] |
| Asset Assignment Form                                   |
| Asset Audit Log Template                                |








