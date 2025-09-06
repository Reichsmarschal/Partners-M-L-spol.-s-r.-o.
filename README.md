# Partners-M-L-spol.-s-r.-o.
Commit to Deploy  Ziel: Jeder Merge in main veröffentlicht automatisch die produktive Website. Jeder PR erzeugt eine isolierte Vorschau. Rollback in Minuten.
Pipeline

Commit pushen.

CI baut das Projekt.

Tests und Lint laufen.

PR: Preview-URL. main: Live-Deploy.

Cache invalidieren. Monitoring prüfen. Version taggen.

Branch-Strategie

main: Produktion.

develop: Staging.

feature/*: PR mit Preview-Deploy.

Qualitätschecks

Build muss erfolgreich sein.

Lint ohne Fehler.

Lighthouse ≥ 90 für Performance und SEO.

404 und 500 Seiten vorhanden.

DSGVO: Cookie Banner, Impressum, Datenschutz.

Rollback

Vorherigen erfolgreichen Build aus der Deploy-Historie reaktivieren.

Alternativ letzten Release-Tag auschecken und neu deployen.

Secrets und Variablen

SITE_ID, AUTH_TOKEN oder Provider-spezifische Keys.

BASE_URL, ENV=production|staging.

Niemals Secrets ins Repo commiten.

Option A: Netlify Git-Integration

Repo verbinden.

Build Command: npm run build.

Publish Directory: dist oder build.

Deploy Previews aktivieren.

Redirects in _redirects pflegen.
