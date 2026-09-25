# Architekturübersicht

## Zweck

Dieses Dokument beschreibt die aktuelle Zielarchitektur von Open Finance Space.

Die Architektur soll eine sichere, wartbare, verständliche und modular erweiterbare Grundlage für die Finanzsoftware schaffen.

## Architekturprinzipien

Die Entwicklung folgt diesen Grundsätzen:

- klare Trennung von Verantwortlichkeiten
- Finanzquelle als zentraler Ausgangspunkt des Finanzmodells
- Local-First-Datenhaltung
- modulare Erweiterbarkeit
- sichere Verarbeitung von Finanzdaten
- nachvollziehbare technische Entscheidungen
- progressive Komplexität
- Orientierung statt Funktionssammlung

## Technischer Architekturstack

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

## Systemaufbau

### Frontend

Das Frontend wird mit Flutter umgesetzt.

Verantwortlich für:

- Benutzerinteraktion
- Darstellung von Finanzinformationen
- Eingabe und Validierung von Benutzerdaten
- Classic- und Modern-Darstellung
- optionale barrierearme Interaktion

### Core

Der fachliche Kern wird in Rust umgesetzt.

Verantwortlich für:

- Finanzlogik
- Verarbeitung von Finanzobjekten
- Berechtigungen
- Geschäftsregeln
- Schnittstellen zum Datenzugriff
- zentrale und nachvollziehbare Verarbeitung von Finanzprozessen

Die fachliche Logik soll nicht von einer bestimmten Benutzeroberfläche abhängig sein.

### Datenhaltung

SQLite bildet die lokale Datenbasis.

Die Datenhaltung folgt dem Local-First-Prinzip:

- Daten liegen grundsätzlich lokal beim Nutzer.
- Die Anwendung soll auch ohne Cloud-Verbindung nutzbar sein.
- Datenschutz und Kontrolle über die eigenen Daten haben hohe Priorität.
- Cloud-Synchronisation kann später als optionale Erweiterung ergänzt werden.

## Modulare Architektur

Die Architektur ist auf Erweiterbarkeit ausgelegt.

Ein Plugin-System soll später zusätzliche Funktionen und Module ermöglichen, ohne den stabilen Kern unnötig zu verkomplizieren.

Mögliche spätere Erweiterungen sind unter anderem:

- weitere Finanzdienstleister
- Multibanking
- internationale Zahlungswege
- Fremdwährungen
- Business- und ERP-Funktionen
- Wallet- und weitere Finanzmodule
- optionale KI-Funktionen

Nicht jede Erweiterung gehört zur ersten Version.

## Finanzmodell

Die Finanzquelle bildet den zentralen Anker des Finanzmodells.

Weitere Objekte können mit ihr und untereinander verbunden werden, unter anderem:

- Umsatz
- Zahlung
- Vertrag
- Dokument
- Kontakt
- Aufgabe
- Termin
- Kategorie

Das interne Datenmodell darf leistungsfähig sein, während die Benutzeroberfläche einfach und verständlich bleibt.

## Benutzeroberfläche

Open Finance Space unterstützt zwei Darstellungs- und Arbeitsweisen:

### Classic

Traditionelle Navigation und vertraute Strukturen für Nutzer, die eine klassische Finanzsoftware bevorzugen.

### Modern

Kontextbezogene, übersichtliche und kartenorientierte Darstellung.

Beide Varianten verwenden denselben technischen Kern. Der Nutzer soll nicht auf eine bestimmte Arbeitsweise festgelegt werden.

## Prototyp vor Implementierung

Zentrale Benutzeroberflächen sollen zunächst als klickbarer Prototyp entwickelt und geprüft werden.

Dabei werden insbesondere betrachtet:

- Verständlichkeit
- logische Wege
- fehlende Schritte
- Überlastung
- Classic und Modern
- unnötige Komplexität

Erst nach dieser Prüfung soll die technische Implementierung erfolgen.

## Sicherheit

Sicherheitsanforderungen werden von Beginn an berücksichtigt.

Schwerpunkte sind:

- Schutz von Finanzdaten
- minimale Berechtigungen
- sichere lokale Datenhaltung
- Verschlüsselung mit etablierten Bibliotheken
- sichere Schnittstellen
- nachvollziehbare sicherheitsrelevante Aktionen

Details werden in der Sicherheitsdokumentation und den zugehörigen ADRs festgehalten.

## Architekturentscheidungen

Wichtige Architekturentscheidungen werden über Architecture Decision Records dokumentiert.

Aktuell relevante Entscheidungen werden dort schrittweise konsolidiert.

Siehe:

- ADR-0001 Projektgrundlage Open Finance Space
- ADR-0002 Technologischer Architekturstack
- ADR-0003 Sicherheitsarchitektur

Weitere Entscheidungen werden nach der historischen ADR-Konsolidierung ergänzt.
