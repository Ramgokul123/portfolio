# Gokul Ramachandran — Portfolio

Cinematic, AI-driven single-page portfolio. Self-contained (one HTML file), no build step, no dependencies. Photo embedded. Code is obfuscated + copy-protected.

**Live:** _add your Vercel URL here after deploy_

## Deploy to Vercel
```bash
git init
git add .
git commit -m "Portfolio site"
git branch -M main
git remote add origin https://github.com/Ramgokul123/portfolio.git
git push -u origin main
```
Then vercel.com → **Add New → Project** → import repo → Framework **Other**, no build command, output `./` → **Deploy**.
Every future `git push` auto-redeploys.

## Enable the contact form (easy — this part is NOT obfuscated)
The form works out of the box via a mailto fallback. To receive real emails:
1. Create a free form at https://formspree.io and copy the ID (the part after `/f/`).
2. In `index.html`, find this readable line near the bottom:
   `<script>window.SITE_CONFIG = { FORMSPREE_ID: "YOUR_FORMSPREE_ID" };</script>`
3. Replace `YOUR_FORMSPREE_ID` with your ID. Commit & push — done.

## Content protection (what's included)
- Main JavaScript is **obfuscated** (unreadable).
- **Right-click disabled**, and DevTools/View-Source shortcuts blocked (F12, Ctrl+Shift+I/J/C, Ctrl+U, Ctrl+S).
- **Text selection / copy / drag disabled** (form fields stay usable).
- Anti-inspection (debugger) trap when DevTools is opened.

> Note: front-end code can never be 100% hidden — the browser must run it. These measures stop casual copying and inspection, not a determined developer. That's normal for every website.

## Editing later
- **Email / phone / résumé link / social links:** still plain text in `index.html` (search for them).
- **Formspree ID:** the readable config line above.
- **Colors:** CSS variables in `:root`.
- The scrambled `_0x...` block is the obfuscated app logic — leave it as-is.
