# 🎒 LernApps KHS

> **Interaktive Mini-Lern-Apps für den Frontal- und Plenumsunterricht an einer Hauptschule.**  
> Optimiert für den Einsatz auf dem **Lehrkraft-iPad** mit Bildspiegelung ans **Smartboard / Whiteboard**.

[![Live Demo](https://img.shields.io/badge/🚀_Live_App-Hier_starten-22c55e?style=for-the-badge&logo=google-chrome&logoColor=white)](https://chillmastor.github.io/LernAppsKHS/)
[![Tailwind CSS](https://img.shields.io/badge/Styling-Tailwind%20CSS%20CDN-38bdf8?style=flat&logo=tailwindcss)](https://tailwindcss.com)
[![Vanilla JS](https://img.shields.io/badge/Logic-Vanilla%20JS-F7DF1E?style=flat&logo=javascript)](https://developer.mozilla.org)
[![Version](https://img.shields.io/badge/Version-1.1.0-indigo)](package.json)

> ### 🌐 **Direkter Link zur Live-App:**  
> 👉 **[https://chillmastor.github.io/LernAppsKHS/](https://chillmastor.github.io/LernAppsKHS/)**  
> *(Keine Installation nötig – läuft direkt auf dem Lehrkraft-Tablet, Smartboard oder PC!)*

---

## 🎯 Didaktisches Konzept & Einsatzszenario

Die Apps in diesem Repository sind speziell für den Unterrichtsalltag an der **Hauptschule (Klassenstufen 5 bis 10)** konzipiert:

* **Nutzung im Plenum:** Die Lehrkraft (oder ein moderierendes Kind) steuert die App über das Tablet. Die Klasse interagiert mündlich (Vorlesen, Melden, Begründen, gemeinsame Lösungsfindung).
* **Fernlesbarkeit aus der letzten Reihe:** Große Schriftgrößen (`text-3xl` bis `text-5xl` für Überschriften, min. `text-xl` bis `text-2xl` für Fließtext und Optionen).
* **Touch-Optimierung:** Große Buttons und Klickflächen (min. `p-4`), die sich problemlos mit dem Finger oder dem Smartboard-Stift bedienen lassen.
* **Integrierter & einklappbarer Smartboard-Timer:** Jede App verfügt über eine schlanke Zeitanzeige mit Schnellauswahl (3 Min, 5 Min, 10 Min), Pause-Funktion und Signal bei Ablauf. Mit einem Klick auf `▲ Schrumpfen` lässt sich der Header auf eine Minimalleiste reduzieren, um maximalen vertikalen Platz am Smartboard zu bieten.
* **Sprachsensibilität:** Kurze, verständliche Hauptsätze, Signalwort-Farbcodierungen und visuelle Erklärungen vor Fachbegriffen.
* **Präsentationscharakter (4–5 Phasen):**
  1. *Aktivierung / Vorwissen:* Motivierender Einstiegsimpuls mit Alltagsbezug.
  2. *Regelerarbeitung:* Schrittweises Aufdecken von Regeln und Strategien per Klick.
  3. *Werkzeug / Radar:* Visuelle Signalwort- oder Zahlenstrahlübersicht.
  4. *Gemeinsame Übungsfälle:* 3 bis 5 interaktive Beispiele mit sofortigem visuellem Feedback (grün / sanftes rot mit Erklärung) und Feiereffekten (Konfetti).

---

## 📂 Vorhandene Lern-Apps & Direktlinks

| App / Datei | Fach | Klassenstufe | Live-Link & Kurzbeschreibung |
| :--- | :--- | :--- | :--- |
| **[`index.html`](index.html)** | Übergreifend | Alle | 🔗 **[Dashboard live öffnen](https://chillmastor.github.io/LernAppsKHS/index.html)**<br>Zentrales Portal mit Timer, Filtern, Vollbild & Modulkacheln. |
| **[`textaufgaben.html`](textaufgaben.html)** | Mathematik | Klasse 6 (~20 Min) | 🔗 **[Textaufgaben live starten](https://chillmastor.github.io/LernAppsKHS/textaufgaben.html)**<br>4-Schritte-Methode, Signalwort-Radar, interaktiver Textmarker & 3 Kriminalfälle. |
| **[`runden.html`](runden.html)** | Mathematik | Klasse 5/6 (~15 Min) | 🔗 **[Clever Runden live starten](https://chillmastor.github.io/LernAppsKHS/runden.html)**<br>Supermarkt-Kassensturz, 0–4 & 5–9 Regel, Euro-Zahlenstrahl mit Schieberegler & 4 Fälle. |
| *In Vorbereitung* | Mathematik | Klasse 6 | **Brüche visualisieren:** Interaktive Pizza- und Schokomodelle für Zähler und Nenner. |

---

## 🛠️ Technische Architektur

* **Kein Build-Step erforderlich:** Reines HTML5, Tailwind CSS via CDN, Tone.js für Soundeffekte und Canvas-Confetti für Animationen.
* **Vercel-Ready:** Änderungen in `index.html` oder neuen `.html`-Dateien sind nach dem Git-Push sofort live auf Vercel verfügbar.
* **Modulare Struktur:** Jeder Unterrichts-Input liegt als eigenständige HTML-Datei im Stammverzeichnis oder in Unterordnern und ist in `index.html` verlinkt.

---

## 🚀 Lokale Entwicklung

Zum lokalen Testen reicht ein beliebiger statischer Webserver:

```bash
# Mit Python:
python -m http.server 8080

# Oder mit Node / npx:
npx serve .
```

Anschließend im Browser öffnen: `http://localhost:8080`

---

## 📋 Neue Mini-App hinzufügen (Kurzanleitung)

1. Erstelle eine neue HTML-Datei (z. B. `runden.html`).
2. Kopiere die Grundstruktur aus `textaufgaben.html` (Smartboard-Header mit Timer, Fernlesbarkeits-Klassen, Audio & Confetti).
3. Binde die App in `index.html` als neue Kachel ein.
4. Erhöhe die Versionsnummer in `package.json` und im Metatag.
5. Committe und pushe die Änderungen.

---

## 📄 Lizenz
MIT License • Entwickelt für den modernen Unterricht an Hauptschulen.
