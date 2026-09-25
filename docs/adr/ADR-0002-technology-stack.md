# ADR-0002: Technologischer Architekturstack

## Status

Akzeptiert

## Kontext

Open Finance Space soll als moderne, sichere und erweiterbare Finanzsoftware entwickelt werden.

Die technische Grundlage muss:

- wartbar sein
- eine klare Trennung von Verantwortlichkeiten ermöglichen
- lokal und robust arbeiten können
- Sicherheitsanforderungen erfüllen
- zukünftige Erweiterungen ermöglichen
- eine spätere mobile Nutzung auf derselben technischen Grundlage unterstützen

## Entscheidung

Der aktuelle technische Architekturstack wird wie folgt festgelegt:

| Bereich | Entscheidung |
|---|---|
| Frontend | Flutter |
| Core | Rust |
| Datenbank | SQLite |
| Datenhaltung | Local First |
| Architektur | modular |
| Erweiterbarkeit | Plugin-System |
| Kryptografie | etablierte Bibliotheken |
| Plattformstrategie | Desktop zuerst, Mobile vorbereitet |

### Frontend: Flutter

Flutter wird für die Benutzeroberfläche eingesetzt.

Damit sollen insbesondere die beiden vorgesehenen Arbeitsweisen unterstützt werden:

- Classic
- Modern

Die Benutzeroberfläche bleibt dabei vom fachlichen Kern getrennt.

### Core: Rust

Rust bildet den fachlichen und technischen Kern der Anwendung.

Der Core übernimmt insbesondere:

- Geschäftslogik
- Verarbeitung der Finanzobjekte
- zentrale Regeln
- Berechtigungen
- Schnittstellen zur Datenhaltung
- fachliche Prozesse

### Datenbank: SQLite

SQLite wird als lokale Datenbank eingesetzt.

Die Wahl unterstützt den Local-First-Ansatz und ermöglicht eine robuste lokale Datenhaltung ohne zwingende Abhängigkeit von einem zentralen Server.

### Local First

Die Daten gehören grundsätzlich zum lokalen Datenbestand des Nutzers.

Die Anwendung soll auch ohne Cloud-Dienst nutzbar sein.

Cloud-Synchronisation wird nicht als Voraussetzung der Kernfunktionalität betrachtet und kann später als optionale Erweiterung umgesetzt werden.

### Modulare Architektur und Plugin-System

Die Software wird modular aufgebaut.

Ein Plugin-System soll spätere Erweiterungen ermöglichen, ohne den stabilen Kern unnötig zu vergrößern.

### Kryptografie

Für kryptografische Funktionen sollen etablierte und geeignete Bibliotheken verwendet werden. Eigene kryptografische Verfahren werden nicht entwickelt.

### Plattformstrategie

Die Entwicklung startet mit dem Desktop.

Die Architektur wird so ausgelegt, dass eine spätere mobile Version auf derselben technischen Grundlage vorbereitet werden kann.

## Konsequenzen

### Positive Konsequenzen

- klar definierter technischer Ausgangspunkt
- nachvollziehbare Technologieentscheidungen
- lokale und offline-fähige Kernarchitektur
- klare Trennung zwischen Benutzeroberfläche und fachlichem Kern
- gute Voraussetzungen für modulare Erweiterungen
- Vorbereitung auf spätere mobile Nutzung

### Zu berücksichtigende Konsequenzen

- Flutter und Rust erfordern eine klare technische Schnittstelle zwischen UI und Core.
- Das Plugin-System muss kontrolliert entworfen werden, damit die Kernarchitektur nicht unnötig komplex wird.
- Local First erfordert eine sorgfältige Planung von Datenhaltung, Sicherung und späterer Synchronisation.
- Die Desktop-First-Strategie priorisiert zunächst die Desktop-Nutzung.

## Alternativen

Alternative Technologien können für einzelne Erweiterungen oder Integrationen geprüft werden.

Eine Änderung des grundlegenden Architektur-Stacks muss jedoch als eigene Architekturentscheidung dokumentiert werden.
