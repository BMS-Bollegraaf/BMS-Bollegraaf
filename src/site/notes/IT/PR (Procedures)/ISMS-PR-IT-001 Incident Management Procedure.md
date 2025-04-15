---
{"dg-publish":true,"permalink":"/it/pr-procedures/isms-pr-it-001-incident-management-procedure/","tags":["incident","procedure"]}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Related Documents:**
**ISO/IEC 27001 Controls:** 5.24, 5.25, 5.26, 5.27

---
## **Table of Contents**  
1. [PURPOSE](#purpose)  
2. [SCOPE](#scope)  
3. [POLICY STATEMENTS](#policy statement)  
4. [INCIDENT MANAGEMENT LIFECYCLE](#roles-and-responsibilities)  
5. [INCIDENT RECORDS](#6)  
6. [ROLES AND RESPONSIBILITIES](#responsibilities)  
7. [REVIEW](#compliance)  
8. [RELATED DOCUMENTS](#8)  

---
## **1. PURPOSE**  
To establish a consistent and coordinated approach to detecting, reporting, investigating, and resolving IT and information security incidents in order to minimize impact and support continuous improvement.
## **2. SCOPE**
This procedure applies to:
- All IT and information security incidents (e.g., system outages, data breaches, malware infections)
- All employees, contractors, service providers, and systems within the ISMS scope
 
 ## **3. DEFINITIONS** 
 
| Term               | Definition                                                                                                |
| ------------------ | --------------------------------------------------------------------------------------------------------- |
| **Event**          | Any observable occurrence in a system or network                                                          |
| **Incident**       | An event that adversely affects the confidentiality, integrity, or availability of information or systems |
| **Major Incident** | A high-impact incident causing service disruption or regulatory breach                                    |
|                    |                                                                                                           |
## **4. INCIDENT MANAGEMENT LIFECYCLE**
#### 4.1 Identification
- Incidents may be detected via:
    - Monitoring tools (e.g., SIEM, NMS)
    - User reports (via ticketing system, email, phone)
    - Third-party notifications (e.g., suppliers, regulators)
- Reported incidents must be logged with:
    - Date/time, reporter, system affected, initial symptoms
#### 4.2 Classification and Prioritization
- Incidents are classified based on impact and urgency:
    - **High**: Critical systems, regulatory breach, widespread disruption
    - **Medium**: Localized disruption, recoverable within SLA
    - **Low**: Minor or contained incidents
#### 4.3 Containment
- Short-term containment actions (e.g., isolate system, revoke access) to limit further impact
- Long-term containment to maintain business continuity until root cause resolve.
#### 4.4 Investigation and Diagnosis
- IT/Security team analyzes logs, alerts, and symptoms to determine:
    - Root cause
    - Systems and data affected
    - Entry point or attack vector
#### 4.5 Resolution and Recovery
- Restore affected services using clean backups or patching
- Verify system integrity and confirm normal operations
- Remove temporary controls and reinstate normal services
#### 4.6 Communication and Escalation
- Stakeholders are notified based on severity (e.g., users, management, legal)
- **Major incidents** are escalated to the ISMS Steering Committee and may involve regulators

#### 4.7 Post-Incident Review
- Root Cause Analysis (RCA) must be conducted for major or recurring incidents
- Lessons learned are documented and used to update:
    - Controls, policies, procedures
    - Awareness programs and system configurations
## **5. INCIDENT RECORDS**  
The following must be maintained:
- Incident Log (ID, type, impact, status, resolution time)
- Evidence and audit trails
- Communication logs
- RCA Report (if applicable)
- Corrective Action Plan (CAP)
## **6. ROLES AND RESPONSIBILITIES

| Role             | Resonsibilities                                             |
| ---------------- | ----------------------------------------------------------- |
| End Users        | Report incidents and cooperate during investigations        |
| [[Functions/IT Support\|IT Support]]   | Log and respond to reported incidents                       |
| [[Functions/IT Engineer\|IT Engineer]]  | Analyze, contain, and resolve security-related incidents    |
| [[Functions/ISMS Manager\|ISMS Manager]] | Coordinate major incident response and ensure documentation |
| Top Management   | Review critical incident outcomes and support resources     |
## **7. REVIEW**  
This procedure must be reviewed **annually**, or after:
- A major incident
- Updates to tools, roles, or regulations
- Recommendations from internal or external audits
## **8. RELATED DOCUMENTS**

| Process                                           |
| ------------------------------------------------- |
| [[IT/PO (Policies)/ISMS-PO-SEC-001 Information Security Policy\|ISMS-PO-SEC-001 Information Security Policy]]   |
| [[IT/PO (Policies)/ISMS-PO-IT-017 IT Service Managent Policy\|ISMS-PO-IT-017 IT Service Managent Policy]]     |
| [[IT/PO (Policies)/ISMS-PO-SEC-008 Logging and Monitoring Policy\|ISMS-PO-SEC-008 Logging and Monitoring Policy]] |
| [[IT/PO (Policies)/ISMS-PO-SEC-004 Password Policy\|ISMS-PO-SEC-004 Password Policy]]               |
| [[IT/PR (Procedures)/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]   |
| Incident Log Template                             |
| Root Cause Analysis Template                      |
|                                                   |








