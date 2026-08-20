# Woodward Model UN — website

Static site, no build step. 7 pages, shared stylesheet, one small JS file.

## Files

| File | What it is |
|---|---|
| `index.html` | Home |
| `wamun-xi.html` | Conference: committees, logistics, registration |
| `resources.html` | Position papers, procedure, resolutions |
| `calendar.html` | Meeting schedule + upcoming events |
| `photos.html` | Club photo gallery |
| `cabinet.html` / `secretariat.html` | Leadership rosters |
| `styles.css` | All layout, type, and color |
| `motifs.css` | Background motif positioning + scroll animation styles |
| `site.js` | Injects background motifs, runs scroll reveals and parallax |
| `images/` | Logo, headshots, club photos |

## Deploy to GitHub Pages

Already configured: **Settings → Pages**, source `main`, folder `/root`.
Push to `main` and the site rebuilds automatically at
`https://27lyu-pixel.github.io/wamun-site/`.

For a custom domain: **Settings → Pages → Custom domain**, then add the DNS
records GitHub specifies at your registrar.

## Design notes

- **Colors** live as CSS variables at the top of `styles.css` (`:root`).
  Changing those five hex values re-skins every page at once.
- **Background motifs** (globe, country polygons, seated delegates, dot grid)
  are SVGs injected by `site.js` and positioned by `motifs.css`. Adjust
  `.motif { opacity }` to make them more or less visible.
- **Scroll behavior**: elements with class `reveal` fade up when scrolled into
  view; motifs drift at different rates; a red progress rail tracks page
  position. All of it is disabled automatically under
  `prefers-reduced-motion`.

## Content still needed

| Page | What's missing |
|---|---|
| `images/logo.png` | Club logo — header and footer fall back to text until added |
| `wamun-xi.html` | Date, venue, fee, committee topics, background guides, chairs, logistics, registration form |
| `resources.html` | Position paper template, procedure sheet, resolution archive |
| `calendar.html` | Meeting day/time/room, real upcoming events |
| `photos.html` | Real photos for the six placeholder tiles |
| `cabinet.html` / `secretariat.html` | Names, roles, headshots |

Anything marked **Content to add** in a page is a placeholder meant to be
replaced, not styled around.
