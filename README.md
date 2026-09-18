# Gokul Ramachandran — Portfolio

A cinematic, AI-driven single-page portfolio. Self-contained (one HTML file), no build step, no dependencies. Your profile photo is already embedded.

**Live:** _add your Vercel URL here after deploy_

## Features
- Mouse-reactive neural-network canvas background
- Cinematic scroll & reveal animations
- Project showcase with detail modals
- "Ask my AI" assistant (runs 100% in-browser — no API key/backend)
- Working contact form (Formspree) with a mailto fallback
- Fully responsive, dark neon theme

## Deploy to Vercel

### Option A — Git (recommended)
```bash
git init
git add .
git commit -m "Portfolio site"
git branch -M main
git remote add origin https://github.com/Ramgokul123/portfolio.git
git push -u origin main
```
Then: https://vercel.com → **Add New → Project** → import the repo → Framework Preset **Other**, no build command, output dir **`./`** → **Deploy**.

### Option B — Vercel CLI
```bash
npm i -g vercel
vercel --prod
```

## Enable the contact form (2 minutes)
The form works out of the box via a **mailto fallback** (opens the visitor's email app). To receive messages as real emails instead:
1. Sign up free at https://formspree.io and create a new form.
2. Copy your form ID (looks like `xdorwkln`, the part after `/f/`).
3. In `index.html`, find:  `const FORMSPREE_ID = 'YOUR_FORMSPREE_ID';`
4. Replace `YOUR_FORMSPREE_ID` with your ID. Commit & push — Vercel redeploys automatically.

## Customize
- **Photo:** already embedded. To change it, replace the `<img src="data:image/jpeg;base64,…">` inside `<div class="inner" id="avatarInner">`.
- **Résumé link:** search `powerdriveedm.com/resume/resume-gokul` and swap in your URL (or add `resume.pdf` to the repo and use `/resume.pdf`).
- **Colors:** edit the CSS variables in `:root` at the top of the `<style>` block.
