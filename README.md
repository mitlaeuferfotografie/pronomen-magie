# pronomen-magie

## Hosting & Datenschutz

- **Live-Version:** https://mitlaeuferfotografie.github.io/pronomen-magie/ – jede Änderung auf `main` wird automatisch gebaut und veröffentlicht (`.github/workflows/pages.yml`).
- **Keine externen Dienste:** Tailwind CSS (v3, erzeugt aus `src/tailwind-input.css`); die App nutzt die Systemschrift werden beim Bauen eingebunden und mit der App ausgeliefert. Es gibt keine Verbindungen zu Google Fonts oder dem Tailwind-CDN.
- **Impressum & Datenschutz:** Komponente `ImpressumModal` in `src/App.jsx` (gesamter Rechtstext in einer Komponente, gleicher Text wie in den Schwester-Apps). Erreichbar ohne Passwort über: Fußzeile im Menü („Impressum · Datenschutz“) und Link im Lehrkraft-Login (Zahnrad).
