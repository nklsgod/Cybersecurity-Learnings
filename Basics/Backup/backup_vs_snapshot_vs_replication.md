# backup_vs_snapshot_vs_replication.md

## Ziel

Klare Abgrenzung der Begriffe **Replication**, **Snapshot** und **Backup** – inkl. Security- und Ransomware-Relevanz.

---

## Replication

**Zweck:** Hochverfügbarkeit & Business Continuity  
**Charakteristik:**

- (Nahezu) Echtzeit-Synchronisation
- Fokus auf **RTO**, nicht auf Historie
- Änderungen (inkl. Löschen & Verschlüsselung) werden repliziert

**Schützt vor:**

- Hardware-Ausfall
- Zonen-/Region-Ausfall (je nach Setup)

**Schützt NICHT vor:**

- User Error
- Ransomware
- Logischen Fehlern

➡️ **Kein Ersatz für Backup**

---

## Snapshot

**Zweck:** Schneller Zustand zu einem Zeitpunkt  
**Charakteristik:**

- Storage-nah
- Sehr schnell erstellt
- Häufig Teil von Backup-Lösungen

**Vorteile:**

- Schnelle Wiederherstellung
- Geringe Performance-Auswirkung

**Risiken:**

- Oft **nicht offsite**
- Kein automatisches Retention-/Compliance-Konzept

➡️ **Allein nicht revisionssicher**

---

## Backup

**Zweck:** Datenwiederherstellung & Compliance  
**Charakteristik:**

- Zeitbasierte Recovery Points
- Retention-Policies
- Restore-Workflows

**Schützt vor:**

- User Error
- Ransomware
- Datenkorruption
- Compliance-Verstößen

➡️ **Einzige echte Sicherheitskopie**

---

## Merksatz

> Replication = Verfügbarkeit  
> Snapshot = schneller Zwischenstand  
> Backup = Rettungsleine
