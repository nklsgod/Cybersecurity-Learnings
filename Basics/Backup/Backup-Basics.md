Backups – Replication, Snapshots & 3-2-1

1. Replication

Definition:
Fortlaufende Spiegelung von Daten auf ein anderes System (nahezu Echtzeit).

Eigenschaften:
• Sehr geringe Datenverluste (RPO ≈ 0)
• Hohe Verfügbarkeit
• Kein klassisches Backup

Vorteile:
• Schnelle Wiederherstellung
• Ideal für Hochverfügbarkeit

Nachteile:
• Fehler/Ransomware werden mit repliziert
• Kein historischer Stand

Beispiel:
Primäre Datenbank → Replik in anderem Rechenzentrum

⸻

2. Snapshots

Definition:
Zeitpunktaufnahme eines Systems oder Dateisystems.

Eigenschaften:
• Sehr schnell erstellt
• Meist platzsparend (Copy-on-Write)
• Kurz- bis mittelfristig

Vorteile:
• Schnelles Rollback
• Gut gegen versehentliches Löschen

Nachteile:
• Oft abhängig vom gleichen Storage
• Kein Schutz bei Totalverlust

Beispiel:
VM-Snapshot vor Update

⸻

3. Backups

Definition:
Separate Kopie der Daten auf ein anderes Medium oder System.

Eigenschaften:
• Historische Datenstände
• Physisch oder logisch getrennt

Vorteile:
• Schutz vor Ransomware
• Schutz vor Hardware- & Standortverlust

Nachteile:
• Langsamere Wiederherstellung
• Speicher- & Verwaltungsaufwand

Beispiel:
Tägliches Cloud-Backup, wöchentlich lokal

⸻

4. Die 3-2-1-Backup-Strategie

Regel:
• 3 Kopien der Daten
• 2 unterschiedliche Medientypen
• 1 Kopie extern / offsite

Ziel:
Maximaler Schutz vor:
• Hardwaredefekt
• Ransomware
• Menschlichem Fehler
• Standortverlust

Praxisbeispiel:
• Originaldaten auf Server
• Lokales NAS-Backup
• Verschlüsseltes Cloud-Backup

⸻

Kurzvergleich

Methode Schutz vor Fehler Schutz vor Ransomware Schutz vor Standortverlust
Replication ❌ ❌ ⚠️
Snapshot ⚠️ ⚠️ ❌
Backup ✅ ✅ ✅

⸻

Merksatz

Replication = Verfügbarkeit
Snapshots = schnelles Zurückspringen
Backups = echte Sicherheit
3-2-1 = professioneller Standard
