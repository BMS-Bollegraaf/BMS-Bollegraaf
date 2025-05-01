---
{"dg-publish":true,"permalink":"/it/policies/isms-po-it-013-network-security-policy/","tags":["network","security","policy"],"noteIcon":"default"}
---

**Effective Date:** 21-03-2025  
**Version:** 1.0  
**Last Updated:** 21-03-2025  
**Approved By:** [Authority Name]  
**Owner:** [[Functions/IT Manager\|IT Manager]]
**Classification:** [[Classification/Internal\|Internal]]
**ISO/IEC 27001 Controls:** 8.20, 8.21, 8.22, 8.15, 5.10

---
## **1. PURPOSE**  
To establish security requirements for the organization’s networks to ensure protection against unauthorized access, threats, disruptions, and data leakage.
## **2. SCOPE**
This policy applies to:
- All internal, external, wired, wireless, and cloud-based networks
- All systems, devices, users, and third parties connecting to or interacting with the organization’s networks
## **3. POLICY STATEMENTS** 
#### 3.1 Network Segmentation
- Networks must be logically or physically segmented based on business function and risk level (e.g., user LAN, server zone, DMZ, guest Wi-Fi).
- Sensitive systems must be isolated from general user traffic.

#### 3.2 Perimeter Security
- Firewalls must be deployed at network boundaries.
- Only required inbound/outbound ports and protocols may be open.
- Intrusion Detection/Prevention Systems (IDS/IPS) must be implemented where appropriate.
#### 3.3 Wireless Networks
- Corporate Wi-Fi must:
    - Use WPA3 (or at least WPA2 Enterprise) encryption
    - Require individual authentication (e.g., 802.1X / RADIUS)
- Guest Wi-Fi must be isolated from corporate resources.

#### 3.4 Remote Access
- Remote users must access the network via secure VPN with **MFA**.
- Split tunneling must be disabled unless specifically authorized.

#### 3.5 Device and Access Control
- Only authorized and registered devices may connect to internal networks.
- Network Access Control (NAC) or endpoint compliance tools should be implemented to verify security posture.

#### 3.6 Monitoring and Logging
- Network traffic must be monitored for anomalies and suspicious activity.
- Logs from routers, firewalls, switches, and VPN gateways must be retained and reviewed regularly.

#### 3.7 Cloud and Hybrid Networks
- Cloud VPCs/VNETs must:
    - Follow similar segmentation and firewall rules as on-premise networks
    - Use security groups, NSGs, and cloud-native firewalls
    - Enable flow logging and encryption for data in transit

#### 3.8 Third-Party Connections
- Third-party connections (e.g., suppliers, vendors) must be:
    - Risk assessed and documented
    - Monitored and time-limited
    - Terminated immediately after project completion
## **4. ROLES AND RESPONSIBILITIES**

| **Role**         | **Responsibility**                                         |
| ---------------- | ---------------------------------------------------------- |
| [[Functions/IT Engineer\|IT Engineer]]  | Implement, monitor, and maintain network security controls |
| [[Functions/IT Manager\|IT Manager]]   | Review network logs and respond to threats                 |
| End Users        | Follow acceptable use and connection policies              |
| [[Functions/ISMS Manager\|ISMS Manager]] | Ensure compliance and alignment with ISO 27001             |
## **5. COMPLIANCE**  
Violations of this policy may result in loss of access, disciplinary action, or legal consequences.
## **6. REVIEW**  
This policy must be reviewed **annually**, or,
- Following a major network change or security incident
- In response to new threats or technologies
- Based on internal/external audit findings
## **7. RELATED DOCUMENTS**  

| Proces                                          |     |
| ----------------------------------------------- | --- |
| [[IT/Policies/ISMS-PO-SEC-006 Access Control Policy\|ISMS-PO-SEC-006 Access Control Policy]]       |     |
| [[IT/Policies/ISMS-PO-IT-010 Remote Access Policy\|ISMS-PO-IT-010 Remote Access Policy]]         |     |
| [[IT/Procudures/ISMS-PR-SEC-010 Incident Response Procedure\|ISMS-PR-SEC-010 Incident Response Procedure]] |     |
| Network Diagram & Asset Register                |     |
| Firewall Change Request Form                    |     |
| [[IT/Guidelines/ISMS-GD-IT-013-A VPN Usage Guidelines\|ISMS-GD-IT-013-A VPN Usage Guidelines]]       |     |









