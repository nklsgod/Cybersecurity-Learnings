# bcdr_design_kfw_szenario.md

## Ziel

BCDR-Grunddesign für ein reguliertes Umfeld (Bank / KfW-nah).

---

## Anforderungen

- Hohe Verfügbarkeit
- Schutz vor User Error & Ransomware
- Audit- & Compliance-Fähigkeit
- Klare RTO / RPO Definition

---

## Architektur-Bausteine

### Verfügbarkeit

- Availability Zones
- Load Balancer
- Replication (z. B. SQL, Storage)

### Disaster Recovery

- Azure Site Recovery
- Region Failover
- Niedriges RTO für kritische Systeme

### Backup

- Azure Backup (Recovery Services Vault)
- GRS oder ZRS
- Immutable / Soft Delete

---

## Beispiel-Klassifizierung

| System           | RPO     | RTO     | Lösung                 |
| ---------------- | ------- | ------- | ---------------------- |
| Active Directory | Minuten | Minuten | Replication + Backup   |
| Kernanwendung    | 15 Min  | < 1h    | Site Recovery + Backup |
| Archivdaten      | 24h     | 24h     | Backup only            |

---

## Typische Prüfungs-/Interviewfrage

**Warum nicht nur Site Recovery?**  
→ Weil SR **keine Historie** bietet und logische Fehler repliziert.

---

## Merksatz

> Availability hält Systeme am Laufen.  
> Backup rettet Daten.  
> BCDR verbindet beides.
