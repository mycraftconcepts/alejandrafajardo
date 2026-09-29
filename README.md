# Alejandra Fajardo Beltrán — Personal Site

One-page bilingual (ES/EN) resume site.

**Live:** https://alejandrafajardo.mycraftconcepts.com/

## Structure

Static site, no build step. Served directly by GitHub Pages from `main`.

| Path | Purpose |
| --- | --- |
| `index.html` | The site. Language copy lives in the `COPY` object in the inline script at the bottom. |
| `support.js` | Small render runtime the page depends on |
| `AlejandraFajardoBeltran-Resume-EN.pdf` / `-ES.pdf` | Printable resumes, linked from the "Printable resume" / "Hoja de vida" buttons |
| `favicon.*`, `apple-touch-icon.png`, `icon-*.png`, `site.webmanifest` | AFB monogram icons, rendered from the same Cormorant Garamond mark used in the nav. Small sizes use a proportionally larger monogram so it stays legible at 16px. |
| `og-card.jpg` | 1200×630 link-preview card, referenced by the Open Graph and Twitter meta tags in `index.html` |
| `portrait-square.jpg` | Portrait |
| `CNAME` | Custom domain for GitHub Pages (`alejandrafajardo.mycraftconcepts.com`) |
| `.nojekyll` | Tells Pages to serve files as-is, without Jekyll processing |

## Updating

- **Resumes:** replace the PDFs, keeping the same filenames.
- **Page content:** edit the `COPY` object in `index.html` (both languages).
- **Name, role line or portrait:** regenerate `og-card.jpg` too, or shared links will show stale details.
- **Domain:** the canonical URL, `og:url` and `og:image` in `index.html` use the full `https://alejandrafajardo.mycraftconcepts.com/` address. Update them if the domain ever changes.

Commit to `main` and Pages redeploys automatically.

## Hosting

- **Repository:** `mycraftconcepts/alejandrafajardo`, hosted by Craft Concepts Digital.
- **Domain:** `alejandrafajardo.mycraftconcepts.com`, a Cloudflare CNAME record pointing to `mycraftconcepts.github.io` (DNS only, not proxied). The `mycraftconcepts.com` domain is verified in the `mycraftconcepts` GitHub organization.
- **HTTPS:** enforced in the repository's Pages settings.
- **Don't delete `CNAME`.** If the repository is ever transferred, GitHub drops the custom domain: set it again in Settings → Pages right away.
- The old address, `alejandra-fajardo-beltran.github.io`, no longer works.

## Local preview

```
python3 -m http.server 8000
```

Then open http://localhost:8000
