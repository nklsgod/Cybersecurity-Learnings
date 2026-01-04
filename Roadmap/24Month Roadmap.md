# 🗺️ Cloud Security Masterplan: Identity & Automation Focus
**Ziel:** Cloud Security Engineer / IAM Specialist (Azure Focus)
**Strategie:** Identity-First → IaC/Automation → Security Engineering
**Dauer:** 7 Wochen Bootcamp + 24 Monate

---

## 🚦 Phase 0: Das Bootcamp (Woche 0–7)
> **Fokus:** Fundament legen, Repository aufbauen, SC-900.

### Woche 0: Setup & Standards
* [ ] GitHub/GitLab Repo initialisieren
* [ ] Evidence-Standard definieren (`export` > `screenshot`)
* [ ] Dev-Tenant & Lab-VM aufsetzen

### Woche 1: Networking Fundamentals
* [ ] OSI, TCP/IP, DNS, TLS verstehen
* [ ] **Build:** Firewall Intake Process & Port-Cheatsheet
* [ ] **Evidence:** Wireshark PCAP & TLS Handshake Analyse

### Woche 2: Azure Networking Basics
* [ ] VNet, Subnets, NSGs
* [ ] **Build:** Decision-Log Template für Freigaben
* [ ] **Evidence:** NSG-Export & Review-Kommentar

### Woche 3: Endpoint & Hardening
* [ ] Windows Security, Defender, Local Admins
* [ ] **Build:** Client Hardening Baseline v0.1
* [ ] **Evidence:** PowerShell Export Script (Status-Check)

### Woche 4: Identity Basics (Entra ID)
* [ ] User, Groups, Admin Roles
* [ ] **Build:** Identity Export Toolkit v0.1
* [ ] **Evidence:** User/Role-Export via Graph API

### Woche 5: Conditional Access & Governance
* [ ] MFA, Block Legacy Auth, Guest Access
* [ ] **Build:** CA Policy Pack v0.1 (Basis-Regelwerk)
* [ ] **Evidence:** CA Configuration Export (JSON)

### Woche 6: Logging & Detection (Sentinel)
* [ ] Log Analytics, KQL Syntax
* [ ] **Build:** KQL Pack v0.1 (Sign-ins & Audit Queries)
* [ ] **Evidence:** Query Results & Alert Rule Screenshot

### Woche 7: Abschluss & Zertifizierung
* [ ] **Zertifikat:** **SC-900 (Microsoft Security Fundamentals)**
* [ ] **Release:** Repo Version 1.0 (Portfolio-Ready)

---

## 🚀 Phase 1: Das erste Jahr (Identity & Plattform)
> **Mantra:** "Identity is the new Perimeter."

### Q1: Onboarding & Operative Basics (Monat 1–3)
* **Fokus:** Prozesse verstehen, erste "Quick Wins" liefern.
* [ ] **Network:** Firewall/Proxy Prozesse standardisieren.
* [ ] **Endpoint:** Client Baseline v1.0 finalisieren & Drift messen.
* [ ] **Doku:** Erste 4 ADRs (Architecture Decision Records) schreiben.
* [ ] **Output:** Identity Review Toolkit v1.0 (Breakglass, MFA-Coverage).

### Q2: Identity Deep Dive (Monat 4–6)
* **Fokus:** IAM als Spezialisierung.
* [ ] **Zertifikat:** **SC-300 (Identity & Access Administrator)**.
* [ ] **Build:** Conditional Access Pack v2.0 (Design + Doku).
* [ ] **Build:** Privileged Identity Management (PIM) Konzept.
* [ ] **Training:** SOC Level 1 (Teil 1) – Triage & Log Basics.

### Q3: Infrastructure & Linux (Monat 7–9)
* **Fokus:** Die Plattform unter der Security verstehen.
* [ ] **Zertifikat:** **AZ-104 (Azure Administrator)**.
* [ ] **Linux:** Fundamentals, Hardening & SSH Basics.
* [ ] **Build:** Azure Landing Zone v1 (Basic Network/Log Setup).
* [ ] **Build:** RBAC Review Checklist.

### Q4: Security Foundations & GRC (Monat 10–12)
* **Fokus:** Security als Gesamtsystem & Compliance.
* [ ] **Zertifikat:** **CompTIA Security+**.
* [ ] **Build:** Threat-Control-Matrix (Welche Gefahr → Welches Control?).
* [ ] **Build:** Minimales Risk-Register & Control-Matrix.

---

## 🛡️ Phase 2: Das zweite Jahr (Automation & Engineering)
> **Mantra:** "Code beats Click."

### Q5: Infrastructure as Code (IaC) & Data (Monat 13–15)
* **Fokus:** Weg vom Klicken, hin zum Code.
* [ ] **Zertifikat:** **Terraform Associate** (empfohlen) oder IaC Deep Dive.
* [ ] **Data:** Key Vault, Storage Encryption, Private Endpoints.
* [ ] **Build:** IaC Module für Security Resources (Policy, Alerts).
* [ ] **Build:** Container Security Cheatsheet & Lab.

### Q6: Azure Security Engineering (Monat 16–18)
* **Fokus:** Security Controls härten und automatisieren.
* [ ] **Zertifikat:** **AZ-500 (Azure Security Engineer)**.
* [ ] **Build:** Policy as Code (Azure Policy Definitions).
* [ ] **Build:** Security Control Matrix v2.0 (Automated Evidence).
* [ ] **Output:** Defender for Cloud Tuning.

### Q7: Detection & Response (Monat 19–21)
* **Fokus:** Angriffe erkennen und reagieren.
* [ ] **Training:** SOC Level 1 (Teil 2) – SIEM & IR.
* [ ] **Build:** Sentinel MVP (Analytics Rules + Automation).
* [ ] **Build:** KQL Pack v2.0 (Advanced Hunting).
* [ ] **Build:** 3 Incident Response Playbooks (Account, App, Data).

### Q8: Architecture & Portfolio Finish (Monat 22–24)
* **Fokus:** Seniorität zeigen & "Interview-Ready" werden.
* [ ] **Doku:** 5 Architecture One-Pagers (Identity, Network, etc.).
* [ ] **Reporting:** Quarterly Security Posture Report Template.
* [ ] **Portfolio:** Finales Polishing, READMEs, anonymisierte Samples.
* [ ] **Prep:** Interview-Training (Technical & Behavioral).

---

## 🏆 Zertifikats-Roadmap

| Zeitpunkt | Zertifikat | Fokus | Status |
| :--- | :--- | :--- | :--- |
| **Woche 7** | **SC-900** | Grundlagen | ⬜ |
| **Monat 6** | **SC-300** | Identity (Core Skill) | ⬜ |
| **Monat 9** | **AZ-104** | Cloud Admin (Platform) | ⬜ |
| **Monat 12** | **Security+** | General Security Theory | ⬜ |
| **Monat 15** | **Terraform** | IaC / Automation | ⬜ |
| **Monat 18** | **AZ-500** | Cloud Security Eng. | ⬜ |

---

## 📂 Repository Struktur (Soll-Zustand)

```text
/cloud-security-portfolio
├── 00-meta/              # Standards, ADRs, Release Notes
├── 01-endpoint/          # Hardening Baselines (Win/Linux)
├── 02-network/           # Firewall Intake, NSG Patterns
├── 03-identity/          # CA Policies, Entra Exports, PIM
├── 04-infrastructure/    # Terraform/Bicep Code (Landing Zone)
├── 05-detection/         # Sentinel Rules, KQL Pack, IR Playbooks
├── docs/                 # Architecture One-Pagers, Risk Register
└── scripts/              # PowerShell Tooling (Export/Audit)
