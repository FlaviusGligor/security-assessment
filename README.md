# security-assessment
Cybersecurity risk assessment and POS infrastructure security audit for a local hospitality venue.
# Hospitality & POS Cybersecurity Risk Assessment

![Security Shield](https://img.shields.io/badge/Domain-Cybersecurity_Audit-blue)
![Sector](https://img.shields.io/badge/Industry-Hospitality_/_Horeca-purple)
![Framework](https://img.shields.io/badge/Framework-NIST_CSF_/_CIS_Controls-green)
![Context](https://img.shields.io/badge/Academic-Google_Cybersecurity_Seminars_UVT-orange)

## Overview
This repository presents a practical **Cybersecurity Risk & Infrastructure Assessment** conducted for a local Hospitality establishment (Restaurant / Bar venue). 

The evaluation focuses on critical operational pain points common in the Horeca sector: point-of-sale (POS) network isolation, credentials management during multi-shift operations, guest Wi-Fi co-mingling, and physical/operational access security.

> **Data Privacy & Anonymization:** All infrastructure identifiers, venue details, employee information, and IP addresses have been fully anonymized (PII/Corporate Privacy).

---

## Scope & Operational Domains Evaluated

* **POS Infrastructure & Payment Processing:** Network routing, POS endpoint isolation (Freya POS environment), and peripheral device exposure.
* **Network Segmentation & Wireless Security:** Co-existence of public guest Wi-Fi and internal business management networks.
* **Identity & Shift Management:** Shared account credentials, administrative privileges across staff shifts, and role-based access.
* **Physical Security & Endpoint Hygiene:** Access to network hardware, unattended terminals, and physical cabinet locking.

---

## Key Assessment Findings & Risk Matrix

| Risk ID | Domain | Identified Vulnerability / Threat Scenario | Severity | Remediation Strategy |
| :--- | :--- | :--- | :--- | :--- |
| **RISK-01** | Network | **Public/POS Co-mingling:** Guest Wi-Fi shares the same logical segment as POS devices | **HIGH** | Implement 802.1Q VLANs with Client Isolation on guest subnet |
| **RISK-02** | Access | **Shared Admin Accounts:** Generic shift logins without individual accountability | **HIGH** | Role-Based Access Control (RBAC) & unique shift PINs/accounts |
| **RISK-03** | Physical | **Unsecured Network Hardware:** Exposed switches/routers in accessible staff areas | **MEDIUM** | Lockable wall-mount rack cabinet & unused port shutdown |
| **RISK-04** | Backup | **Local Database Backups:** POS sales database stored locally without offsite encryption | **HIGH** | Automated daily encrypted offsite backups (3-2-1 Rule) |

---

## Applied Frameworks & Standards
* **NIST Cybersecurity Framework (NIST CSF 2.0):** Identify, Protect, Detect, Respond, Recover.
* **CIS Critical Security Controls (v8):** Implementation Group 1 (IG1 - Small Business Hygiene).

---

## Repository Structure
* `/docs/Executive_Summary.md` - Non-technical high-level briefing for business owners/managers.
* `/docs/Risk_Assessment_Report.md` - Technical audit report with threat models and mitigation steps.
* `/templates/Assessment_Checklist.md` - Hospitality-focused security evaluation matrix.
