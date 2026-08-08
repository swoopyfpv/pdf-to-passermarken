# Passermarke — PDF drucken, wenn die schwarze Patrone leer ist

### 🖨️ **[→ Tool direkt im Browser öffnen](https://swoopyfpv.github.io/pdf-to-passermarken/)**

![KI CODE](https://img.shields.io/badge/KI%20CODE-Nutzung%20auf%20eigene%20Verantwortung-orange)

Schwarze Druckerpatrone leer, aber das Dokument muss raus? **Passermarke** wandelt Schwarz in einem PDF so um, dass dein Drucker es aus **Cyan, Magenta und Gelb mischt** (CMY-Schwarz) — oder alternativ komplett in **Dunkelblau** druckt.

Kostenlos, ohne Anmeldung, und **100% lokal im Browser**: Kein PDF wird hochgeladen, keine Datenübertragung. Du kannst das Repo auch einfach herunterladen und die `index.html` direkt lokal öffnen — funktioniert komplett offline.

## ⚠️ KI CODE — Hinweis

Dieses Tool wurde **mit KI entwickelt**. Es wird ohne Gewähr bereitgestellt — **Nutzung auf eigene Verantwortung**. Prüfe das umgewandelte PDF vor dem Druck kurz in der Vorher/Nachher-Vorschau. Wer dem Code nicht trauen will: Er ist vollständig einsehbar, hat kein Backend und lässt sich offline ausführen.

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

## Lokal ausführen

```
git clone https://github.com/swoopyfpv/pdf-to-passermarken.git
```
Dann `index.html` im Browser öffnen — kein Build, kein Server nötig.

## Technik

- Statische Seite, kein Backend, keine externen Requests — alle Libraries liegen lokal in `vendor/`
- [pdf.js](https://mozilla.github.io/pdf.js/) 3.11.174 (Rendering) · [jsPDF](https://github.com/parallax/jsPDF) 2.5.1 (PDF-Ausgabe)
- Seiten werden gerastert — der Text im Ausgabe-PDF ist nicht mehr durchsuchbar (für den Druck irrelevant)

## English summary

Free browser tool to **print a PDF when your black ink cartridge is empty**: converts black to composite CMY black (mixed from cyan, magenta and yellow) or to dark blue. Runs 100% client-side — no upload, no tracking. You can also download the repo and run it locally/offline. **AI-generated code — use at your own risk.** [Open the tool.](https://swoopyfpv.github.io/pdf-to-passermarken/)

## Lizenz

MIT. Enthaltene Libraries: pdf.js (Apache-2.0), jsPDF (MIT).
