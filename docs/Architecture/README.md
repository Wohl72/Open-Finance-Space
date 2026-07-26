# Architekturübersicht

## Zweck

Dieses Dokument beschreibt die grundlegende Architektur von Open Finance Space.

Die Architektur soll eine sichere, wartbare und erweiterbare Basis für Finanzsoftware schaffen.

## Architekturprinzipien

Die Entwicklung folgt diesen Grundprinzipien:

- klare Trennung von Verantwortlichkeiten
- sichere Verarbeitung von Finanzdaten
- modulare Erweiterbarkeit
- nachvollziehbare technische Entscheidungen
- API-basierte Kommunikation

## Systemaufbau

Die Anwendung wird in logische Bereiche getrennt:

### Frontend

Verantwortlich für:
- Benutzerinteraktion
- Darstellung von Finanzinformationen
- Eingabe und Validierung von Benutzerdaten

### Backend

Verantwortlich für:
- Geschäftslogik
- Berechtigungen
- Verarbeitung von Finanzprozessen
- Schnittstellen

### Datenhaltung

Verantwortlich für:
- Speicherung von Daten
- Konsistenz
- Sicherung und Wiederherstellung

## Architekturentscheidungen

Wichtige Architekturentscheidungen werden über ADRs dokumentiert.

Siehe:

- ADR-0001 Projektgrundlage Open Finance Space
- ADR-0002 Technologischer Architekturstack
