# henryookonkwo.github.io

Personal portfolio site. Static HTML, no build step, no dependencies to install.

**Live:** https://henryookonkwo.github.io

## Files

| File | What it is |
|---|---|
| `index.html` | The entire site — markup, CSS and JS in one file |
| `favicon.svg` | Browser tab icon |
| `og-image.png` | Link preview card (1200×630) for LinkedIn, Slack, iMessage, X |
| `robots.txt` | Search engine directives |
| `sitemap.xml` | Sitemap for search engines |
| `.nojekyll` | Tells GitHub Pages to serve files as-is, skipping Jekyll processing |

## Deploying

GitHub Pages serves this repository directly. Any push to `main` is live in about a minute.

Settings → Pages → Source: **Deploy from a branch** → Branch: **main** / **/ (root)**.

## Editing

Open `index.html` in any editor. Everything is in that one file:

- CSS custom properties for the whole colour system are at the top, in `:root`. Light values are defined there; the dark palette redefines the same names in the two blocks below it.
- Content follows the stylesheet, section by section.
- The JavaScript at the bottom handles three things: the theme toggle, the expandable stack layers, and the scroll-spy on the index rail.

To preview locally, open the file in a browser, or run `python3 -m http.server` in this folder and visit `http://localhost:8000`.

## If you move to a custom domain

1. Add a file named `CNAME` in this folder containing only the domain, e.g. `henryokonkwo.dev`
2. At your DNS provider, add four `A` records for the apex domain pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`, and a `CNAME` record for `www` pointing to `henryookonkwo.github.io`
3. In Settings → Pages, enter the domain and tick **Enforce HTTPS** once the certificate is issued
4. Find-and-replace `https://henryookonkwo.github.io` with the new domain in `index.html`, `robots.txt` and `sitemap.xml` — those absolute URLs are what link previews and search engines use

## Accessibility

The page is built to WCAG 2.1 AA: skip link, semantic landmarks, ordered headings, visible focus rings, keyboard-operable disclosure widgets with correct ARIA state, `aria-current` on the active section, 44px minimum touch targets, and full `prefers-reduced-motion` and `forced-colors` support. Keep those intact when editing.
