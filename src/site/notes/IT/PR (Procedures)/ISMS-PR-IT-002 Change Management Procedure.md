---
{"dg-publish":true,"permalink":"/it/pr-procedures/isms-pr-it-002-change-management-procedure/","tags":["Change","procedure"],"noteIcon":"default"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/ISMS Manager\|ISMS Manager]] / [[Functions/IT Manager\|IT Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 8.32, 5.36, 5.33, 8.25

---
## **Table of Contents**  
1. [PURPOSE](#purpose)  
2. [SCOPE](#scope)  
3. [TYPE OF CHANGES](#type-of-changes)  
4. [CHANGE LIFECYCLE](#change-of-lifecycle)  
5. [EMERGENCY CHANGE PROTOCOL](#emergency-change-protocol)  
6. [DOCUMENTS REQUIREMENTS](#documents-requirements)  
7. [ROLES AND RESPONSIBILITIES](#roles-and-responsibilities)  
8. [AUDIT & REVIEW](#audit-review) 
9. [RELATED DOCUMENTS](#related-documents)

---
## **1. PURPOSE**  
To ensure that all changes to IT systems, infrastructure, and applications are **requested, assessed, approved, implemented, and reviewed** in a controlled and secure manner, reducing risk of service disruption or security impact.
## **2. SCOPE**
Applies to:
- All changes affecting live production systems, networks, applications, or cloud services
- All staff, vendors, or third parties performing changes under contract or SLA
- Environments including production, development, test, and DR
## **3. TYPE OF CHANGES** 

| Type      | Descripton                                  | Examples                                            |
| --------- | ------------------------------------------- | --------------------------------------------------- |
| Standard  | Pre-approved, low-risk, recurring           | OS patching, software updates, new user creation    |
| Normal    | Non-urgent changes that require risk review | Firewall rule change, server upgrade, config change |
| Emergency | Urgent, time-sensitive changes              | Zero-day patch, outage recovery, breach mitigation  |
## **4. CHANGE LIFECYCLE**

#### Step 1: **Request Submission**
- Submit a **Change Request (CR)** via ITSM [[IT/Applications/TOPDesk/TOPdesk\|TOPdesk]] or change form
- Include: purpose, risk level, rollback plan, impacted services, and requester
#### Step 2: **Impact Assessment**
- IT team + system owner review:
    - Business risk
    - Security impact
    - Dependencies and downtime
    - Data confidentiality or availability issues
#### Step 3: **CAB Review (Normal/Emergency)**
- **[[Functions/CAB (Change Advisory Board)\|CAB (Change Advisory Board)]]** reviews medium/high-risk changes
- Emergency changes may be **post-reviewed** if urgent
#### Step 4: **Approval**
- Approval required from:
    - Technical lead (for low/standard risk)
    - [[Functions/CAB (Change Advisory Board)\|CAB (Change Advisory Board)]] + [[Functions/ISMS Manager\|ISMS Manager]] (for high/critical impact)
#### Step 5: **Implementation**
- Perform change during approved window
- Notify users and stakeholders as per the **Change Communication Plan**
- Log execution results and any deviations from plan
#### Step 6: **Post-Change Review**
- Confirm success and document outcomes
- Restore service or rollback if required
- Close the request with **lessons learned (if applicable)**
## **5. EMERGENCY CHANGE PROTOCOL**  
- Notify [[Functions/ISMS Manager\|ISMS Manager]] and [[Functions/CAB (Change Advisory Board)\|CAB (Change Advisory Board)]] lead immediately
- Proceed with change if it:
    - Prevents major outage or data loss
    - Is needed for critical patching or compliance
- Document and **review within 1 business day**
## **6. DOCUMENTS REQUIREMENTS**  

Every change record must include:
- Change ID and type
- Description and rationale
- Risk rating and impacted assets
- Implementation & rollback plan
- Approvals and testing notes
- Final status and lessons learned
## **7. ROLES AND RESPONSIBILITIES**  

| Role                            | Responsibility                              |
| ------------------------------- | ------------------------------------------- |
| Change Requester                | Submits detailed CR and coordinates with IT |
| Technical Approver              | Reviews feasibility and risks               |
| [[Functions/CAB (Change Advisory Board)\|CAB (Change Advisory Board)]] | Approves or rejects high-impact changes     |
| [[IT/IT\|IT]]                          | Executes change and logs results            |
| [[Functions/ISMS Manager\|ISMS Manager]]                | Ensures compliance, audits change records   |
## **8. AUDIT & REVIEW**
- Change logs must be retained for **at least 12 months**
- Quarterly reviews of:
    - Change volumes
    - Failed vs successful changes
    - Emergency change trends
- Annual policy review or after any major incident
## **9. RELATED DOCUMENTS**

| [[IT/PO (Policies)/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]                            |     |
| -------------------------------------------------------------------- | --- |
| [[IT/PO (Policies)/ISMS-PO-IT-020 Windows Active Directory Naming Convention Policy\|ISMS-PO-IT-020 Windows Active Directory Naming Convention Policy]] |     |
| [[IT/SOP (Standard Operating Procedure)/ISMS-SOP-IT-SECWR Secure Workstation & Remote Access SOP\|ISMS-SOP-IT-SECWR Secure Workstation & Remote Access SOP]]         |     |
| Firewall Change Request Form                                         |     |
| Change Request Log Template                                          |     |
| CAB Meeting Minutes Template                                         |     |





