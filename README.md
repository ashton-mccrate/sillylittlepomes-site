# sillylittlepomes-site

The marketing site + privacy policy for **Silly Little Pomes**, served by GitHub
Pages at <https://sillylittlepomes.com>. It also hosts the landing + privacy
pages for the sibling app **Little While** under `/littlewhile` (same domain,
shared CSS — cheaper than standing up a second site).

Deliberately lean: plain static HTML/CSS, no build step.

Silly Little Pomes —

- `index.html` — the landing page.
- `privacy/index.html` — the privacy policy (`/privacy`), required by App Review
  because the app ships anonymous TelemetryDeck analytics.

Little While —

- `littlewhile/index.html` — the landing page, which doubles as the App Store
  **Support URL** (`/littlewhile`); it carries the support email.
- `littlewhile/privacy/index.html` — the privacy policy (`/littlewhile/privacy`).
  Little While collects nothing (no network, no accounts, no analytics), so the
  policy just says so — but App Review still requires the URL.

## Brand assets

`assets/fonts/PomesDisplay.ttf`, `assets/img/splash-logo.png`, and the colour
values in `assets/css/site.css` are copied from the Pomes app repo
(`ashton-mccrate/sillylittlepomes`). If the wordmark or display font changes
there, re-copy them here. Colours mirror `src/theme/colors.ts`.

`assets/img/littlewhile-wordmark.png` (the app's transparent splash mark) and
`assets/img/littlewhile-favicon.png` (its app icon) are copied from the Little
While app repo (`ashton-mccrate/littlewhile`, `assets/splash-icon.png` and
`assets/icon.png`). Little While reuses the same PomesDisplay font + palette, so
no extra fonts or colours are needed.

## Hosting

- GitHub Pages, deployed from `main` (root). `CNAME` pins the apex domain.
- **Enforce HTTPS** is on (Apple requires https for the Privacy Policy URL).
- DNS: apex `A`/`AAAA` records point at GitHub Pages; `www` CNAMEs to
  `ashton-mccrate.github.io`.

## Editing

Open the HTML files directly in a browser to preview, then push to `main`.
Changes go live in a minute or two.
