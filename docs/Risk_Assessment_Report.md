# Technical Security Audit & Risk Assessment Report

## 1. Vulnerability Analysis & Remediation Plans

### RISK-01: Shared Guest & POS Network Infrastructure
* **Target Asset:** POS Terminals, Receipt Printers, Management PC
* **Vulnerability:** Absence of VLAN separation on wireless access points.
* **Threat Scenario:** A rogue client connected to the public Wi-Fi network uses ARP spoofing or port scanning to discover internal POS devices and exploit unpatched network service vulnerabilities.
* **Risk Score:** **HIGH**
* **Remediation Plan:**
  1. Configure 802.1Q VLAN tag support on the primary gateway/router.
  2. Create **VLAN 10** (Management & POS) and **VLAN 20** (Guest Network).
  3. Enable **Client Isolation** on VLAN 20 to prevent guest-to-guest communications.
  4. Implement firewall drop rules blocking traffic originating from VLAN 20 targeted at VLAN 10.

---

### RISK-02: Shared Administrative Credentials Across Shifts
* **Target Asset:** POS Management Software & System Settings
* **Vulnerability:** Generic shift login accounts with elevated permissions.
* **Threat Scenario:** Insider misuse or unauthorized system adjustments (e.g., inventory manipulation, price overrides) cannot be traced to an individual worker.
* **Risk Score:** **HIGH*
* **Remediation Plan:**
  1. Implement Role-Based Access Control (RBAC).
  2. Assign unique 4-digit PINs / accounts for each staff member.
  3. Restrict high-privilege operations (refunds, database access, system updates) strictly to manager accounts protected by strong passwords.

---

### RISK-03: Local POS Database Backup Vulnerability
* **Target Asset:** Sales History, Inventory Records, Financial Databases
* **Vulnerability:** Backups saved locally on the primary POS storage drive without offsite replication.
* **Threat Scenario:** Storage drive corruption or malware/ransomware outbreak results in total loss of operational data and inventory records.
* **Risk Score:** **HIGH** (Likelihood: Medium, Impact: High)
* **Remediation Plan:**
  1. Implement the **3-2-1 Backup Rule**: 3 copies of data, 2 different media types, 1 offsite.
  2. Configure nightly automated encrypted cloud backups for POS database files.
  3. Periodically test database restoration to ensure backup integrity.
