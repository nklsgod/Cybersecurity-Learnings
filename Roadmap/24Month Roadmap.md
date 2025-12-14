# Cloud-Security Playbook (24 Monate) – **Azure Hauptspur** + **TryHackMe SAL1 (Prio 2)**

**Zeitbudget:** 12h/Woche (neben Job + Uni)  
**Hauptressource (immer):** Pluralsight / A Cloud Guru **inkl. Hands-on Labs**  
**Nebenressource:** Microsoft Learn (Scope/Begriffe, Nachschlagen)  
**Prio 1 Zertifikate:** AZ-900 → Security+ → AZ-104 → (Azure Security Themen) → AZ-500  
**Prio 2 Zertifikat (Flex/Fun + Skills):** **TryHackMe SAL1 (SOC Analyst Level 1)**

> **Prinzip:** SAL1 ist “Prio 2” ⇒ wir bauen es so ein, dass es **deine Azure/CompTIA Ziele nicht stört**.  
> Das heißt: SAL1 läuft als **zeitlich begrenzter Block (ca. 10–12 Wochen)** in Monaten 10–13, wenn du schon Cloud-Grundlagen hast und SOC-Training maximal “andockt”.

---

## 0) Wochenstruktur (12h) – Standard

- 2× 90 min Pluralsight/ACG Kurs (3h)
- 2× 90 min ACG Labs (3h)
- 1× 120 min Build (2h)
- 1× 60 min Review (1h)
- **+ 3h “Flex-Block”** (je nach Phase: Exam-Prep, SAL1, Extra Labs)

**Deliverables pro Woche (Pflicht)**

- 1 Lab-Report, 1 Diagramm, 10–20 Anki-Karten, 1 Seite “What I’d do at work” (Risiko/Logging/Rollback)

---

## 1) Templates (kurz)

### Lab-Report (`00-templates/lab-report.md`)

```md
# Lab: <Titel>

Datum | Dauer | Plattform | Kosten
Ziel | Architektur | Schritte | Nachweise
Security Notes (Risiko/Controls/Logging)
Lessons Learned (3 bullets)
```

### One-Pager Cloud-Doku (`00-templates/one-pager.md`)

```md
Kontext & Need | Scope | Architektur-Link
Top-3 Risiken | Top-5 Controls | Logging/Monitoring
Entscheidungen | Empfehlung
```

---

## 2) Build-Guides (ausformuliert, damit es “wie echte Arbeit” aussieht)

### 2.1 Firewall/Proxy Request Playbook (10 Cases)

**Deliverable-Format**

- `firewall-proxy-playbook/`
  - `playbook.md` (Übersichtstabelle)
  - `case-01_...md` bis `case-10_...md`
  - `checklist_missing-info.md`
  - `risk-library.md` (Exfiltration, C2, MITM, Supply Chain …)

**Case-Detail (Mini-Beispiel)**

```md
# Case – Office 365 via Proxy

Business Need: O365 muss erreichbar sein.

Quelle→Ziel: Client-Subnet → O365 Endpoints (FQDN-Allowlist) via Proxy
Port/Proto: 443/TCP
Risiko: Zu breit = Exfiltration/C2 möglich
Controls: nur Proxy, keine direct egress, kleinste Allowlist, ggf. Zeitfenster
Logging: Proxy logs + Review bei Spikes/neuen Zielen
Test/Rollback: Test Login/Teams; Rollback Regel deaktivieren + Ticket referenzieren
```

### 2.2 Client Hardening Baseline + Ausnahmeprozess

**Deliverable-Format**

- `client-hardening/`
  - `baseline_v1.md` (Tabelle: Setting | Warum | Prüfen | Umsetzen | Nebenwirkung | Ausnahme)
  - `exceptions_process_v1.md` (1 Seite: Antrag → Approval → Laufzeit → Monitoring → Review)
  - `evidence/` (Screenshots + Commands)

### 2.3 Logging/KQL Mini-Notebook (Azure)

**Deliverable-Format**

- `logging-kql/`
  - `kql_notebook_v1.md` (20 Queries, kommentiert)
  - `use-cases.md` (5 Use Cases + Datenquellen + Response steps)
  - `tuning-notes.md` (False positives, Thresholds)

---

# 3) Roadmap (mit deinen Vorgaben + SAL1 eingebaut)

## Monate 1–6 (Fundament)

### Monat 1: Networking + Freigaben (Azure-Umfeld)

- **Prio 1:** Pluralsight/ACG Networking + Azure NSG Labs
- **Build:** Firewall/Proxy Playbook – 5 Cases
- **Optional:** Google Cybersecurity Cert starten (wenn du Struktur willst)

### Monat 2: Linux/Logs + Hardening Basics

- **Prio 1:** Pluralsight Linux + Logging + Windows Hardening
- **Build:** Hardening Baseline v1 + Ausnahmeprozess (10 Settings getestet)

### Monat 3–4: AZ-900 (Azure Fundamentals)

- **Prio 1:** ACG AZ-900 + Labs (RG/VNet/NSG/IAM basics)
- **Build:** 4 One-Pager Cloud-Dokus + Diagramme
- **Milestone:** AZ-900 exam-ready/abgelegt

### Monat 4–6: CompTIA Security+ (Prio 1)

- **Prio 1:** Pluralsight Security+ Track (als Domain-Struktur)
- **Hands-on:** kleine Drills pro Domain (IAM, Network, IR, Crypto) in Azure/AWS-Labs oder lokal
- **Build:** `secplus_to_job_map.md` (Security+)
- **Milestone:** Security+ exam-ready/abgelegt (Ende Monat 6)

---

## Monate 6–12 (Azure Admin → echte Cloud-Skills + Security in Azure)

### Monat 6–9: AZ-104 (Azure Administrator) (Prio 1)

- **ACG:** AZ-104 Track + Labs (Compute/Storage/Network/Monitor/RBAC)
- **Builds (konkret):**
  - M6: Azure Admin Lab Book v1 (4 Labs dokumentiert)
  - M7: Operations Runbook v1 (Patch/Backup/Monitoring)
  - M8: Cost Guardrails v1 (Budgets/Alerts + “was tue ich bei Cost Spike?”)
  - M9: Secure Baseline Pack (Azure) (IAM/Network/Logging je 1 Seite)
- **Milestone:** AZ-104 exam-ready/abgelegt

### Monat 10–12: **Azure Security Themen (Prio 1)** + **SAL1 Vorbereitung (Prio 2)**

Hier dockt SAL1 perfekt an, weil du sowieso Logging/Policy/IR anfässt.

#### Zeitaufteilung pro Woche (12h) in Monaten 10–12

- **6h Azure (Prio 1):**
  - 1×90 Kurs + 1×90 Kurs + 2×90 Labs = 6h
- **3h SAL1 (Prio 2):**
  - 2×90 TryHackMe (Path/Rooms) = 3h
- **2h Build (Prio 1):** Azure Artefakt der Woche
- **1h Review:** Anki + Summary

#### Azure Security (Prio 1) – Builds

1. **RBAC Rollenmodell v1**
   - 3 Rollen (Reader/Operator/Admin) + Breakglass + Approval Flow
   - Diagramm: “Wer darf was wo?”
   - Evidence: Screenshots/Policy/Role assignments
2. **Azure Policy Pack v1 (light)**
   - 5 Policies (Tagging required, no public IP, secure storage, etc.)
   - Pro Policy: Zweck, Scope, Ausnahmen, Nachweis
3. **Logging/KQL Notebook v1**
   - 20 Queries + 5 Use Cases + Response steps

#### SAL1 (Prio 2) – TryHackMe Reihenfolge (genau dein “Learn → Practice → Simulate”)

**Learn (Core)**

1. **Pre Security (Path)**
2. **Cyber Security 101 (Path)**
3. **SOC Level 1 (Path)**

**Practice (Core)** 4. **Investigating with Splunk (Room)**  
5. **Benign (Room)**  
6. **Secret Recipe (Room)**

**Simulate (Core)** 7. **SOC Simulator** (Szenarien für Exam Prep)

**Milestone Ende Monat 12:** SOC Level 1 Path abgeschlossen + mindestens 2 Practice Rooms + erste Simulator-Szenarien.

---

## Monate 12–18 (Azure Security Engineer)

### Monat 13: **SAL1 Exam Sprint (Prio 2, kurz & kontrolliert)**

> Nur wenn Security+/AZ-104 wirklich fertig sind. Sonst: SAL1 um 4–8 Wochen schieben (bleibt Prio 2).

**Zeit (12h/Woche, nur 4 Wochen):**

- 7–8h Azure Security (Prio 1 weiterführen, nicht abbrechen)
- 3–4h SAL1 (Prio 2): SOC Simulator + Wiederholen schwacher Themen

**Ziel:** SAL1 Certification ablegen + Credly Badge/Proof sauber in CV/LinkedIn.

### Monat 14–18: AZ-500 (Azure Security Engineer) (Prio 1)

- **ACG:** AZ-500 Track + Labs (Key Vault, RBAC, Network Security, Defender, Monitoring)
- **Builds (konkret):**
  - Azure Security Controls Map (Top 10): was/warum/wie/nachweisen
  - Azure IR Mini-Runbooks (3 Szenarien: Creds leaked, storage exposure, suspicious admin change)
  - Detection Notebook v2 (30 Queries/Filters + Tuning Notes)
- **Milestone:** AZ-500 exam-ready/abgelegt

---

## Monate 18–24 (optional nach Zielrolle)

> Wenn du Richtung **Security Architecture / Cloud Security Engineer** willst: mehr Blueprint/GRC.  
> Wenn du Richtung **SecOps/SOC** willst: mehr Tickets/SIEM/SOAR.

**Empfehlung für dich ():**

- 2 Monate GRC (Risk Register + Evidence Pack)
- 2 Monate Capstone “Azure Secure Blueprint”
- Optional: LetsDefend Tickets 3–5/Woche für “Hackerabwehr Vibe” + Praxisstories

---

# 4) CV/LinkedIn – so nutzt du SAL1 fürs “Flexen” ohne cringe

**SAL1 (TryHackMe) – Beispiel-Bullets**

- Completed SOC Level 1 training and virtual SOC simulations; performed alert triage, log analysis, and case closure.
- Investigated anomalies in Splunk; documented evidence, hypotheses, remediation steps, and prevention recommendations.
- Built detection notes (signals, false positives, tuning) and incident mini-runbooks.

**Azure (Prio 1) – Beispiel-Bullets**

- Built RBAC role model and Azure Policy pack; documented controls, exceptions, and evidence for auditability.
- Created KQL notebook with use cases and response steps; improved logging/monitoring coverage.
- Authored firewall/proxy request playbook with least-privilege rules, logging strategy, and rollback plans.
