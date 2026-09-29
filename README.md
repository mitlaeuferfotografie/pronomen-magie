# pronomen-magie

## Hosting & Datenschutz

- **Live-Version:** https://mitlaeuferfotografie.github.io/pronomen-magie/ – jede Änderung auf `main` wird automatisch gebaut und veröffentlicht (`.github/workflows/pages.yml`).
- **Keine externen Dienste:** Tailwind CSS (v3, erzeugt aus `src/tailwind-input.css`); die App nutzt die Systemschrift werden beim Bauen eingebunden und mit der App ausgeliefert. Es gibt keine Verbindungen zu Google Fonts oder dem Tailwind-CDN.
- **Impressum & Datenschutz:** Komponente `ImpressumModal` in `src/App.jsx` (gesamter Rechtstext in einer Komponente, gleicher Text wie in den Schwester-Apps). Erreichbar ohne Passwort über: Fußzeile im Menü („Impressum · Datenschutz“) und Link im Lehrkraft-Login (Zahnrad).

## Das kann ich schon

Über den Knopf **„Das kann ich schon:“** (🎯) sieht jedes Kind, welche Regeln es schon sicher beherrscht – oben in der Leiste alle Bausteine mit den passenden Übungen, in einer Übung und auf dem Ergebnis-Bildschirm nur die Bausteine dieser Übung. Gleiches Schema wie bei den Redezeichen-Helden.

- 6 Bausteine (`SKILLS` in `src/App.jsx`): Pronomen im Text finden (Verborgene Runen) · Pronomen ersetzen Nomen (Hexenkessel, Verwandlungszauber) · Das passende Pronomen einsetzen (Zaubersprüche, Kristall der Wahrheit, Schriftrolle, Feder & Tinte) · Personal- oder Possessivpronomen (Schatztruhen) · Person und Zahl (Raster der Weisen) · Höflichkeitsform (Höflichkeits-Zauber, Schlosstore)
- Es zählt nur der **erste Versuch** pro Aufgabe. Schriftrolle und Feder & Tinte: beim ersten Prüfen zählt jede Lücke. Kristall der Wahrheit: Bei einer richtig erkannten „Illusion“ entscheidet die erste Reparatur. Schlosstore: jede Entscheidung zählt, ein heruntergefallenes Wort nicht.
- Einstufung aus den letzten 10 Ergebnissen je Baustein: 💪 Kann ich! (ab 90 %) · 🙂 Fast! (ab 70 %) · 🎯 Übe ich noch · 🔍 Noch zu wenig Aufgaben (unter 4).

## Zauber-Code

- **Neues Format, 12 Zeichen** (`XXXX-XXXX-XXXX`): Sterne der 11 Übungen + Stufen der 6 Bausteine + 1 Prüfzeichen gegen Tippfehler (`generateSkillCode` / `parseSkillCode`). O/I/L werden beim Eintippen als 0/1/1 gelesen.
- **Alte 13-stellige Codes** (nur Ziffern) werden weiter gelesen (nur Sterne, „Das kann ich schon“ beginnt dann neu). Bekannte Schwäche des alten Formats: 1 Stern und 10 Sterne sind darin nicht unterscheidbar (beim Laden werden daraus 10) – das neue Format hat diesen Fehler nicht.
- Die Reihenfolge von `GAME_ORDER` und `SKILLS` ist Teil des Formats – nie umsortieren.
