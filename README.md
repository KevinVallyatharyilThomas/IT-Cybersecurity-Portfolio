# Cloud-Centric Organization Lab Portfolio

This portfolio presents a comprehensive walkthrough of setting up a secure, cloud-centric organization from scratch. It is based on a practical lab completed by Kevin and includes the implementation of Microsoft 365, Intune, Azure Sentinel, Cloudflare Zero Trust, and Terraform.

---

## Overview
Kevin's lab demonstrates the end-to-end deployment of a modern cloud infrastructure. It begins with domain registration and DNS setup, followed by Microsoft 365 tenant creation, device management, security policy enforcement, SIEM integration, and Zero Trust architecture using Cloudflare.

---


## Technologies Used
The following technologies were utilized throughout the lab:
- **Microsoft 365 / Entra ID** for identity and productivity services
- **Microsoft Intune** for device management and policy enforcement
- **Microsoft Defender for Endpoint & Office 365** for threat protection
- **Azure Sentinel** for SIEM and incident response
- **Cloudflare Zero Trust** for secure access and network filtering
- **Terraform** for infrastructure automation
- **GitHub & VS Code** for version control and development

---

## Step-by-Step Setup

### 1. Domain Registration & DNS
Kevin registered a domain via Namecheap and transferred DNS management to Cloudflare. This enabled future integration with Cloudflare Zero Trust.

### 2. Microsoft 365 Tenant Setup
A new Microsoft 365 tenant was created using an onmicrosoft.com domain. A custom domain was added and verified via Cloudflare DNS. Licenses such as EMS E5, Defender P2, and M365 Business Premium were activated.

### 3. Intune Device Management
Dynamic security groups were created to manage users and devices. Autopilot profiles were configured, and hardware IDs were imported to onboard devices automatically.

### 4. Security Policies via Intune
CIS benchmark policies were imported using PowerShell and GitHub projects. These included compliance, antivirus, firewall, encryption, and attack surface reduction policies.

### 5. Defender for Endpoint Integration
Endpoint Detection and Response (EDR) was enabled via Intune. Integration with Microsoft Defender ensured real-time protection and policy enforcement.

### 6. Android Device Management
Android Enterprise was configured with Managed Google Play. App protection and compliance policies were created and tested using Android Studio Emulator.

### 7. Email & SaaS Security
Defender for Office 365 was configured to secure email services. Cloud App Security was integrated to monitor and control SaaS applications.

### 8. Conditional Access
Conditional Access policies were imported from GitHub and applied to users and devices. Global admin accounts were excluded to prevent lockouts.

### 9. SIEM with Azure Sentinel
Azure Sentinel was deployed using Terraform. Data connectors were configured to ingest logs from Defender, Office 365, Entra ID, and other sources.

### 10. SOAR Automation
A playbook was created to detect RDP brute-force attacks. Azure Logic Apps and Automation Runbooks were used to block attacker IPs and notify security teams.

### 11. Cloudflare Zero Trust
Cloudflare Zero Trust was configured using Terraform. Identity providers, access groups, device posture checks, and gateway policies were defined to enforce secure access.

---

## Security Features
The lab implemented multiple layers of security:
- Endpoint Detection & Response (EDR)
- Conditional Access & Multi-Factor Authentication (MFA)
- DNS & HTTP filtering via Cloudflare
- Device compliance enforcement with Intune
- Threat Intelligence integration with Sentinel

---

## Automation & Infrastructure as Code
Terraform was used to automate:
- Azure Sentinel deployment
- Virtual machine provisioning
- Cloudflare Zero Trust configuration
GitHub served as the version control platform for all infrastructure code.

---

## SIEM & Monitoring
Azure Sentinel provided centralized log aggregation and incident detection. Custom analytics rules, hunting queries, and workbooks were used to monitor and respond to threats.

---

## Testing Methodology
The lab included rigorous testing:
- Role-based access validation for Red and Blue teams
- Device posture checks for encryption, OS version, and compliance
- SCIM provisioning sync between Azure AD and Cloudflare
- Gateway policy enforcement and log analysis

---

## Conclusion
This portfolio showcases Kevin's hands-on expertise in building a secure, scalable, and automated cloud-centric organization. It reflects real-world skills in cloud security, device management, and infrastructure automation.

