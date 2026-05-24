# Goalski landing page (Carrd-style)

A single-page, dependency-free landing page in the Carrd aesthetic. Pure HTML, CSS, and a tiny bit of JavaScript. No build step required.

## What's in this folder

- `index.html` — the entire page (hero, features, pricing, trial callout, FAQ, footer)
- `style.css` — all styling (brand palette, typography, layout, responsive rules)
- `script.js` — scroll-fade animations and the current-year footer stamp
- `logo.png` — the Goalski logo (used both for the hero mark and the browser favicon)

## Run it locally

Just double-click `index.html`. It opens in your browser. Done. No npm, no install.

If you want a slightly nicer local preview with live reload, you can run a one-line static server from this folder:

```
npx serve .
```

## Publish to GitHub Pages

1. Create a new public GitHub repository (for example `goalski-landing`).
2. Drag the four files from this folder into the repo on github.com (or push from the command line).
3. In the repo, go to **Settings → Pages**.
4. Under **Source**, pick the `main` branch and the `/ (root)` folder, then click **Save**.
5. Wait about a minute. GitHub will give you a URL like `https://yourname.github.io/goalski-landing/`.

To point your own domain (like `goalski.com`) at it:

1. In GitHub **Settings → Pages**, type your domain into **Custom domain** and save.
2. At your domain registrar, add a `CNAME` record pointing your domain to `yourname.github.io`.
3. Wait for DNS to propagate (a few minutes to a few hours), then turn on **Enforce HTTPS**.

## Editing tips

- All copy lives in `index.html`. Search for the text you want to change and edit it in place.
- Brand colors live at the top of `style.css` under `:root` — change one variable and it cascades everywhere.
- The signup CTAs use `mailto:hello@goalski.com`. Replace that email address in `index.html` (three spots) with whatever address you actually want leads to land in.
- The page uses Inter from Google Fonts. To swap fonts, replace the `<link>` in `index.html` and the `font-family` line in `style.css`.

## What's NOT included (on purpose)

- No backend, no `/api/leads` integration. The form is a plain mailto, exactly like a real Carrd site. If you want to wire it back to the Goalski API later, swap the mailto buttons for an HTML `<form>` that posts to `https://goalski.com/api/leads`.
- No React, no framer-motion, no Tailwind. Just three files.
- No analytics. Drop in a snippet from Google Analytics, Plausible, or Fathom by pasting it before `</head>` in `index.html`.
