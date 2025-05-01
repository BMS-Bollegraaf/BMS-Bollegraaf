---
{"dg-publish":true,"permalink":"/it/procudures/isms-pr-007-it-hardware-return-procedure/","noteIcon":"default"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**Related Documents:**
**ISO/IEC 27001 Controls:** A.5.9, A.6.2, A.8.1.3, A.11.2.7

---
## **1. PURPOSE**  
This procedure defines the process for the return of company-owned IT hardware by staff, contractors, and third parties to maintain the confidentiality, integrity, and availability of information assets, and to ensure compliance with ISO/IEC 27001 requirements.
## **2. SCOPE**
Applies to all personnel in possession of company-issued IT hardware, including laptops, desktops, mobile devices, and peripherals. This includes staff offboarding, internal transfers, contract completion, or device replacement.

 ## **3. ROLES AND RESPONSIBILITIES**

| **Role**         | **Responsibility**                                            |
| ---------------- | ------------------------------------------------------------- |
| Employee         | Initiates return, ensures all items are accounted for         |
| Manager / [[HR/HR\|HR]] | Triggers offboarding and asset recovery workflow              |
| [[Functions/IT Support\|IT Support]]   | Coordinates return, performs inspection and data sanitization |
| [[Functions/ISMS Manager\|ISMS Manager]] | Audits compliance with asset return controls                  |
## **4. PROCEDURE STEPS**

#### 4.1 **Initiation**
- Upon offboarding, transfer, or return request, HR or the employee submits a _Hardware Return Request_ through the ISMS/ITSM platform.
- Request must include asset tag(s), serial number(s), and reason for return.
#### 4.2 **Notification (Optional: SMS Integration)**
- Automated notification (email) sent to employee and IT with return instructions.
- Email reminders (if enabled) scheduled 24 hours before return deadline.
#### 4.3 **Return Process**
- Hardware is physically returned to IT Service Desk or via secure courier.
- Receiving personnel verify each item against the asset register.
#### 4.4 **Inspection & Sanitization**
- Devices are checked for physical damage.
- All data is securely wiped in line with the _Media Handling & Disposal Procedure_.
- Access tokens, accounts, and VPN credentials are revoked.
#### 4.5 **Asset Register Update**
- IT updates the Asset Management System to mark items as:
    - Returned and Reusable
    - Returned and Decommissioned
    - Returned and Damaged (if applicable)
#### 4.6 **Confirmation**
- Final confirmation sent to employee and HR via email.
- All records retained for audit and compliance purposes.
## **5. RECORD RETENTION**  
All return records, asset logs, and communications must be retained for a minimum of **2 years**, in accordance with the ISMS documentation policy.
## **6. REVIEW**
This procedure will be reviewed annually by the ISMS Committee and updated as necessary based on risk assessments, audit findings, or organizational changes.
## **7. NON-COMPLIANCE**  
Failure to follow this procedure may result in disciplinary action and will be treated as a breach of the **[[IT/Policies/ISMS-PO-SEC-001 Information Security Policy\|ISMS-PO-SEC-001 Information Security Policy]]**.











