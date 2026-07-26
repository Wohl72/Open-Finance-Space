# Development Guide

## Zweck

Dieses Dokument beschreibt die Entwicklungsprozesse von Open Finance Space.

Ziel ist eine nachvollziehbare, sichere und strukturierte Softwareentwicklung.

## Entwicklungsprinzipien

Die Entwicklung folgt diesen Grundsätzen:

- kleine und nachvollziehbare Änderungen
- Dokumentation wichtiger Entscheidungen
- saubere Versionskontrolle
- automatisierte Tests, wenn möglich
- Qualität vor Geschwindigkeit

## Versionskontrolle

Das Projekt verwendet Git zur Versionsverwaltung.

Änderungen werden über Commits nachvollziehbar dokumentiert.

## Branch-Strategie

Die Entwicklung erfolgt strukturiert über Branches.

Grundsätzlich:

- Hauptzweig für stabile Versionen
- separate Branches für neue Funktionen und Änderungen
- Pull Requests zur Überprüfung größerer Änderungen

## Entwicklungsablauf

Änderungen werden nach folgendem Ablauf durchgeführt:

1. Änderung planen
2. Umsetzung in einem separaten Branch durchführen
3. Änderungen überprüfen
4. Tests durchführen
5. Änderung in den Hauptzweig übernehmen

## Commit-Regeln

Commits sollen:

- eine klare Beschreibung der Änderung enthalten
- eine nachvollziehbare Einheit bilden
- keine unfertigen Änderungen enthalten

Beispiele:

- Dokumentation: Architekturübersicht erweitern
- Feature: Benutzerverwaltung hinzufügen
- Fix: Fehler bei Datenverarbeitung beheben

## Code-Review

Größere Änderungen sollen vor der Übernahme geprüft werden.

Dabei werden insbesondere betrachtet:

- Funktionalität
- Sicherheit
- Wartbarkeit
- Auswirkungen auf bestehende Komponenten

## Code-Qualität

Der Quellcode soll:

- verständlich
- wartbar
- dokumentiert
- sicher

sein.

## Tests

Neue Funktionen sollen durch geeignete Tests abgesichert werden.

Fehler werden dokumentiert und nachvollziehbar behoben.
