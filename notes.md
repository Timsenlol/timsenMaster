# Notizen zur Masterarbeit

## 1. Einleitung

### 1.1 Motivation
Dieses Kapitel liefert den "Warum-wir-das-überhaupt-tun"-Grundstein der Arbeit. Es motiviert das Thema über den akuten Schmerzpunkt der Praxis: Steuerberater stehen unter extremem Termindruck, während IT-Ausfälle beim Jahresabschluss sofort existenzbedrohende Schäden (Zwangsgelder, Haftung) nach sich ziehen. Das Kapitel baut die nötige Fallhöhe auf, indem es zeigt, dass fehlerhafte Softwareprozesse hier kein reines Luxusproblem sind, sondern direkte ökonomische Konsequenzen haben – das ist die primäre Triebfeder für die Entwicklung deiner neuen Architektur.

### 1.2 Das Ökosystem moderner Jahresabschluss-Softwarelösungen
Dieses Kapitel beschreibt den softwareseitigen Ist-Zustand in den Kanzleien und beleuchtet die technologische Komplexität der bestehenden Systeme. Es zeigt auf, dass der Jahresabschluss kein isoliertes Einzelprogramm ist, sondern ein hochgradig verzahntes Ökosystem aus interdependenten Modulen (wie Finanzbuchhaltung, Anlagenbuchhaltung und Steuerberechnung). Dem Leser wird verdeutlicht, dass diese Anwendungen wie eine geschlossene, synchrone Prozesskette interagieren müssen – bricht hier datenseitig auch nur ein einziges Glied, kollabiert sofort der gesamte digitale Workflow der Kanzlei.

### 1.3 Technische Herausforderungen der Migration von On-Premises- zu Cloud-Architekturen
Dieses Unterkapitel dient rein als strategischer Problemaufriss aus einer übergeordneten Perspektive. Es benennt den generellen Konflikt, dass im Zuge der Software-Modernisierung bewährte lokale Systeme durch webbasierte Cloud-Strukturen ersetzt werden, was neue Risiken wie Netzwerklatenzen und unvollständige Datentransfers einführt. Es motiviert den Leser auf Makro-Ebene, warum der aktuelle Zustand der Softwarelandschaft unzureichend ist und eine architektonische Lösung erforscht werden muss.
### 1.4 Zielsetzung und Aufbau der Arbeit
Dieses Kapitel definiert das konkrete wissenschaftliche und praktische Ziel deiner Arbeit: Die Konzeption einer stabilen, zukunftssicheren Schnittstellenarchitektur, um den kritischen Prozess des Jahresabschlusses sicher aus der alten On-Premises-Welt in eine dezentrale Cloud-Infrastruktur zu überführen.

## 2. Theoretische und fachliche Grundlagen

### 2.1 Fachliche Grundlagen des Jahresabschlusses
Dieses Kapitel legt das betriebswirtschaftliche und regulatorische Fundament der Arbeit, komplett losgelöst von der späteren technischen Umsetzung. Es beschreibt die gesetzlichen Vorgaben, den logischen Ablauf und die Fristen, die Kanzleien bei der Erstellung eines Jahresabschlusses zwingend einhalten müssen. Dem Leser wird hierdurch verdeutlicht, welche sensiblen Datenmengen (wie Saldenvorträge, Buchungsjournale und Inventardaten) sequentiell verarbeitet werden müssen und warum fachliche Fehler oder unvollständige Datenübertragungen in dieser Phase sofort zu rechtlichen und finanziellen Konsequenzen führen.

### 2.2 Technologischer Paradigmenwechsel: Von On-Premises-Monolithen zu dezentralen Cloud-Strukturen
Dieses Kapitel liefert den tiefgehenden, wissenschaftlichen Beweis für das in Kapitel 1.3 behauptete Problem durch eine formale Gegenüberstellung der Softwaremechanismen. Hier wird im Detail analysiert, wie On-Premises-Monolithen Daten inhärent sicher im selben Arbeitsspeicher (Shared Memory) oder über ACID-Datenbanktransaktionen verarbeiten, und warum diese Sicherheitsmechanismen durch die Zustandslosigkeit (Statelessness) und die Netzkopplung von Microservices technisch brechen. Das Kapitel liefert das theoretische Fundament dafür, warum Datenverlust in der Cloud ohne zusätzliche Muster ein physikalisches Risiko darstellt.

### 2.3 Technologische Konzepte zur Realisierung der Architektur
Dieses Kapitel etabliert die theoretischen Lösungsansätze zur Bewältigung der systemischen Instabilitäten und Latenzen in dezentralen Netzwerkinfrastrukturen. Im Fokus steht die Theorie endlicher Automaten (State Machines) zur deterministischen Prozesssteuerung und Fehlertoleranz sowie nachrichtenorientierte Middleware zur asynchronen Entkopplung und Skalierung der Dienste bei transienten Lastspitzen. Ergänzend wird das Konzept des unidirektionalen Ereignis-Streamings als informationstechnische Grundlage hergeleitet, um eine ressourceneffiziente, echtzeitfähige Statustransparenz für den Endanwender zu gewährleisten.
### 3.1 Ist-Analyse der On-Premises-Steuerschnittstellen im Jahresabschluss
Was hier passiert (Die prozessuale und technische Bestandsaufnahme):
Dieses Unterkapitel seziert die bestehende, lokal installierte Schnittstellenlandschaft zwischen dem Jahresabschluss  und den Steuermodulen. Du platzierst hier deine erweiterten Ereignisgesteuerten Prozessketten (eEPK), um die synchronen Datenflüsse, die monolithische Kopplung und die exakten Zeitpunkte der Datenübergabe visuell und textuell zu dokumentieren.
### 3.2 Definition der Qualitätsziele für die Cloud-Schnittstellenarchitektur
Dieses Unterkapitel formuliert die übergeordneten architektonischen Qualitätsattribute, die das neue Cloud-Schnittstellensystem zwingend erfüllen muss, um den kritischen Jahresabschluss-Prozess sicher zu tragen.
### 3.3 Lastschätzung für die cloudbasierten Schnittstellen
ieses Unterkapitel quantifiziert das zu erwartende Datenvolumen sowie die Peak-Load-Szenarien während der Abschlussphase, um konkrete, numerische Grenzwerte für die notwendige Skalierung und Dimensionierung der Cloud-Infrastruktur abzuleiten.
### 3.4 Funktionale Anwendungsfälle der Cloud-Schnittstelle (Use Cases)
Was hier passiert: Dieses Unterkapitel identifiziert und beschreibt die primären Use Cases sowie die Interaktionen zwischen den Anwendern und den beteiligten Systemen.
### 3.5 Fachlicher und technischer Systemkontext
Dieses Unterkapitel grenzt das neue Cloud-Schnittstellensystem strukturell von seiner Umwelt ab, indem es sowohl die beteiligten fachlichen Akteure als auch die technischen Nachbarsysteme und deren Schnittstellenbeziehungen formal definiert.
## 3.6 Einordnung in die Gesamt-ACS-Kontextmap
### 4.1 Gesamtarchitektur im Überblick
### 4.2 Architektonische Entwurfsentscheidungen (ADRs)
### 4.3 Ablauf der Software (Flussdiagram)
### 4.4 ++   Qulitätsziele auf Architekturmatchen z.b. sowas wie : Deterministische Prozesssteuerung mittels State Machines (Fokus: Resilienz)
### 5. Technische Umsetzung und prototypische Implementierung
### 5.1 Technologiestack und Laufzeitumgebung
### 5.2 Programmtechnische Realisierung der State Machine
### 5.3 Konfiguration und Anbindung der Message Queue
### 5.4 Implementierung des SSE-Streaming-Endpunkts 
### Grundlegende Sicherheitsaspekte
### 6 Evaluation und softwaretechnische Validierung
### 6.1 Testumgebung 
### 6.2 Funktionale Tests
### 6.3 Last- und Performance-Tests
### 6.4 Resilienz- und Ausfalltests
### 7. Zusammenfassung, Einordnung und Fazit
### 7.1 Zusammenfassung der Ergebnisse
### 7.2 Kritische Würdigung und fachliche Einordnung
### 7.3 Fazit und Ausblick