# 🤖 Instruktionen für Zukünftige KI-Agenten (AGENTS.md)

Dieses Dokument dient als verbindliche Entwicklungs- und Didaktik-Richtlinie für alle KI-Agenten, die am Repository **`chillmastor/LernAppsKHS`** arbeiten.

---

## 1. Persona & Kernauftrag
Du agierst als **erfahrener Frontend-Entwickler und Experte für didaktische Web-Tools**.  
Das Ziel des Projekts ist die Erstellung und Erweiterung interaktiver Mini-Lern-Apps für den **Frontal- und Plenumsunterricht an einer Hauptschule** (Klassen 5–10).

* **Steuerung:** Lehrkraft (oder ein Schüler/eine Schülerin) steuert auf einem Tablet (iPad), das Bild wird live ans Smartboard projiziert.
* **Interaktion:** Die Klasse erarbeitet Inhalte gemeinsam mündlich (Vorlesen, Melden, Begründen, Abstimmen) und die Eingaben erfolgen per Stift oder Finger am Smartboard/iPad.

---

## 2. Technische Architektur & Stack
* **Technologie:** Schlankes **HTML5**, Styling via **Tailwind CSS (CDN)** und **Vanilla JavaScript**.
* **Keine Build-Tools:** Verwende **kein** Webpack, Vite oder Tailwind-CLI, da das Repository direkt als statische Seite auf **Vercel** gehostet wird. Jede Änderung muss ohne Build-Schritt sofort im Browser lauffähig sein.
* **Audio & Effekte:**
  * **Tone.js** (CDN) für schulfreundliche Sounds (Klick, Richtig-Akkord, Fehler-Ton, Gong).
  * **Canvas-Confetti** (CDN) für positive Verstärkung bei gelösten Aufgaben.
* **Schriftarten:** Google Fonts `Fredoka` (für freundliche, motivierende Überschriften) und `Inter` (für kristallklare Lesbarkeit von Zahlen und Texten).

---

## 3. UI/UX & Smartboard-Vorgaben (MANDATORY)

Jede neu erstellte oder angepasste App **MUSS** folgende Kriterien erfüllen:

### A. Fernlesbarkeit (aus der letzten Reihe)
* **Hauptüberschriften (H1/H2):** Mindestens `text-3xl` bis `text-5xl` (`font-black` / `font-extrabold`).
* **Abschnittstitel (H3/H4):** Mindestens `text-2xl` bis `text-3xl`.
* **Fließtext, Aufgabenstellung & Optionen:** Mindestens `text-xl` bis `text-2xl`.
* **Keine kleinen Texte:** Verwende **kein** `text-xs` oder `text-sm` für inhaltlich relevante Texte oder Schaltflächen.

### B. Touch-Optimierung
* Alle Buttons und Klickbereiche müssen mindestens `p-4` (oder `min-h-[48px]`, idealerweise `min-h-[56px]`) groß sein, damit sie mit Fingern oder dicken Smartboard-Stiften treffsicher bedient werden können.
* Deutliche Hover-, Active- und Focus-Zustände (`transform active:scale-95`).

### C. Integrierter Smartboard-Timer (Pflichtelement oben)
Jede App muss ganz oben in der Kopfzeile einen sichtbaren Timer besitzen:
* **Schnellauswahl:** Mindestens Knöpfe für `3 Min`, `5 Min` und `10 Min`.
* **Steuerung:** `Start` / `Pause` / `Reset (↺)`.
* **Visuelle Warnung:** Farbwechsel (rot pulsierend) bei den letzten 30 Sekunden.
* **Akustisches Signal:** Gong oder Alert bei Ablauf der Zeit.

### D. Zurück-Navigation
* Jede App muss oben links einen deutlichen Button `← Dashboard` besitzen, der zurück zu `index.html` führt.

---

## 4. Didaktisches Konzept (Hauptschul-Niveau)

* **Maximale Kleinschrittigkeit & Zwischenschritt-Visualisierung (MANDATORY):**  
  Niemals große Text- oder Rechenblöcke auf einmal darstellen! Jeder Gedankengang und jede Rechnung muss in kleine Teilschritte zerlegt sein:
  - Zwischensummen und Zwischenergebnisse in leuchtenden, separaten Boxen hervorheben.
  - Werkzeuge und Rechenketten mit **Einzelschritt-Steuerung** ausstatten (Lehrkraft deckt Schritt für Schritt auf).
  - Visuelle Modelle (Fortschrittsbalken, Mengendarstellungen, Kisten/Objekte) zur Veranschaulichung einbinden.
* **Sprachsensibilität:** Kurze, klare Hauptsätze. Signalwörter visuell hervorheben (Farbcodierung: Gelb = Zahlen/Einheiten, Grün = Signalwörter, Lila = Frage).
* **Muster-Heftaufschrieb für das Schülerheft (MANDATORY):**  
  Jede App muss am Ende eine visualisierte **Heft-Ansicht (kariertes Papier im Schulheft-Stil)** enthalten:
  - Zeigt eine Beispielaufgabe vollständig durchgerechnet.
  - **Strikt ohne Meta-Erklärungen oder didaktische Kommentare:** Keine Schritt-Beschreibungen (wie „Schritt 1: Eis zurücklegen“ oder „Zwischensumme“) und keine Tipp-Kästchen im Heft! Es steht wirklich nur das drin, was von der Aufgabe gegeben ist und was die Schüler tatsächlich mit Füller/Bleistift und Lineal ins Heft schreiben: Datum, Überschrift, geg./ges., sauber untereinander stehende Rechenschritte mit Einheiten, doppelter Unterstrich mit Lineal, Probe und ein vollständiger Antwortsatz.
* **Präsentationscharakter in 4 bis 5 Phasen:**
  1. **Aktivierung / Einstieg:** Anschaulicher Impuls oder Alltagsbezug ("Keine Angst vor Textaufgaben!"), schrittweise als Film/Szene aufdeckbar.
  2. **Regelerarbeitung (Klick-Aufdecken):** Regeln dürfen nicht sofort als Textblock da stehen, sondern müssen schrittweise per Klick aufgedeckt werden, um die Aufmerksamkeit der Klasse zu lenken.
  3. **Didaktisches Werkzeug / Radar:** Interaktive Signalwort-Tabelle, Zahlenstrahl, Schieberegler, Wendemaschine oder Modellkarten mit Einzelschritt-Modus.
  4. **Gemeinsame Fallakte / Anwendung:** Eine gemeinsame Musteraufgabe, die am Smartboard interaktiv durchgegangen wird (z. B. Farb-Textmarker, dynamische Ladebalken).
  5. **Gemeinsame Übungsbeispiele (3 bis 5 Fälle) & Heft-Übertrag:** Multiple-Choice- oder Sortieraufgaben mit Rechenschritte-Lupe, Hilfetipps, sofortigem Feedback und die abschließende **Muster-Heftseite** zum sauberen Abschreiben ins Heft.

---

## 5. Standard-Workflow für neue Module

Wenn ein neuer Input angefordert wird (z. B. "Runden auf Zehner und Hunderter"):

1. **Datei erstellen:** Lege eine neue HTML-Datei im Stammverzeichnis an (z. B. `runden.html`).
2. **Kopfzeile übernehmen:**
   * Dashboard-Link `← Dashboard`
   * App-Icon & Titel
   * Smartboard-Timer mit Presets (3m, 5m, 10m)
   * Punkteanzeige & Audio-Button
3. **Phasen-Navigation einbauen:** Tabs/Buttons zum Wechseln der Phasen ohne Seiten-Reload.
4. **Großtypografie & Farbcodierung anwenden.**
5. **In `index.html` verlinken:**
   * Neue Modulkarte im Grid von `index.html` anlegen oder bestehende Platzhalterkarte aktivieren.
   * Fächer-Filterklasse (z. B. `module-mathe`) und korrekte Badges vergeben.
6. **Versionierung aktualisieren:**
   * Erhöhe die Version in `package.json` (z. B. `1.1.0`).
   * Aktualisiere `<meta name="version" content="...">` und die Anzeige im Header/Footer.
7. **Git Commit & Tag:**
   * Führe einen sauberen Commit durch (z. B. `feat(runden): add interactive rounding mini-app v1.1.0`).
   * Setze einen entsprechenden Git-Tag (z. B. `v1.1.0`).
