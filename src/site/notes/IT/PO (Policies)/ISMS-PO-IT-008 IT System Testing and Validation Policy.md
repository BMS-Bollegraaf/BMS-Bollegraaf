---
{"dg-publish":true,"permalink":"/it/po-policies/isms-po-it-008-it-system-testing-and-validation-policy/","tags":["policy","testing","validation"],"noteIcon":"lightbulb"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 5.23, 5.25, 8.29, 8.30

---
## **Table of Contents**  
1. [PURPOSE](#purpose)  
2. [SCOPE](#scope)  
3. [POLICY STATEMENT](#policy-statement)  
4. [ROLES AND RESPONSIBILITIES](#roles-and-responsibilities)  
5. [COMPLIANCE](#compliance)  
6. [REGISTRATION](#registration)  
7. [RELATED DOCUMENTS](#appendices) 



---
## **1. PURPOSE**  
To ensure all new or modified IT systems, applications, and platforms undergo formal testing and validation before being deployed into production, thereby reducing security, performance, and functional risks.
## **2. SCOPE**
This policy applies to:
- All internal and third-party developed applications
- Changes to existing production systems (code, configurations, integrations)
- Infrastructure projects, cloud migrations, and system upgrades
- Testing environments and activities involving organizational systems or data  
 
## **3. POLICY STATEMENTS** 
#### 3.1 Mandatory Testing
- All systems and software must undergo **testing prior to production release**, including:
    - Functional Testing
    - Integration Testing
    - Security Testing (e.g., vulnerability scans, code analysis)
    - User Acceptance Testing (UAT)
#### 3.2 Security Testing
- Security testing must be included in the system development life cycle (SDLC).
- New and updated applications must undergo:
    - Static Application Security Testing (SAST)
    - Dynamic Application Security Testing (DAST)
    - Penetration testing (for high-risk or internet-facing apps)
        
#### 3.3 Test Environment Requirements
- Testing must be conducted in **separate, controlled environments** (not in production).
- Test environments must mirror production as closely as possible.
- Test data must be anonymized or synthetic if using real data.

#### 3.4 Validation and Approval
- A formal **go-live checklist** must be completed and signed off by:
    - [[Functions/System Owners\|System Owners]]
    - [[Functions/Information Security Officer (ISO)\|Information Security Officer (ISO)]] (for high-risk changes)
    - QA/Testing Lead
- Any known risks or unresolved issues must be documented and accepted before deployment.
#### 3.5 Documentation
- Testing results, defects, resolutions, and validation sign-offs must be documented and retained.
- Security testing outcomes must be reported to the ISMS team.
#### 3.6 Outsourced Testing
- Any third parties involved in testing must follow this policy and sign an NDA.
- Testing providers must meet security requirements defined in the **Third-Party Security Policy**.

## **4. ROLES AND RESPONSIBILITIES**

| **Role**                               | **Responsibility**                               |
| -------------------------------------- | ------------------------------------------------ |
| QA/Test lead                           | Manage testing process, document results         |
| Developers                             | Perform unit testing and support QA              |
| [[Functions/System Owners\|System Owners]]                      | Approve UAT and production deployment            |
| [[Functions/Information Security Officer (ISO)\|Information Security Officer (ISO)]] | Review and validate security testing results     |
| IT/DevOps                              | Deploy tested code and ensure rollback readiness |

## **5. COMPLIANCE**  
Non-compliance with this policy may result in deployment failures, security incidents, or system downtime. Violations will be subject to internal investigation and possible disciplinary action.
## **6. REGISTRATION**  
This policy must be reviewed **annually** or when:
- Major changes occur to the development or release process
- A critical deployment failure or security issue arises
- New tools or platforms are introduced
## **7. RELATED DOCUMENTS**

| Proces                                             |     |
| -------------------------------------------------- | --- |
| Secure Development Policy                          |     |
| [[IT/PO (Policies)/ISMS-PO-IT-002 Change Management Policy\|ISMS-PO-IT-002 Change Management Policy]]        |     |
| [[IT/PO (Policies)/ISMS-PO-IT-006 Vulnerability Management Policy\|ISMS-PO-IT-006 Vulnerability Management Policy]] |     |
| [[IT/PR (Procedures)/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]    |     |
| Release & Deployment Checklist                     |     |
| UAT Sign-Off Form                                  |     |











