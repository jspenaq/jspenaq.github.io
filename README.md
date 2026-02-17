# jspenaq.github.io

Developer portfolio for Juan Sebastián Peña Quintero.

## 🚀 Live Sites

- **Portfolio (Developer):** https://jspenaq.github.io
- **Consulting (Security):** https://jspenaq.dev

## 📁 Structure

```
/
├── index.html          # Homepage with hero + featured projects
├── work.html           # All work page with bento grid
├── work/               # Project detail pages
│   ├── lolsapiens.html
│   ├── docker-ai.html
│   ├── pokecoach.html
│   └── ...
└── README.md
```

## 🎨 Design

- **Style:** Neo-brutalist (bold borders, offset shadows, high contrast)
- **Colors:** Cream background (#f5f0e8), black text, yellow accent (#f5e642)
- **Fonts:** Space Grotesk (headers), Space Mono (monospace)
- **Layout:** Bento grid for project listings, 7-block template for details

## 📦 Deployment to GitHub Pages

### Initial Setup

1. **Create repository:**
   ```bash
   # Repository name MUST be: jspenaq.github.io
   ```

2. **Push code:**
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/jspenaq/jspenaq.github.io.git
   git push -u origin main
   ```

3. **Enable GitHub Pages:**
   - Go to repository Settings
   - Navigate to Pages (left sidebar)
   - Source: Deploy from branch
   - Branch: `main` / `root`
   - Click Save

4. **Wait 2-3 minutes** for deployment

5. **Visit:** https://jspenaq.github.io

### Updates

```bash
# Make changes to HTML files
git add .
git commit -m "Update portfolio"
git push

# GitHub Pages auto-deploys in 1-2 minutes
```

## 🔗 Links to Update

Before deploying, update these links in the HTML:

### In `index.html`, `work.html`, and project pages:

- **Calendly:** Replace `https://calendly.com/jspenaq` with your actual link
- **Email:** Confirm `jspenaq@unal.edu.co` is correct
- **LinkedIn:** Confirm `/in/juan-sebastian-peña-quintero` is correct
- **GitHub:** All GitHub links point to correct repos

## ✏️ Editing Projects

### To add a new project:

1. **Add to `work.html`:**
   - Copy a `.bento-card` div
   - Update title, description, tags, links

2. **Create detail page:**
   - Copy `work/lolsapiens.html` as template
   - Update all 7 sections (Context, Role, Decisions, etc.)
   - Save as `work/yourproject.html`

3. **Update featured (optional):**
   - Add to `index.html` featured grid if it's a top project

### To edit existing projects:

- Open the relevant HTML file
- Use Ctrl+F to find the section
- Edit the text directly
- Commit and push

## 🎯 SEO & Meta Tags

Each page has:
- `<title>` - Shows in browser tab
- `<meta name="description">` - Shows in Google search
- Open Graph tags ready (can add later)

## 🔄 Two-Site Strategy

**jspenaq.github.io** (this site):
- For developer roles
- Showcases fullstack/AI projects
- Code-heavy, technical

**jspenaq.dev** (separate):
- For consulting clients
- LLM Security focus
- Business-facing

Both use same neo-brutalist style for brand consistency.

## 🐛 Troubleshooting

**Site not updating?**
- Check Actions tab for build status
- Hard refresh browser (Ctrl+Shift+R)
- Clear GitHub Pages cache: Settings → Pages → Save again

**404 errors?**
- Verify repository name is `jspenaq.github.io`
- Check file names are lowercase and match links
- Confirm branch is `main` (not `master`)

**Styles broken?**
- All CSS is inline in HTML (no external files needed)
- Check browser console for errors

## 📱 Mobile Responsive

All pages are mobile-responsive with breakpoint at 900px.
Test at: https://responsivedesignchecker.com

## 📄 License

Portfolio content © 2026 Juan Sebastián Peña Quintero

Code structure can be used as reference for personal portfolios.
