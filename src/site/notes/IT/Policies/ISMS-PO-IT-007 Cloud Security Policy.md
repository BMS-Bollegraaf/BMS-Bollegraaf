---
{"dg-publish":true,"permalink":"/it/policies/isms-po-it-007-cloud-security-policy/","tags":["policy","cloud","security"],"noteIcon":"default"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 5.23, 5.10, 8.1, 8.27

---
## **1. PURPOSE**  
To define the organization's approach to managing and securing the use of cloud services, ensuring confidentiality, integrity, and availability of data and systems hosted in the cloud.
## **2. SCOPE**
This policy applies to:

- All cloud services used by the organization (e.g., AWS, Azure, GCP, Microsoft 365, Google Workspace)
- All employees, administrators, and third parties accessing or managing cloud-based systems or data  
 
## **3. POLICY STATEMENT**S 
#### 3.1 Cloud Service Provider (CSP) Selection

- Only approved CSPs that meet the organization’s security and compliance requirements may be used.
- CSPs must provide:
    - Data encryption
    - Logging and monitoring capabilities
    - Compliance with relevant standards (e.g., ISO 27001, SOC 2, GDPR)
#### 3.2 Access Control
- Access must be role-based and follow the principle of least privilege.
- All cloud administrator accounts must use **multi-factor authentication (MFA)**.
- Default passwords and access keys must be rotated and securely stored.
#### 3.3 Data Protection
- All sensitive and classified data stored or processed in the cloud must be encrypted **in transit and at rest**.
- Data must be stored in approved geographic regions aligned with regulatory requirements.

#### 3.4 Configuration Management
- Cloud infrastructure must be configured using secure baselines.
- Infrastructure-as-Code (IaC) practices must include code review and version control.
#### 3.5 Logging and Monitoring
- All critical cloud services must enable **logging, monitoring, and alerting** (e.g., AWS CloudTrail, Azure Monitor).
- Logs must be retained and reviewed regularly as per the Logging and Monitoring Policy.
#### 3.6 Backup and Recovery
- Backup policies must apply to cloud-hosted systems, and recovery procedures must be documented and tested.
#### 3.7 Vendor Risk and SLA Management
- Security and data protection obligations must be clearly defined in **contracts or SLAs**.
- Third-party risk assessments must be performed before onboarding any new cloud services.
#### 3.8 Acceptable Use
- Users must not use cloud services for personal or unauthorized storage, sharing, or processing of organizational data.
- Any external sharing must be approved and logged.
## **4. ROLES AND RESPONSIBILITIES**

| **Role**             | **Responsibility**                                  |
| -------------------- | --------------------------------------------------- |
| Cloud Administrators | Configure, secure, and maintain cloud platforms     |
| Users                | Follow acceptable use guidelines                    |
| [[Functions/IT Engineer\|IT Engineer]]      | Monitor, audit, and ensure compliance               |
| [[Functions/ISMS Manager\|ISMS Manager]]     | Oversee cloud-related risk and compliance processes |
## **5. COMPLIANCE**  
Non-compliance may result in exposure to data breaches or regulatory violations and will be subject to disciplinary or legal consequences.
## **6. REVIEW**  
This policy must be reviewed **annually** or after:
- Significant changes to cloud architecture
- Adoption of new cloud platforms or services
- Cloud-related incidents or audit findings
## 7. RELATED DOCUMENTS  

| Proces                                            |
| ------------------------------------------------- |
| [[IT/Policies/ISMS-PO-SEC-001 Information Security Policy\|ISMS-PO-SEC-001 Information Security Policy]]   |
| [[IT/Policies/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]         |
| [[IT/Policies/ISMS-PO-SEC-008 Logging and Monitoring Policy\|ISMS-PO-SEC-008 Logging and Monitoring Policy]] |
| Vendor Management Policy                          |
| Data Classification & Handling Policy             |
