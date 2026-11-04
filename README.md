# Neelima P R – Technical Writing Portfolio

A single-page portfolio website for Neelima P R, Senior Technical Writer. It showcases projects, core expertise, work history, tools and contact details.

**Live site:** `https://<your-username>.github.io/<repo-name>/`
 
## Features

- Single self-contained `index.html` with no build step and no dependencies
- Responsive layout for desktop, tablet and mobile
- Light and dark themes, following the system setting with a manual toggle
- Sections: Hero, Selected Work, Core Expertise, About and Timeline, Tools, Education, Contact
- Copy-to-clipboard email button
- Respects reduced-motion preferences

## Project structure

```
.
├── index.html   # The entire site (HTML, CSS and JS)
└── README.md
```

## Run locally

Open `index.html` in any browser. Or serve it locally:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

1. Create a public repository. Naming it `<your-username>.github.io` gives you a root URL.
2. Upload `index.html` and `README.md` to the repository root.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and the `/ (root)` folder, then click **Save**.
6. Wait a minute or two, then open the URL shown on the Pages settings screen.

The same file also works on Netlify, Cloudflare Pages and Vercel by dropping in the folder.

## Customise

| What | Where in `index.html` |
| --- | --- |
| Colours and theme | CSS variables in `:root` at the top of the `<style>` block |
| Hero text and stats | `<header class="hero">` |
| Projects | `<section id="work">`, one `<article class="card">` per project |
| Timeline | `<div class="timeline">` in the About section |
| Tools | The `.tools` block, one `.chips` group per category |
| Email | `mailto:` links, the visible address, and the `writeText(...)` call in the script |
| Page title and description | `<title>` and `<meta name="description">` in `<head>` |

### Adding a LinkedIn link

Add this inside the contact section's `.btns` div:

```html
<a class="btn ghost" href="https://www.linkedin.com/in/your-profile/">LinkedIn</a>
```

### Adding work samples

Link a project card to a sample by adding an anchor inside the card, for example:

```html
<a href="https://link-to-your-sample" style="color:var(--accent)">View sample →</a>
```

Or host PDFs and pages in the same repo and link to them with relative paths.

## Tech

HTML5, CSS3 and vanilla JavaScript. Fonts (Fraunces and Inter) are loaded from Google Fonts, with system font fallbacks.

## Contact

neelspr4@gmail.com

## License

© Neelima P R. All rights reserved.
