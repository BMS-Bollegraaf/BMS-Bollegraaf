---
{"dg-publish":true,"permalink":"/it/po-policies/isms-po-sec-008-logging-and-monitoring-policy/","noteIcon":"lightbulb"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 8.15, 8.16, 5.36, 5.25

---
## **Table of Contents**  
1. [PURPOSE](#purpose)  
2. [SCOPE](#scope)  
3. [POLICY STATEMENTS](#policy-statements)  
4. [ROLES AND RESPONSIBILITIES](#roles-and-responsibilities)  
5. [COMPLIANCE](#compliance)  
6. [REGISTRATION](#registration)  
7. [RELATED DOCUMENTS](#related-documents)  
8. [REGISTRATION](#registrations)  
9. [RELATED DOCUMENTS](#appendices) 
10. [RELATED NORMS AND STANDARDS](#appendices) 
11. [DEFINITIES](#DEFINITIES) 

---
## **1. PURPOSE**  
To establish the organization's requirements for logging and monitoring of systems and activities to detect unauthorized access, security breaches, and ensure accountability.
## **2. SCOPE**
This policy applies to:

- All servers, endpoints, network equipment, applications, cloud platforms, and systems that process or store organizational data
- All employees, contractors, and third parties with access to such systems  
 
## **3. POLICY STATEMENTS** 
 
#### 3.1 Logging Requirements

- Security and system event logging must be **enabled on all critical systems**, including:
    - Authentication and access events (logins, failed attempts)
    - Administrative or privileged account usage
    - System changes or configuration modifications
    - File access and data transfers    
- Logs must include **timestamps, user IDs, system identifiers**, and the event outcome.

#### 3.2 Log Storage and Retention
- Logs must be **protected from unauthorized access or alteration**.
- Retain logs for a minimum of **12 months** or in accordance with legal/regulatory requirements.
- Logs must be stored centrally (e.g., SIEM or secure logging platform).

#### 3.3 Monitoring Requirements
- Security logs must be **monitored regularly** (e.g., daily or real-time via automated tools).
- Monitoring should detect unusual or suspicious activity, including:
    - Multiple failed logins
    - Privileged account misuse
    - Unusual data transfers or network traffic

#### 3.4 Alerting and Response
- Automated alerts should be configured for high-risk events.
- All incidents detected through logging must be responded to per the **Incident Response Procedure**

#### 3.5 Third-Party and Cloud Logging
- Systems hosted by third parties or in the cloud must maintain appropriate logging controls.
- Access to log data from those services must be retained or made available for audite

#### 3.6 Review and Audit
- Log reviews must be documented.
- Internal or external audits may include review of log management practices.
- Log integrity should be verified periodically.

## **4. ROLES AND RESPONSIBILITIES**

| **Role**          | **Responsibility**                                                           |
| ----------------- | ---------------------------------------------------------------------------- |
| [[Functions/IT Engineer\|IT Engineer]]   | Enable logging and monitoring, maintain systems, respond to alerts           |
| [[Functions/ISMS Manager\|ISMS Manager]]  | Ensure policy compliance and review logs as part of the ISMS                 |
| [[Functions/System Owners\|System Owners]] | Validate critical events are logged and retained                             |
| Internal Audit    | Perform reviews of log completeness, retention, and monitoring effectiveness |
## **5. COMPLIANCE**  
Failure to comply with this policy may lead to undetected security breaches, data loss, or regulatory penalties. Violations will be addressed in accordance with HR and disciplinary procedures.
## **6. REGISTRATION**  
This policy must be reviewed **annually**, or upon:

- Significant infrastructure or application changes
- Security incidents involving monitoring gaps
- Changes in legal, regulatory, or contractual obligations 

## 7. RELATED DOCUMENTS  

| Proces                                                             |
| ------------------------------------------------------------------ |
| [[IT/PO (Policies)/ISMS-PO-SEC-001 Information Security Policy\|ISMS-PO-SEC-001 Information Security Policy]]                    |
| [[IT/PO (Policies)/ISMS-PO-IT-006 Vulnerability Management Policy\|ISMS-PO-IT-006 Vulnerability Management Policy]]                 |
| [[IT/PO (Policies)/ISMS-PO-SEC-003 Information Classification and Handling Policy\|ISMS-PO-SEC-003 Information Classification and Handling Policy]] |
| [[IT/PR (Procedures)/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]                    |
| System-Specific Logging Configuration Guidelines                   |












