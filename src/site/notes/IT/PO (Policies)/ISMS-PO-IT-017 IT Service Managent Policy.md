---
{"dg-publish":true,"permalink":"/it/po-policies/isms-po-it-017-it-service-managent-policy/"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Related Documents:**
**ISO/IEC 27001 Controls:** 5.31, 5.32, 5.34, 5.35, 5.36, 8.5
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
This policy defines the framework for managing IT services using Topdesk in alignment with ISO/IEC 27001, supporting the secure and effective handling of service requests, incidents, assets, and changes.
## **2. SCOPE**
This policy applies to:
- All IT services delivered by the internal IT team or third-party providers
- All employees, contractors, and business units using or supporting IT services
- All support processes, tools, and systems used for IT service delivery and incident response
## **3. POLICY STATEMENTS** 
#### 3.1 Service Delivery Framework
- IT services must be aligned with business needs and delivered using a consistent **IT Service Management (ITSM)** approach.
- Services must be documented with **Service Level Agreements (SLAs)** or **Operational Level Agreements (OLAs)**
#### 3.2 Incident Management
- All IT incidents must be:
    - Reported via a centralized ticketing system 
    - Logged with severity, impact, and resolution details
    - Resolved within agreed SLAs and escalated when needed

#### 3.3 Request Fulfillment
- Service requests (e.g., access, hardware, software) must follow documented procedures and approval workflows.
- Request types, response times, and fulfillment steps must be defined and tracked.
#### 3.4 Change Management
- All significant IT changes must follow the **[[IT/PO (Policies)/ISMS-PO-IT-002 Change Management Policy\|ISMS-PO-IT-002 Change Management Policy]]**:
    - Risk-assessed
    - Approved by CAB or delegated approvers
    - Logged and communicated to stakeholders

#### 3.5 Configuration and Asset Management
- IT assets and configurations must be recorded in the **Asset & Configuration Management Database [[IT/Applications/TOPDesk/TOPdesk\|TOPdesk]] (CMDB)**.
- Changes to configurations must be tracked and audited.
#### 3.6 Service Continuity and Availability
- IT services must have **business continuity plans** and **disaster recovery procedures** appropriate to their criticality.
- Regular backup, restore, and failover tests must be conducted.

#### 3.7 Monitoring and Reporting
- Systems must be monitored for uptime, performance, and capacity.
- Regular reports must be provided to management, including:
    - Ticket resolution metrics
    - Downtime or SLA breaches
    - Root cause of major incidents
#### 3.8 External Providers
- Outsourced IT services must have:
    - Defined contracts and SLAs
    - Regular performance reviews
    - Risk assessments and compliance monitoring
## **4. ROLES AND RESPONSIBILITIES**

| **Role**         | **Responsibility**                                                  |
| ---------------- | ------------------------------------------------------------------- |
| [[IT/Servicedesk/Servicedesk\|Servicedesk]]  | First-line support, incident logging, ticket triage in  [[IT/Applications/TOPDesk/TOPdesk\|TOPdesk]] |
| [[Functions/IT Manager\|IT Manager]]   | Oversee service delivery, reporting, and escalations                |
| Change Manager   | Approve and document changes                                        |
| Service Owners   | Define and review service KPIs, SLAs                                |
| [[Functions/ISMS Manager\|ISMS Manager]] | Ensure ITSM aligns with ISMS and security requirements              |
## **5. COMPLIANCE**  
Non-compliance may result in:
- Service disruptions
- SLA penalties
- Audit findings
- Disciplinary action or vendor penalties
## **6. REVIEW**  
This policy shall be reviewed **annually**, or when:
- Major services are introduced or retired
- Incident trends show systemic issues
- Feedback from audits or users requires changes
## **7. RELATED DOCUMENTS**  

| Proces                                        |
| --------------------------------------------- |
| Incident Managent Policy                      |
| [[IT/PO (Policies)/ISMS-PO-IT-002 Change Management Policy\|ISMS-PO-IT-002 Change Management Policy]]   |
| [[IT/PO (Policies)/ISMS-PO-IT-012 IT Asset Management Policy\|ISMS-PO-IT-012 IT Asset Management Policy]] |
| [[IT/PO (Policies)/ISMS-PO-IT-004 Backup and Recovery Policy\|ISMS-PO-IT-004 Backup and Recovery Policy]] |
| Service Catalog                               |
| SLA Templates                                 |
| IT Ticketing & Escalation Workflow            |
|                                               |
## **8. ISO/IEC 27001 CONTROL MAPPING

| ISO Control | Desciption                                | [[IT/Applications/TOPDesk/TOPdesk\|TOPdesk]] Module     |
| ----------- | ----------------------------------------- | ---------------------- |
| A.5.9       | Inventory of Information and Other Assets | Asset Management       |
| A.8.7       | Review of User Access Rights              | Service Requests       |
| A.8.8       | Protection Against Malware                | Incident Management    |
| A12.1.2     | Change Management                         | Change Management      |
| A.16.1.2    | Reporting Information Security Events     | Incident Management    |
| A.5.32      | Logging and Monitoring Activities         | Audit Trails & Reports |








