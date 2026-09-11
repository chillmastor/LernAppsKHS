# Smartboard & Hauptschul-Didaktik Richtlinien (chillmastor/LernAppsKHS)

## Pflicht-Standards für jede Lern-App:
1. **Technologie**: Nur HTML5 + Tailwind CSS (CDN) + Vanilla JS. Keine Build-Tools. Vercel-kompatibel.
2. **Fernlesbarkeit**:
   - Überschriften: `text-3xl` bis `text-5xl`.
   - Fließtext & Antwortoptionen: mindestens `text-xl` bis `text-2xl`.
   - Keine kleinen Texte (`text-xs`/`text-sm` nur für unwichtige Metadaten).
3. **Touch-Optimierung**:
   - Buttons mindestens `p-4` (Klickfläche min. 48px hoch).
4. **Smartboard-Timer oben**:
   - In jeder App oben fixiert: Zeitanzeige mit Schnellauswahl (3m, 5m, 10m), Start/Pause/Reset und Gong bei Ablauf.
5. **Didaktik**:
   - 4-5 Phasen: Einstieg -> Klick-Aufdecken der Regeln -> Radar/Modell -> Gemeinsame Übungsfälle (3-5) mit didaktischem Feedback und Konfetti.
6. **Zentrales Portal**:
   - Jede neue App MUSS in `index.html` verlinkt werden.
   - Jede neue App MUSS einen Zurück-Button `← Dashboard` zu `index.html` besitzen.
7. **Versionierung**:
   - Version in `package.json` erhöhen und Git-Commit durchführen.
