# Gokul Ramachandran — Portfolio

Cinematic, AI-driven single-page portfolio. Self-contained, no build step. Photo embedded, code obfuscated + copy-protected.

**Live:** https://portfolio-six-sand-90.vercel.app/

## Files
- `index.html` — the whole site (one file)
- `resume.pdf` — served by the site's "Résumé" buttons at `/resume.pdf`
- `vercel.json`, `.gitignore`

## Deploy / update
```bash
git add .
git commit -m "update site"
git push
```
Vercel auto-redeploys in ~30s.

## Contact form
Already connected to Formspree (ID `moevvqjy`) — messages go to your inbox.
- First submission: Formspree emails you a one-time confirmation link — click it to activate delivery.
- To change the address/ID later, edit the readable line near the bottom of `index.html`:
  `<script>window.SITE_CONFIG = { FORMSPREE_ID: "moevvqjy" };</script>`
- A hidden honeypot field blocks spam bots automatically.

## Update your resume later
Replace `resume.pdf` in this folder with a new file of the same name, commit & push. The Résumé buttons will serve the new one.

## Content protection
Obfuscated JS, right-click + DevTools shortcuts blocked, text-copy disabled (form fields still work). Note: front-end code can never be fully hidden — this deters casual copying only.
