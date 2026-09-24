# Wilhelmsburger Gründach-Atlas — Version 6.3

Interaktive Karte zum Gründachbestand und zum Begrünungspotenzial auf der
Elbinsel Wilhelmsburg (Masterthesis, Fabian Schlag).

**Live: siehe GitHub-Pages-Link rechts unter „About".**

Version 5.5 bleibt unter
<https://fabsilonius.github.io/gruendach-atlas-v5/> erreichbar.

## Was in v6 anders ist

- Helle Oberfläche im Farbsystem der Arbeit
- Bestand und Potenzial als einander ausschließende Ebenen, jede einzeln
  abschaltbar
- Potenzialebene auf einzelnen Dachteilflächen statt auf ganzen Gebäuden,
  zusätzlich gefiltert auf Teilflächen, die an mindestens einer Stelle
  2 m breit sind
- Überarbeiteter Kosten- und Wirkungsrechner: Die Kostenspannen beziehen sich
  auf eine Projektgröße von 100 m² und werden auf die tatsächliche Fläche
  umgerechnet — kleinere Dächer sind je m² teurer, größere deutlich billiger
- Der Rechner kennt zwei Bezüge: die angeklickte Dachteilfläche und die Summe
  aller unbegrünten Teilflächen desselben Gebäudes. Nur auf Gebäudeebene greifen
  der Größeneffekt und der Förderhöchstbetrag, der je Gebäude gilt
- Geneigte Dächer erhalten ab 5° einen Zuschlag für die Schubsicherung, und der
  Mengennachlass fällt dort geringer aus als auf dem Flachdach — ein Sheddach
  ist kein großes Flachdach

## Inhalt

| Datei | Beschreibung |
|---|---|
| `index.html` | Die Webanwendung (Leaflet), eine einzige Datei ohne Build-Schritt |
| `data/gruendaecher_2022.geojson` | Belegter Gründachbestand, Jahrgang 2022 |
| `data/gruendaecher_2024.geojson` | Belegter Gründachbestand, Jahrgang 2024 |
| `data/potenzialflaechen.geojson` | Begrünbare Dachteilflächen, Modellstand |
| `data/statistik.json` | Aggregierte Kennzahlen |

## Hinweise zur Nutzung

- Als Hintergrund stehen die Digitalen Orthophotos der Freien und Hansestadt
  Hamburg (Zeitreihe 2022 unbelaubt, 2024 belaubt, 2026 unbelaubt, via WMS
  `geodienste.hamburg.de`) sowie OpenStreetMap zur Verfügung.
- Die Potenzialebene umfasst rund 15.000 Teilflächen und etwa 9 MB; der erste
  Kartenaufbau kann je nach Verbindung einige Sekunden dauern.
- Getestet in aktuellen Versionen von Chrome, Safari und Firefox.

## Zur Belastbarkeit der Zahlen

Der Gründachbestand ist vollständig am Luftbild geprüft — das Modell schlägt
vor, die Aufnahme in den Atlas entscheidet die visuelle Prüfung. Die
Potenzialebene ist reiner Modellstand und **nicht** nachkartiert. Statik,
Dachzustand und Nutzungskonflikte kann das Verfahren nicht beurteilen; eine
als geeignet ausgewiesene Fläche ist ein Hinweis, keine Zusage.

Die Werte des Kostenrechners sind Orientierungswerte. Statik, Planung, Gerüst,
Genehmigung und die Dachabdichtung selbst sind nicht enthalten. Maßgeblich für
die Förderung ist allein die Richtlinie der IFB Hamburg. Der Gebäudebezug ist
die unsicherere der beiden Angaben: Er summiert modellierte Teilflächen und
unterstellt, dass alle tragfähig sind und in einem Zug umgesetzt werden.

Einzelheiten stehen in der Anwendung unter „Datengrundlage und Lesehinweise".

## Datenquellen

Digitale Orthophotos, Dachflächen und Gebäudedaten: Landesbetrieb
Geoinformation und Vermessung (LGV) Hamburg, Datenlizenz Deutschland
Namensnennung 2.0. Kartendarstellung mit Leaflet.
