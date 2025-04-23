---
{"dg-publish":true,"permalink":"/it/pr-procedures/isms-pr-sec-010-incident-response-procedure/","tags":["incident","response","procedure"],"noteIcon":"default"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 15-04-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 5.24, 5.25, 5.26, 5.27

---
## **1. PURPOSE**  
To define a standardized approach for identifying, reporting, analyzing, responding to, and learning from information security incidents in order to minimize damage and support continuous improvement
## **2. SCOPE**
This procedure applies to:
- All employees, contractors, and third parties
- All information systems, networks, cloud services, and physical devices
- Any suspected or confirmed security event or incident involving the confidentiality, integrity, or availability of information assets  
## **3. DEFINITIONS**

| Term                      | Description                                                                 |
| ------------------------- | --------------------------------------------------------------------------- |
| **Security Event**        | An observable occurrence in a system or network.                            |
| **Security** **Incident** | A security event that compromises or poses a risk to organizational assets. |
| **Major Incident**        | An incident with significant business, regulatory, or reputational impact.  |
## **4. RESPONSIBILITIES**

#### 4.1 Identification

- Users must report suspected incidents immediately via [email/ticket/phone].
- Events that may trigger incident response include:
    - Unauthorized access attempts
    - Malware infections
    - Data breaches or data loss
    - Unusual system behaviour or outages
#### 4.2 Logging & Classification
- All reported incidents must be logged in the **Incident Register**.
- Incidents are classified based on:
    - Severity (Low / Medium / High / Critical)
    - Impact (Data, system, financial, compliance)
#### 4.3 Initial Assessment

- IT/Security reviews the report to:
    - Confirm if it is a true incident
    - Determine scope, affected systems, and potential impact
    - Assign response team and priority
#### 4.4 Containment
- Immediate steps taken to prevent further damage (e.g., disconnect system, revoke access, isolate device
#### 4.5 Eradication & Recovery
- Remove the threat (e.g., malware clean-up, patching)
- Restore systems from backups if needed
- Verify full functionality and integrity before returning systems to production
#### 4.6 Notification & Escalation
- Notify stakeholders, management, and regulators (if required by law) within defined SLAs.
- Escalate major or regulatory-impacting incidents to the ISMS Steering Committee.
#### 4.7 Post-Incident Review
- Conduct a **Root Cause Analysis (RCA)**
- Document lessons learned
- Update relevant policies, controls, or training materials
- Review response performance and process gaps
## 5. ROLES AND RESPONSIBILITIES**

| Role               | Responsibility                                               |
| ------------------ | ------------------------------------------------------------ |
| Incident Reporter  | Identify and report suspected incidents                      |
| [[Functions/IT Engineer\|IT Engineer]]    | Investigate, contain, recover, and document incidents        |
| [[Functions/ISMS Manager\|ISMS Manager]]   | Coordinate high-impact incidents, notify stakeholders        |
| Business Owners    | Support containment and business continuity                  |
| Legal / Compliance | Review regulatory impact and external reporting requirements |
## **6. DOCUMENTATION AND EVIDENCE**  
Maintain the **Incident Log** with:
- Unique ID, date/time, description, severity
- Steps taken, resolution, recovery time
- Approvals and RCA summary
## **7. TESTING AND REVIEW**
- Incident response plans must be **tested at least annually** through:
    - Simulated incidents (tabletop exercises)
    - Real incident postmortems
- Procedure must be reviewed **annually** or after a major incident.
## **8. RELATED DOCUMENTS**

| Proces                                                             |
| ------------------------------------------------------------------ |
| [[IT/PO (Policies)/ISMS-PO-IT-001 IT Security Policy\|ISMS-PO-IT-001 IT Security Policy]]                              |
| [[IT/PO (Policies)/ISMS-PO-IT-004 Backup and Recovery Policy\|ISMS-PO-IT-004 Backup and Recovery Policy]]                      |
| [[IT/PO (Policies)/ISMS-PO-SEC-008 Logging and Monitoring Policy\|ISMS-PO-SEC-008 Logging and Monitoring Policy]]                  |
| [[IT/PO (Policies)/ISMS-PO-SEC-003 Information Classification and Handling Policy\|ISMS-PO-SEC-003 Information Classification and Handling Policy]] |
| Incident Log Template / Root Cause Analysis Template               |
|                                                                    |











