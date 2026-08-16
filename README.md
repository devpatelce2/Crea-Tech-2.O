# Crea-Tech 2.0 — Landing Page

Static single-page site (no build step). Ready to deploy on Vercel.

## Project structure
```
.
├── index.html      # the whole site (HTML/CSS/JS inline)
├── vercel.json     # static-site config + security headers
├── package.json    # optional local-dev scripts
└── .gitignore
```

## Run locally

Option A — Vercel CLI (matches production routing exactly):
```
npm i -g vercel
vercel dev
```

Option B — any static server:
```
npx serve .
```

Then open http://localhost:3000 (or whatever port is shown).

## Deploy to Vercel

**Via CLI:**
```
npm i -g vercel
vercel        # first deploy, follow prompts
vercel --prod # promote to production
```

**Via Git (recommended):**
1. Push this folder to a GitHub/GitLab/Bitbucket repo.
2. Go to https://vercel.com/new and import the repo.
3. Framework preset: "Other" (or leave as detected — no build command, no output directory needed since `index.html` sits at the project root).
4. Deploy. No environment variables required.

## Notes
- Everything (CSS, JS, canvas particle animation) is inline in `index.html` — no external assets to worry about except Google Fonts, which load from a CDN.
- The countdown timer target date is hardcoded in the `<script>` tag (`2026-08-22T00:00:00+05:30`) — update it if the event date changes.
- The registration link points to a Google Form and a WhatsApp group; update the URLs in the `#register` section if those change.
