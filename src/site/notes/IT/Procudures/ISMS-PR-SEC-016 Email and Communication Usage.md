---
{"dg-publish":true,"permalink":"/it/procudures/isms-pr-sec-016-email-and-communication-usage/","tags":["procedure","email","communication"],"noteIcon":"default"}
---

 **Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 5.10, 5.29, 8.13, 8.28, 5.36

---
## **1. PURPOSE**  
To define secure, acceptable, and compliant use of email and electronic communication platforms for all personnel, reducing the risk of data leakage, phishing, and policy violations.
## **2. SCOPE**
This procedure applies to:
- All staff, contractors, and third parties using organizational email accounts
- Messaging tools (e.g., Microsoft Teams)
- Communication involving internal, external, and personal data
- Corporate devices and authorized BYOD
## **3. POLICY STATEMENTS** 
- **Email (Microsoft 365 / Exchange)** – for internal/external formal communication
- **Microsoft Teams / Chat** – for internal collaboration
- **Outlook Mobile App** – if enrolled under MDM
- **Approved SMTP relays / Graph API apps** for automated notifications (e.g., service alerts)

## **4. ACCEPTABLE USE RULES**
- Do ✅:
    - Use company email for work-related communication only
    - Encrypt sensitive attachments using OME or zip/password protection
    - Use approved email signatures with confidentiality disclaimers
    - Flag emails as Confidential if required by policy
        
- Do NOT ❌:
    - Send personal or private content
    - Forward work documents to personal email
    - Click unverified links or open suspicious attachments
    - Auto-forward mail to external addresses
## **5. SENDING SENSITIVE INFORMATION**  

| Sensitivity Level | Required Controls                                                                         |
| ----------------- | ----------------------------------------------------------------------------------------- |
| Internal          | No extra controls unless policy demands                                                   |
| Confidential      | Use **encryption**, watermarking, and recipient verification                              |
| Restricted        | Use **secure channels** (e.g., Teams with guest control or SFTP); avoid email if possible |
## **6. ANTI-PHISHING & SECURITY MEASURES**  
- MFA required on all email accounts
- All emails scanned via **SPF, DKIM, DMARC**
- Suspicious messages must be reported using “**Report Phishing**” button
- Use of **external sender tagging** (e.g., `[External]`) enabled
- Internal simulation campaigns may be run quarterly
## **7. MONITORING & LOGGING**  
- Email logs retained for **12 months** for audit and forensic analysis
- Email misuse (e.g., policy violation, malware, data leak) triggers investigation under **[[IT/Procudures/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]**
## **8. OFFBOARDING AND REVOCATION**
- Email accounts disabled within **24 hours** of employee separation
- Auto-reply configured for **30 days**, then mailbox archived or purged per retention policy
- Access to Teams, shared inboxes, and group chats removed immediately

## **9. ROLES AND RESPONSIBILITIES**

| Role             | Responsibility                                                    |
| ---------------- | ----------------------------------------------------------------- |
| End User         | Follow communication policy and report suspicious content         |
| [[IT\|IT]]           | Monitor email security, configure settings, and manage email logs |
| [[Functions/ISMS Manager\|ISMS Manager]] | Review incidents, audit mailbox controls, approve exceptions      |
## **10. RELATED DOCUMENTS**

| Documents                                          |
| -------------------------------------------------- |
| [[IT/Policies/ISMS-PO-SEC-011 Email and Communication Policy\|ISMS-PO-SEC-011 Email and Communication Policy]] |
| [[IT/Procudures/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]]    |
| [[IT/Policies/ISMS-PO-SEC-015 Data Protection Policy\|ISMS-PO-SEC-015 Data Protection Policy]]         |
| [[IT/Standards/ISMS-ST-SEC-001 Email Signature Standard\|ISMS-ST-SEC-001 Email Signature Standard]]       |
| Secure Communication Quick Quide                   |
| Email Access Recovation Checklist                  |
|                                                    |








