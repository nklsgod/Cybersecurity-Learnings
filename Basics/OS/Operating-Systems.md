Operating Systems – Überblick

1. Batch Operating Systems (BOS)

Prinzip: Jobs werden stapelweise (Batches) ohne Benutzerinteraktion ausgeführt.
• Fokus: Durchsatz
• Verarbeitung: sequenziell
• Speicher: Jobs in Teilaufgaben zerlegt

Vorteile:
• Effizient für Massendaten
• Geringer Overhead bei ähnlichen Jobs

Nachteile:
• Lange Wartezeiten
• Keine Interaktion

Beispiele: Gehaltsabrechnung, Bank-Backends

⸻

2. Time-Sharing Operating Systems (TOS)

Prinzip: CPU-Zeit wird in Zeitscheiben (Quantum) aufgeteilt (Multitasking).
• Fokus: Reaktionszeit & Fairness
• Scheduling: Round-Robin

Vorteile:
• Geringe Wartezeit
• Viele parallele Tasks (scheinbar)

Nachteile:
• Kontextwechsel-Overhead
• Race Conditions möglich

Beispiele: Windows, Linux, macOS

⸻

3. Distributed Operating Systems (DOS)

Prinzip: Mehrere Rechner arbeiten zusammen wie ein System.
• Keine zentrale Steuerung
• Kommunikation über Netzwerkprotokolle

Vorteile:
• Skalierbar
• Ausfallsicher

Nachteile:
• Hohe Komplexität
• Netzwerkabhängig

Beispiele: Cloud-Systeme, Cluster

⸻

4. Network Operating Systems (NOS)

Prinzip: Zentrales Server-OS verwaltet Ressourcen für Clients.
• Tightly-coupled
• Zentrale Administration

Vorteile:
• Zentrale User- & Rechteverwaltung
• Remote-Login

Nachteile:
• Kostenintensiv
• Single Point of Failure

Beispiele: Windows Server, Linux + LDAP

⸻

5. Real-Time Operating Systems (RTOS)

Prinzip: Prioritätsbasiert, zeitkritisch, deterministisch.
• Event-getrieben
• Deadlines entscheidend

Vorteile:
• Garantierte Reaktionszeiten
• Hohe Zuverlässigkeit

Nachteile:
• Stark spezialisiert
• Wenig flexibel

Beispiele: Embedded Systems, autonome Fahrzeuge

⸻

Merkhilfe (Kurzvergleich)
• BOS: Massendaten
• TOS: Interaktiv & fair
• DOS: Verteilt rechnen
• NOS: Netzwerk verwalten
• RTOS: Deadlines einhalten
