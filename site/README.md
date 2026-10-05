# RFSU Godex — extern webbplats

Detta är den publika presentationsytan för RFSU Godex. Webbplatsen är avsiktligt separerad från den dokumentbaserade samarbetsytan i repositoryt.

## Deployment

Vercel-konfiguration:

- Project root: `site`
- Framework preset: `Other`
- Build command: lämnas tom
- Output directory: lämnas tom
- Production branch: `main`

`vercel.json` innehåller clean URLs och säkerhetsheaders. Vid Git-integration ska varje push till `main` skapa en ny deployment.

## UX-principer

- snabb orientering före dokumentdjup
- uppdragslogiken framgår utan GitHub-kunskap
- vårdrealiseringsresan används som narrativ ryggrad
- startpaletten presenteras som preliminär, inte som redan beslutat urval
- extern yta skiljs tydligt från RFSU:s officiella webbplats
- responsiv navigering och tillgänglig semantik
- innehåll är synligt även om JavaScript inte körs
- animation respekterar `prefers-reduced-motion`
- mobilmenyn kan stängas med Escape och återför fokus till menyknappen

## QA

Repositoryt har en GitHub Actions-gate för webbplatsen. Vid push eller pull request som berör `site/` körs:

- HTML-validering
- JavaScript-syntaxkontroll
- kontroll att lokala `href`/`src`-mål finns
- kontroll att interna ankarlänkar pekar på existerande ID:n

## Säkerhet

Vercel-konfigurationen sätter bland annat:

- `X-Content-Type-Options`
- `Referrer-Policy`
- `X-Frame-Options`
- `Permissions-Policy`
- `Content-Security-Policy`

## Filer

- `index.html` — innehåll, metadata och semantisk struktur
- `styles.css` — visuellt system, responsivitet och reduced-motion
- `app.js` — mobilnavigation och progressivt förbättrad reveal
- `vercel.json` — Vercel-konfiguration och headers

## Produktionslås

Canonical URL och absolut Open Graph-bild läggs först när en faktisk Vercel-produktionsdomän eller egen domän är fastställd. De ska inte gissas i förväg.
