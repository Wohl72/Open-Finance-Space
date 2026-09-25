# Open Finance Space

## Projektidee

Open Finance Space soll keine möglichst große Finanzsoftware werden.

Ziel ist eine verständliche, modulare Finanzzentrale, die Finanzinformationen zusammenführt, Zusammenhänge herstellt und dem Nutzer Arbeit abnimmt, ohne ihn mit Funktionen oder Komplexität zu überfordern.

Der konkrete Nutzen für den Nutzer steht dabei vor der Anzahl der Funktionen.

## Grundprinzipien

- **Nutzen vor Funktionen** – jede Funktion benötigt einen konkreten Nutzen.
- **Einfach vor komplex** – die grundlegenden Aufgaben sollen verständlich bleiben.
- **Progressive Komplexität** – zusätzliche Möglichkeiten werden erst sichtbar, wenn sie benötigt werden.
- **Beziehungen statt Inseln** – Finanzinformationen sollen sinnvoll miteinander verbunden werden.
- **Orientierung statt Funktionssammlung** – jede Ansicht soll einen klaren Zweck und einen nachvollziehbaren nächsten Schritt haben.
- **Nutzerkontrolle** – der Nutzer entscheidet, wie Informationen dargestellt und gruppiert werden.
- **Modulare Entwicklung** – neue Bereiche werden gezielt und kontrolliert ergänzt.

## Finanzquelle als Ausgangspunkt

Die Finanzquelle ist der zentrale Ausgangspunkt des Finanzmodells.

Unterstützt werden sollen unter anderem Girokonten, Tages- und Sparkonten, Kreditkartenkonten, Depot- und Anlagekonten sowie weitere Finanzkonten. Fremdwährungskonten und weitere Finanzquellen können später ergänzt werden.

Private und geschäftliche Finanzquellen können parallel geführt werden. Die Darstellung und Gruppierung soll der Nutzer selbst bestimmen können.

## Verbundene Finanzinformationen

Finanzobjekte sollen nicht als isolierte Dateninseln behandelt werden. Das Modell berücksichtigt unter anderem Finanzquelle, Umsatz, Zahlung, Vertrag, Dokument, Kontakt, Aufgabe, Termin und Kategorie.

Beziehungen sollen soweit möglich automatisch unterstützt werden, ohne den Nutzer zu unnötiger manueller Pflege zu zwingen.

## Benutzeroberfläche

Open Finance Space unterstützt zwei Arbeitsweisen:

- **Classic** – traditionelle Navigation und vertraute Strukturen.
- **Modern** – kontextbezogene, übersichtliche und kartenorientierte Darstellung.

Beide Varianten basieren auf demselben technischen Kern.

## V1-Fokus

Die erste stabile Version konzentriert sich auf Finanzquellen und Konten, Finanzübersicht, Umsatzverwaltung, Überweisungen, Dokumente, Verträge, Suche, Datensicherung und lokale Datenspeicherung.

Weitere Bereiche werden erst nach fachlicher und technischer Prüfung aufgenommen.

## Local First

Die Daten sollen grundsätzlich lokal beim Nutzer liegen. Ziele sind Kontrolle über die eigenen Daten, Datenschutz, Offline-Fähigkeit, Unabhängigkeit von einer Cloud und robuste lokale Speicherung.

Cloud-Synchronisation und weitere Online-Funktionen können später ergänzt werden, sind aber keine Voraussetzung für die grundlegende Nutzung.

## Barrierefreiheit und neue Interaktion

Die Software soll schrittweise zugänglicher werden. Geplante Möglichkeiten sind unter anderem optionale Sprachausgabe, Vorlesen neuer Umsätze, Sprachsteuerung und kontextbezogene sprachliche Unterstützung für normale Softwarefunktionen.

Diese Funktionen sind optional und keine Voraussetzung für die normale Bedienung.

## KI

KI ist ein optionales Erweiterungsmodul und keine Grundlage der Software. Mögliche spätere Einsatzbereiche sind Sprachsteuerung, Analyse, intelligente Suche, Erkennung und Klassifikation, Unterstützung bei wiederkehrenden Aufgaben und Automatisierung.

Die Kernsoftware soll vollständig ohne KI nutzbar sein.

## Technische Architektur

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

Die Architektur soll eine spätere mobile Nutzung auf derselben technischen Grundlage ermöglichen.

## Entwicklung

Neue Ideen werden vor der Aufnahme in die Entwicklung geprüft:

1. Welches Problem wird gelöst?
2. Welcher konkrete Nutzen entsteht?
3. Passt die Idee zur Projektphilosophie?
4. Ist sie technisch umsetzbar?
5. Ist sie wirtschaftlich sinnvoll?
6. Welche Abhängigkeiten und Risiken bestehen?
7. Vereinfacht oder verkompliziert sie die Software?

Zentrale Entscheidungen werden als Architecture Decision Records (ADR) dokumentiert.

## Dokumentation

Die technische und fachliche Dokumentation befindet sich im Ordner `docs`.

## Aktueller nächster fachlicher Schritt

Als Grundlage für die weitere Entwicklung wird zunächst das Core-Datenmodell der **Finanzquelle** endgültig definiert.

Dabei werden insbesondere Eigenschaften einer Finanzquelle, Kontotypen, Einzel-, Gemeinschafts- und Geschäftskonten, Eigentümer- und Inhabermodell, Benutzerbeziehungen, Währungen, Salden, Umsätze, Berechtigungen, Darstellung und Gruppierung, mögliche Aktionen, Bankanbindung und spätere Erweiterungspunkte betrachtet.
