# 🚀 Cloud-Centric Organization with SOC Integration

This project demonstrates the design and deployment of a **cloud-centric organization** integrated with **SOC (Security Operations Center)** capabilities. It follows a hands-on lab approach, implementing Microsoft 365, Intune, Azure Sentinel, Defender, Terraform, and Cloudflare to build a secure, enterprise-like environment.

---

## 📌 Table of Contents
1. [Introduction](#introduction)
2. [Technologies Used](#technologies-used)
3. [Implementation Steps](#implementation-steps)
   - [Step 1 – Domain Purchase](#step-1--domain-purchase)
   - [Step 2 – Configure Cloudflare](#step-2--configure-cloudflare)
   - [Step 3 – Microsoft 365 Tenant Setup](#step-3--microsoft-365-tenant-setup)
   - [Step 4 – Initial Configuration](#step-4--initial-configuration)
   - [Step 5 – Custom Domain Integration](#step-5--custom-domain-integration)
   - [Step 6 – Licensing](#step-6--licensing)
   - [Step 7 – Security Groups](#step-7--security-groups)
   - [Step 8 – Auto License Assignment](#step-8--auto-license-assignment)
   - [Step 9 – Backup Admin & Intune Enrollment](#step-9--backup-admin--intune-enrollment)
   - [Step 10 – CIS Baselines & Policies](#step-10--cis-baselines--policies)
   - [Step 11 – Defender for Endpoint Integration](#step-11--defender-for-endpoint-integration)
   - [Step 12 – Virtual Machine Onboarding](#step-12--virtual-machine-onboarding)
   - [Step 13 – Mobile Device Management (Android/iOS)](#step-13--mobile-device-management-androidios)
   - [Step 14 – Defender for Office 365](#step-14--defender-for-office-365)
   - [Step 15 – Conditional Access Policies](#step-15--conditional-access-policies)
   - [Step 16 – Azure Sentinel Deployment](#step-16--azure-sentinel-deployment)
   - [Step 17 – SOAR Playbooks & VM Protection](#step-17--soar-playbooks--vm-protection)
4. [Results](#results)
5. [Conclusion](#conclusion)

---

## Introduction
This lab simulates a **real-world enterprise environment** where:
- Cloud identity is managed via **Microsoft Entra/M365**
- Devices are managed using **Intune Autopilot**
- Security is enforced using **Defender (XDR, EDR, O365 protection)**
- SIEM/SOAR capabilities are implemented with **Azure Sentinel**
- Infrastructure automation is handled with **Terraform + GitHub**

---

## Technologies Used
- 🌐 **Cloudflare Zero Trust**
- 💻 **Microsoft 365 / Entra ID / Intune**
- 🛡 **Microsoft Defender (O365, Endpoint, XDR)**
- 📊 **Azure Sentinel (SIEM + SOAR)**
- ⚙️ **Terraform + GitHub**
- ☁️ **Azure Virtual Machines**
- 📱 **Android/iOS device management**

---

## Implementation Steps

### Step 1 – Domain Purchase
- Purchased a custom domain via Namecheap/GoDaddy.
- Will serve as the **primary identity domain** for the organization.

https://github.com/KevinVallyatharyilThomas/IT-Cybersecurity-Portfolio/blob/main/Screenshots/namecheap.png

---

### Step 2 – Configure Cloudflare
- Transferred DNS management to **Cloudflare**.
- Updated registrar nameservers.
- Enabled DNS management for future Zero Trust integration.

📸 Evidence: `evidence/cloudflare-dns.png`

---

### Step 3 – Microsoft 365 Tenant Setup
- Created a new **Microsoft 365 tenant** using trial subscription.
- Chose an `onmicrosoft.com` base domain.
- Configured **MFA** and global admin account.

📸 Evidence: `evidence/m365-tenant.png`

---

### Step 4 – Initial Configuration
- Set up basic Microsoft 365 environment.
- Verified account and enabled admin roles.

📸 Evidence: `evidence/m365-setup.png`

---

### Step 5 – Custom Domain Integration
- Added the purchased domain to M365.
- Verified DNS through Cloudflare integration.
- Configured DNS records for **Exchange, SharePoint, Teams, Intune**.

📸 Evidence: `evidence/domain-verification.png`

---

### Step 6 – Licensing
Activated required trial licenses:
- Enterprise Mobility + Security E5
- Microsoft Defender for O365 (Plan 2)
- Microsoft Defender for Endpoint (Plan 2)
- Microsoft 365 Business Premium

📸 Evidence: `evidence/licenses.png`

---

### Step 7 – Security Groups
- Created **dynamic groups** in Intune/Entra:
  - `policy-baseline-users`
  - `policy-baseline-windows`
- Used queries for automated assignment.

📸 Evidence: `evidence/intune-groups.png`

---

### Step 8 – Auto License Assignment
- Linked licenses to dynamic groups.
- All new users/devices get policies & licenses automatically.

📸 Evidence: `evidence/license-assignment.png`

---

### Step 9 – Backup Admin & Intune Enrollment
- Created a **backup global admin** account.
- Enabled **automatic Intune enrollment**.

📸 Evidence: `evidence/intune-enrollment.png`

---

### Step 10 – CIS Baselines & Policies
- Downloaded Intune baselines from GitHub.
- Imported **CIS-compliant security, compliance, AV, firewall policies**.
- Applied dynamically to devices/users.

📸 Evidence: `evidence/cis-policies.png`

---

### Step 11 – Defender for Endpoint Integration
- Integrated Defender with Intune.
- Enabled **EDR in block mode, live response, tamper protection**.

📸 Evidence: `evidence/defender-intune.png`

---

### Step 12 – Virtual Machine Onboarding
- Built a **Windows 11 VM** in VirtualBox.
- Collected **hardware ID** for Autopilot onboarding.
- Enrolled VM into Intune & applied policies.

📸 Evidence: `evidence/vm-autopilot.png`

---

### Step 13 – Mobile Device Management (Android/iOS)
- Configured **Android Enterprise** via Intune.
- Created **App Protection Policies**.
- Installed apps (Outlook, Teams) via Managed Google Play.

📸 Evidence: `evidence/android-mam.png`

---

### Step 14 – Defender for Office 365
- Secured **Exchange Online, SharePoint, Teams**.
- Configured ATP policies.

📸 Evidence: `evidence/defender-o365.png`

---

### Step 15 – Conditional Access Policies
- Imported CA policies from GitHub.
- Implemented rules for **Zero Trust access control**.
- Excluded backup admin from CA enforcement.

📸 Evidence: `evidence/conditional-access.png`

---

### Step 16 – Azure Sentinel Deployment
- Deployed **Azure Sentinel** using Terraform.
- Connected log sources:
  - Microsoft 365
  - Defender for Endpoint / O365 / Cloud Apps
  - Entra ID
- Enabled default detection rules.

📸 Evidence: `evidence/sentinel-dashboard.png`

---

### Step 17 – SOAR Playbooks & VM Protection
- Created **SOAR playbooks** in Sentinel:
  - Detect brute-force RDP attacks.
  - Block attacker IP in NSG via automation.
- Integrated alerts with Logic Apps.

📸 Evidence: `evidence/soar-playbook.png`

---

## Results
- ✅ Domain integrated with Cloudflare + Microsoft 365
- ✅ Devices onboarded via Autopilot with policies
- ✅ Android secured with Work Profile & Intune
- ✅ Defender + Conditional Access protecting SaaS
- ✅ Azure Sentinel deployed & monitoring logs
- ✅ SOAR playbooks auto-mitigating brute force attacks

---

## Conclusion
This lab successfully simulated an **enterprise-grade cloud-centric organization** with full SOC integration. It demonstrates hands-on skills in:
- Cloud Identity & Access Management
- Device Onboarding & Policy Automation
- Endpoint Protection & XDR
- SIEM & SOAR deployment with Azure Sentinel
- Infrastructure as Code with Terraform

📌 This project showcases **real-world cloud security and SOC implementation** skills suitable for enterprise environments.
