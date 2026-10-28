# Hospitality & POS Cybersecurity Risk Assessment

![Academic Project](https://img.shields.io/badge/Academic_Project-Individual-blue)
![University](https://img.shields.io/badge/Institution-West_University_of_Timi%C8%99oara_(UVT)-darkblue)
![Program](https://img.shields.io/badge/Program-Google_Cybersecurity_Seminars-orange)
![Framework](https://img.shields.io/badge/Framework-NIST_CSF_2.0_/_CIS_Controls-green)

---

## 🎓 Academic Context & Project Ownership

* **Project Type:** Individual Academic Project
* **Institution:** West University of Timișoara (Universitatea de Vest din Timișoara - UVT)
* **Faculty:** Faculty of Mathematics and Computer Science (Informatică)
* **Program / Initiative:** Google Cybersecurity Seminars - Virtual Routes
* **Author / Analyst:** Flavius Răzvan Gligor
* **Assessment Date:** 2026

### Academic Deliverable Summary
This repository contains my individual capstone assessment for the Google Cybersecurity Seminars program at UVT. The objective was to perform an end-to-end security audit and risk evaluation for an operational SME in the local business community, translating academic security principles into an actionable industry deliverable.

> **Data Privacy & Compliance Notice:** In compliance with professional ethics, non-disclosure requirements, and corporate privacy (PII), all specific network identifiers, business names, staff identities, and IP addresses have been fully anonymized.

---

## 📌 Executive Overview

This project presents a comprehensive **Cybersecurity Risk & Infrastructure Assessment** conducted for a local Hospitality venue (Restaurant / Bar). 

The evaluation focuses on operational pain points critical to the Horeca sector: point-of-sale (POS) network isolation, multi-shift credential governance, guest Wi-Fi segregation, and physical/operational endpoint security.

---

## 🎯 Scope & Operational Domains Evaluated

* **POS Infrastructure & Payment Processing:** Network routing, POS endpoint isolation (Freya POS environment), and peripheral device security.
* **Network Segmentation & Wireless Security:** Co-existence of public guest Wi-Fi and internal management networks.
* **Identity & Access Management (IAM):** Shared account credentials across multi-shift staff, administrative privileges, and role-based access.
* **Physical Security & Endpoint Hygiene:** Physical access to networking hardware, unattended terminals, and cabinet locking.

---

## 📊 Key Assessment Findings & Risk Matrix

| Risk ID | Domain | Identified Vulnerability / Threat Scenario | Severity | Remediation Strategy |
| :--- | :--- | :--- | :--- | :--- |
| **RISK-01** | Network | **Public/POS Co-mingling:** Guest Wi-Fi shares the same logical segment as POS devices | **HIGH** | Implement 802.1Q VLANs with Client Isolation on guest subnet |
| **RISK-02** | Access | **Shared Admin Accounts:** Generic shift logins without individual accountability | **HIGH** | Role-Based Access Control (RBAC) & unique shift PINs/accounts |
| **RISK-03** | Physical | **Unsecured Network Hardware:** Exposed switches/routers in accessible staff areas | **MEDIUM** | Lockable wall-mount rack cabinet & unused port shutdown |
| **RISK-04** | Backup | **Local Database Backups:** POS sales database stored locally without offsite encryption | **HIGH** | Automated daily encrypted offsite backups (3-2-1 Rule) |

---

## 🛠️ Frameworks & Methodologies Applied

* **NIST Cybersecurity Framework (NIST CSF 2.0):** Identify, Protect, Detect, Respond, Recover.
* **CIS Critical Security Controls (v8):** Implementation Group 1 (IG1 - Small Business Baseline).

---

## 📂 Repository Structure

```text
├── README.md                           <-- Overview, Academic Context & Risk Matrix
├── docs/
│   ├── Executive_Summary.md            <-- Non-technical briefing for management
│   └── Risk_Assessment_Report.md       <-- Detailed technical audit & mitigation steps
└── templates/
    └── Assessment_Checklist.md         <-- Hospitality-focused security evaluation matrix
