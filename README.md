# Christian Ed Brun — Executive Virtual Assistant — Website

A simple, responsive one-page portfolio site plus a privacy page. Clean, accessible HTML and CSS ready to publish with GitHub Pages.

Status
- Last updated: 2026-01-01
- Intended for use as a GitHub Pages site (user site or project site).

Contents
- `index.html` — Main one-page site (hero, services, portfolio, testimonials, about, contact).
- `privacy.html` — Privacy policy page.
- `style.css` — Site styles.
- `README.md` — This file.

Quick local preview
1. Save the files to a folder on your computer.
2. Open `index.html` in your browser (no server required).
3. To preview pages served from a local server (optional):
   - Python 3: `python -m http.server 8000` then open `http://localhost:8000/`
   - Or use the Live Server extension in VS Code.

Publish with GitHub Pages (recommended)
- If you want the site at `https://christianedbrun-stack.github.io/` name the repository exactly:
  `christianedbrun-stack.github.io` (this becomes a user site).
- For a project site, any repo name is fine and the published URL will be:
  `https://<username>.github.io/<repo>/`

Example git commands (run locally)
1. Initialize and push:
   ```
   git init
   git add .
   git commit -m "Initial site for Christian Ed Brun"
   git branch -M main
   git remote add origin git@github.com:<your-username>/<repo-name>.git
   git push -u origin main
   ```
2. Enable GitHub Pages:
   - In the repository Settings → Pages, select branch `main` and folder `/ (root)` and save.
   - Wait a minute for the site to publish.

Required edits before publishing
- Formspree contact form: replace the placeholder action in `index.html`
  ```
  action="https://formspree.io/f/{your-id}"
  ```
  with your actual Formspree form ID, e.g.
  ```
  action="https://formspree.io/f/your-id-here"
  ```
  Or replace the form with another backend (Netlify Forms, server endpoint, etc.).
- Images: the portfolio images currently use external Unsplash URLs. If you prefer self-hosted images, add them (e.g., `assets/img/`) and update the `src` paths in `index.html`.
- Privacy & legal: review `privacy.html` and adapt text to your policies and any applicable laws (GDPR, CCPA, HIPAA handling notes if relevant).

Accessibility & SEO notes
- All images include `alt` text and loading="lazy".
- Navigation includes aria attributes and a mobile-friendly toggle.
- Edit meta tags in `index.html` (title, description, open graph) for better SEO and sharing.

Customization ideas
- Add a `favicon.ico` and social preview image (og:image).
- Add a downloadable services PDF (link to a file in the repo or external URL).
- Add analytics (e.g., Plausible or Google Analytics) — prefer privacy-focused options if you handle client data.
- Convert to a small static site generator (Hugo, Eleventy) if you want templating for future content.

Troubleshooting
- Page is unstyled: ensure `style.css` exists at site root and the `<link rel="stylesheet" href="style.css">` path is correct.
- 404 on privacy: confirm `privacy.html` is at the repo root and the link is `/privacy.html` (or `privacy.html` for relative linking).
- Mobile nav not opening: ensure JavaScript is loaded and JS is allowed in your browser.
- Contact form not sending: test the form, check the Formspree dashboard, or try a different form backend.

Want me to add this to a GitHub repo?
- I can prepare a commit and push these files if you provide the repository name and add me as a collaborator or give permission. If you prefer to do it yourself, paste the repo name and I’ll provide exact commands tailored to whether it should be a user site (`christianedbrun-stack.github.io`) or a project site.

Contact
- Email: christianedbrun@gmail.com

License
- You can add a license file (e.g., `MIT`) if you want this template to be reusable. This repository currently has no license file.
