# RFSU Godex — extern webbplats

Detta är den publika presentationsytan för RFSU Godex. Webbplatsen är avsiktligt separerad från den dokumentbaserade samarbetsytan i repositoryt.

## Deployment

Vercel-konfiguration:

- Project root: `site`
- Framework preset: `Other`
- Build command: lämnas tom
- Output directory: lämnas tom
- Production branch: `main`

`vercel.json` innehåller grundläggande headers och clean URLs. Vid Git-integration ska varje push till `main` skapa en ny deployment.

## UX-principer

- snabb orientering före dokumentdjup
- uppdragslogiken framgår utan GitHub-kunskap
- vårdrealiseringsresan används som narrativ ryggrad
- startpaletten presenteras som preliminär, inte som redan beslutat urval
- extern yta skiljs tydligt från RFSU:s officiella webbplats
- responsiv navigering och tillgänglig semantik

## Filer

- `index.html` — innehåll och semantisk struktur
- `styles.css` — visuellt system och responsivitet
- `app.js` — mobilnavigation och lågintensiv reveal
- `vercel.json` — Vercel-konfiguration
