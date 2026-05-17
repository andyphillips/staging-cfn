# Communities for Nature — Website

Staging website for **Communities for Nature** (UK Charity 1204810).

🌐 **Live site:** https://andyphillips.github.io/staging-cfn/

## Structure

```
.
├── index.html                  # Homepage (hero video, pathways, stories)
├── about.html                  # About / Mission / Model / Partners / Governance
├── work-and-impact.html        # Programmes overview, impact stats, stories
├── programmes.html             # All programmes index
├── programme-mithi.html        # Project MITHI detail page
├── stories.html                # Stories & insights index
├── story-mithi.html            # Featured story article
├── get-involved.html           # Partner With Us / Work With Us
├── donate.html                 # Donations — one-off, monthly, crypto
├── contact.html                # Contact form
├── styles.css                  # Shared, mobile-first stylesheet
├── assets/                     # Published assets
│   ├── logo.png
│   └── hero-ocean.mp4
├── AI_images/                  # AI-generated thematic imagery
└── .nojekyll                   # Disables Jekyll processing on GH Pages
```

## Local Development

Open via a local web server (NOT `file://`, as the hero video and some assets won't play):

```bash
python3 -m http.server 8080
# then open http://localhost:8080
```

## Design System

- **Fonts:** Lora (headlines), Square Peg (accents), Nunito (body)
- **Colours:** Teal `#22a7b0`, Dark Teal `#0e6e75`, Off-white `#f5f3ef`
- **Approach:** Mobile-first CSS with breakpoints at 640px, 1024px, 1280px
- **Reusable components:** `.page-hero`, `.split-feature`, `.feature-image-block`, `.story-item`, `.programme-card`, `.card`, `.pw-card`

## Publishing to GitHub Pages

The site publishes from the `main` branch root. After pushing:

1. Repo → **Settings** → **Pages**
2. Source: **Deploy from a branch** → `main` / `(root)`
3. Wait ~1 min, then visit the URL shown.

## What's Ignored from Git

Source media folders (`newImages/`, `images/`, `figma/`, `thumbs/`), IDE files, design-exploration HTML and original-resolution photos are kept locally but excluded from the repo (see `.gitignore`). Only the optimised, published versions live in `assets/` and `AI_images/`.

## ⚠️ Security Note

The current `origin` remote URL contains an embedded GitHub Personal Access Token. **Rotate this token** and re-set the remote without credentials in the URL:

```bash
git remote set-url origin https://github.com/andyphillips/staging-cfn.git
# Then use a credential helper or SSH for auth.
```

