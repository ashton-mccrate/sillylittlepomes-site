# sillylittlepomes-site

The marketing site + privacy policy for **Silly Little Pomes**, served by GitHub
Pages at <https://sillylittlepomes.com>.

Deliberately lean: plain static HTML/CSS, no build step. Two pages —

- `index.html` — the landing page.
- `privacy/index.html` — the privacy policy (`/privacy`), required by App Review
  because the app ships anonymous TelemetryDeck analytics.

## Brand assets

`assets/fonts/PomesDisplay.ttf`, `assets/img/splash-logo.png`, and the colour
values in `assets/css/site.css` are copied from the app repo
(`ashton-mccrate/sillylittlepomes`). If the wordmark or display font changes
there, re-copy them here. Colours mirror `src/theme/colors.ts`.

## Hosting

- GitHub Pages, deployed from `main` (root). `CNAME` pins the apex domain.
- **Enforce HTTPS** is on (Apple requires https for the Privacy Policy URL).
- DNS: apex `A`/`AAAA` records point at GitHub Pages; `www` CNAMEs to
  `ashton-mccrate.github.io`.

## Editing

Open the HTML files directly in a browser to preview, then push to `main`.
Changes go live in a minute or two.
