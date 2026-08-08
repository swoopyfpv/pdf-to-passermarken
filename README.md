# Passermarke — PDF drucken, wenn die schwarze Patrone leer ist

### 🖨️ **[→ Tool direkt im Browser öffnen](https://swoopyfpv.github.io/pdf-to-passermarken/)**

Schwarze Druckerpatrone leer, aber das Dokument muss raus? **Passermarke** wandelt Schwarz in einem PDF so um, dass dein Drucker es aus **Cyan, Magenta und Gelb mischt** (CMY-Schwarz) — oder alternativ komplett in **Dunkelblau** druckt.

Kostenlos, ohne Anmeldung, und **100% lokal im Browser**: Kein PDF wird hochgeladen, keine Datenübertragung, keine Cookies. DSGVO-freundlich by design.

## So funktioniert's

1. **[Tool öffnen](https://swoopyfpv.github.io/pdf-to-passermarken/)** und PDF ablegen
2. Modus wählen:
   - **CMY-Schwarz** — Schwarz wird zu einem minimal getönten Dunkelton. Der Druckertreiber erkennt keine reine Neutralfarbe mehr und mischt aus den drei Farbpatronen. Sieht gedruckt fast wie echtes Schwarz aus.
   - **Blau** — Schwarz wird zu Dunkelblau. Gut lesbar, ehrlicher Look.
3. Umwandeln → herunterladen → drucken

> ⚠️ **Wichtig:** Im Druckdialog **„Farbe"** wählen, nicht „Graustufen" — sonst zwingt der Treiber wieder die (leere) schwarze Patrone. Bei manchen Treibern hilft zusätzlich „Nur Farbtinte verwenden".

## Features

- Vorher/Nachher-Vorschau
- Wählbare Auflösung (150 / 200 / 300 dpi)
- Farbige Inhalte (Logos, Bilder) bleiben auf Wunsch unangetastet — nur Schwarz/Grau wird ersetzt, mit sauberem Antialiasing
- Funktioniert mit mehrseitigen PDFs, Fortschrittsanzeige

## Technik

- Statische Seite, kein Backend, keine externen Requests — alle Libraries liegen lokal in `vendor/`
- [pdf.js](https://mozilla.github.io/pdf.js/) 3.11.174 (Rendering) · [jsPDF](https://github.com/parallax/jsPDF) 2.5.1 (PDF-Ausgabe)
- Seiten werden gerastert — der Text im Ausgabe-PDF ist nicht mehr durchsuchbar (für den Druck irrelevant)
- Läuft auch offline: Repo klonen, `index.html` öffnen, fertig

## English summary

Free browser tool to **print a PDF when your black ink cartridge is empty**: converts black to composite CMY black (mixed from cyan, magenta and yellow) or to dark blue. Runs 100% client-side — no upload, no tracking. [Open the tool.](https://swoopyfpv.github.io/pdf-to-passermarken/)

## Lizenz

MIT. Enthaltene Libraries: pdf.js (Apache-2.0), jsPDF (MIT).
