# immutable_backups_ransomware.md

## Ziel

Verstehen, warum **Immutable Backups** der wichtigste Schutz gegen Ransomware sind.

---

## Problem: Klassische Backups

Angreifer mit Admin-Rechten können:

- Backups löschen
- Retention verkürzen
- Vaults kompromittieren

➡️ Backup existiert, ist aber **nicht mehr vertrauenswürdig**.

---

## Immutable Backup – Definition

Ein Backup, das:

- **nicht gelöscht**
- **nicht verändert**
- **nicht überschrieben**
  werden kann – selbst nicht von Admins – für eine definierte Zeit.

---

## Azure-Mechanismen

- **Soft Delete (14+ Tage)**
- **Enhanced Soft Delete**
- **Immutable Vault (Preview/Feature abhängig)**
- **RBAC + Separation of Duties**
- **Customer Managed Keys (CMK)**

---

## Best Practice (Banken/Behörden)

- Getrennter Backup-Admin
- Vault in separatem Subscription/Management Group
- Immutable + GRS
- Regelmäßige Restore-Tests

---

## Merksatz

> Ein Backup, das gelöscht werden kann, ist kein Backup.
