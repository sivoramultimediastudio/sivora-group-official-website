# SIVORA GROUP — Official Three-Business Website

A responsive, static, multi-page website for **SIVORA MULTIMEDIA STUDIO**, **SIVORA TRENDZ**, and **SIVORA FARMING**.

## GitHub repository and Render site names
- Suggested GitHub repository: `sivora-group-official-website`
- Suggested Render Static Site: `sivora-group-web`
- Example Render URL (subject to availability): `https://sivora-group-web.onrender.com`

## CRITICAL: Correct upload procedure
This ZIP is intentionally **flat**. When extracted, the HTML files must be at the repository **root**, alongside the `assets` folder. Upload the *contents* of the extracted folder, **not the ZIP itself**. Do not upload a parent folder containing all the website files.

Expected structure:
```
index.html
multimedia.html
trendz.html
farming.html
contact.html
style.css
script.js
render.yaml
assets/multimedia.png
assets/trendz.png
assets/farming.png
```

## Render deployment
1. Create a **public** GitHub repository named `sivora-group-official-website` (or another available name).
2. Upload the extracted files at repository root. Check that clicking `index.html` shows full HTML beginning with `<!doctype html>`.
3. Create a new **Static Site** on Render and connect the GitHub repository.
4. Branch: `main`; Root Directory: **blank**; Build Command: `echo "Static website ready"`; Publish Directory: `.`.
5. Deploy and test `/`, `/multimedia.html`, `/trendz.html`, `/farming.html`, `/contact.html` and `/assets/multimedia.png`, `/assets/trendz.png`, `/assets/farming.png`.

## Local preview
Open `index.html` in your browser, or run `python3 -m http.server 8000` from the extracted folder.

## Before launch
Contact page currently uses general enquiry instructions; verify contact details and add actual approved business contact information before public promotion. All logos are the original supplied PNG assets, without modifications. The website is not an e-commerce checkout or backend service.
