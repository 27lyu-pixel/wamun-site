# Woodward Model UN — website

Static site, no build step. 7 pages, one shared stylesheet.

## Deploy to GitHub Pages

1. Push these files to the root of your `wamun-site` repo (`main` branch).
2. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main`, folder `/root`. Save.
3. GitHub gives you a `https://<owner>.github.io/wamun-site/` URL within a minute or two.
4. To use your own domain: **Settings → Pages → Custom domain**, enter the domain. GitHub creates a `CNAME` file in the repo automatically. Then add the DNS records your registrar and GitHub's docs specify (an `A` record for an apex domain, or a `CNAME` record for a subdomain like `www`).

## Content still needed

Every card marked **Content to add** in the pages below needs real input before this replaces the Google Site:

| Page | What's missing |
|---|---|
| `wamun-xi.html` | Conference date/venue/fee, each committee's topic + background guide + chair, logistics (schedule, drop-off, dress code), registration form embed + deadline |
| `resources.html` | Position paper template/samples, parliamentary procedure sheet, resolution archive |
| `newsletter.html` | Links to each newsletter issue, both series |
| `photos.html` | Real photos in place of the six placeholder tiles |
| `cabinet.html` | Names, roles, photos for each officer |
| `secretariat.html` | Names, roles, photos for the WAMUN Secretariat |

Everything else (home page copy, nav, contact emails, Instagram link) is live already.

## Editing without touching layout

Each page is plain HTML — find the text or `<div class="tbd">` block you want to change and edit it directly. No build tools required. `styles.css` controls the look for every page at once; you generally shouldn't need to touch it for a content update.
