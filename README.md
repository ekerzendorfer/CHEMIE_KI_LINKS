# CHEMIE_KI_LINKS – Version 1.4.0

Stand: 13. Oktober 2026

## Enthaltene Ersatzdateien

- `index.html`
- `editor_tools.html`
- `data/tools.json`

## Installation in GitHub

1. Im Repository `CHEMIE_KI_LINKS` die bestehende `index.html` ersetzen.
2. Die bestehende `editor_tools.html` ersetzen beziehungsweise neu hochladen.
3. Im Ordner `data` die bestehende `tools.json` ersetzen.
4. Die vorhandenen Thumbnail-Dateien unter `assets/thumbs/` unverändert lassen.
5. Änderungen committen und GitHub Pages anschließend mit `Strg + F5` neu laden.

## Neu in Version 1.4.0

### Digitales Analytiklabor als Leitprojekt

Das **Digitale Analytiklabor** wird auf der Startseite bewusst außerhalb der normalen Werkzeugkacheln hervorgehoben.

- kompakte gemeinsame Einstiegszeile direkt unter dem Kopfbereich
- links: Prozessgrafik „Unbekannte Probe → Trennen → Analysieren → Beweiskette“
- direkter Einstieg in den Analytik-Hub
- zusätzlicher Link zur Konzeptseite im Onlinekurs
- rechts: kompakterer Bereichsfilter mit kleineren Schaltflächen
- auf schmalen Bildschirmen stapeln sich Leitprojekt und Bereiche responsiv untereinander

Grafik:
`assets/featured/analytiklabor_spotlight.webp`

Das Analytiklabor bleibt damit als vernetztes Gesamtsystem sichtbar, ohne als weitere Einzelkachel in der Werkzeugliste unterzugehen.

## Neu in Version 1.3.0

### Bereich „NEU & AKTUELL“

- zusätzlicher Ein-Klick-Button direkt nach `ALLES`
- zeigt nur Einträge mit `"featured": true`
- sortiert diese nach `updated` absteigend
- gekennzeichnete Karten erhalten ein dezentes Badge `NEU & AKTUELL`
- Suche und Schulstufenfilter funktionieren auch innerhalb dieser Auswahl

Vorläufig ausgewählt sind:

- MESSWERT_LAB
- TITRATIONSTOOL
- VIRTUELLES PHOTOMETER
- KI-STRUKTURMODELL-LAB
- DESTILLATIONSLABOR
- MOL_LAB DIDACTIC

Die Auswahl und die Datumsangaben können jederzeit im Editor geändert werden.

### Neuer Werkzeugdaten-Editor

Der Link `JSON-Editor` befindet sich unauffällig im Fußbereich des Portals. Der Editor unterstützt:

- bestehende `data/tools.json` automatisch laden
- alternativ eine lokale JSON-Datei öffnen
- Einträge anlegen, bearbeiten, duplizieren und löschen
- Reihenfolge mit `Nach oben` und `Nach unten` verändern
- feste Auswahl der fünf Bereiche
- Schulstufen `SEK I`, `SEK II` und `SEK I–II`
- maximal drei Suchstichwörter
- Thumbnail-Pfad
- Kennzeichnung `NEU & AKTUELL`
- Datum der letzten relevanten Aktualisierung
- Vorschau des Eintrags und des Vorschaubildes
- Validierung von Pflichtfeldern, URLs und eindeutigen IDs
- Download einer neu erzeugten `tools.json`

## Arbeitsablauf mit dem Editor

1. Portal öffnen und im Fußbereich `JSON-Editor` anklicken.
2. Eintrag links auswählen und im Formular bearbeiten.
3. `Änderungen übernehmen` anklicken.
4. Nach Abschluss `tools.json herunterladen` wählen.
5. Im GitHub-Repository die Datei `data/tools.json` durch die heruntergeladene Datei ersetzen.
6. Neue Vorschaubilder separat in `assets/thumbs/` hochladen.

Der Editor schreibt aus Sicherheitsgründen nicht direkt in das GitHub-Repository. Er erzeugt ausschließlich eine neue JSON-Datei zum manuellen Hochladen.

## Datenfelder für „NEU & AKTUELL“

Beispiel:

```json
"featured": true,
"updated": "2026-08-03"
```

- `featured: true` nimmt den Eintrag in die Auswahl auf.
- `updated` bestimmt dort die Reihenfolge.
- Ohne Kennzeichnung bleibt `featured` auf `false`.

## Weiterhin gültig

- Der frühere öffentliche Bereich `LINKS / QUELLEN` bleibt entfernt.
- `data/links_list.json` wird nicht mehr geladen.
- Sprachfilter, Tag-Wolke, Debug-Schaltfläche und alter Linkeditor bleiben aus der öffentlichen Oberfläche entfernt.
- Fehlende oder defekte Vorschaubilder werden durch einen neutralen Platzhalter ersetzt.

## Noch fehlende Vorschaubilder

Derzeit betrifft das insbesondere:

- MESSWERT_LAB
- VIRTUELLES PHOTOMETER
- KI-STRUKTURMODELL-LAB
- DESTILLATIONSLABOR
- MOL_LAB DIDACTIC
- MOLLAB PRO
- IONENFISCHEN
- CHEMSNAKE
