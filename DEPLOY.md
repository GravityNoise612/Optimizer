# GitHub Pages Deployment Guide

## Quick Start (5 minutes)

### Step 1: Fork the Repository
1. Click the **Fork** button on GitHub
2. This creates a copy of the project in your account

### Step 2: Enable GitHub Pages
1. Go to your forked repository **Settings**
2. Scroll down to **Pages** section (left sidebar)
3. Under "Build and deployment":
   - Source: Select **Deploy from a branch**
   - Branch: Select **main** (or whatever your default is)
   - Folder: Keep as **/ (root)**
4. Click **Save**

### Step 3: Access Your Site
GitHub will show you a URL like:
```
https://yourusername.github.io/gaming-settings-optimizer/
```

The site is now live! 🎉

---

## Usage After Deployment

### Making Changes
1. Edit `index.html` directly on GitHub or pull locally
2. Add/remove games in the `gamePatterns` array
3. Commit changes to `main` branch
4. GitHub Pages auto-deploys in ~1 minute

### Adding More Games
The `gamePatterns` array in `index.html` contains all supported games.

Format:
```javascript
{ exeNames: ['gameexe.exe', 'game.exe'], name: 'Game Name', priority: 10 }
```

### Updating Settings Database
The `gameDatabase` object contains settings for each game. Add new games or update existing ones:

```javascript
'game name': { 
    name: 'Display Name', 
    settings: { 
        low: { /* 10-12 settings */ },
        medium: { /* same settings */ },
        high: { /* same settings */ },
        ultra: { /* same settings */ }
    }
}
```

---

## Custom Domain (Optional)

Want to use your own domain instead of `yourusername.github.io`?

1. Go to **Settings** → **Pages**
2. Under "Custom domain", enter your domain
3. Add a CNAME record to your domain registrar:
   ```
   CNAME yourusername.github.io
   ```
4. GitHub will verify ownership automatically

---

## Troubleshooting

### Site not loading?
- Wait 2-3 minutes for GitHub Pages to build
- Clear browser cache (Ctrl+Shift+Delete)
- Check if you enabled GitHub Pages correctly

### Changes not showing?
- GitHub Pages rebuilds automatically when you push
- May take 1-2 minutes to appear
- Check the **Actions** tab to see build status

### 404 Error?
- Make sure file is named exactly `index.html`
- Check repository name matches your URL
- Verify Pages is enabled in Settings

---

## Local Testing (Before Deploying)

### Option 1: Live Server (VS Code)
1. Install VS Code extension "Live Server"
2. Right-click `index.html` → "Open with Live Server"
3. Browser opens at `http://localhost:5500`

### Option 2: Python
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```
Then visit: `http://localhost:8000`

---

## File Structure

```
gaming-settings-optimizer/
├── index.html           # Main app (all-in-one file)
├── README.md            # Documentation
├── LICENSE              # MIT License
├── .gitignore          # Git ignore rules
└── DEPLOY.md           # This file
```

---

## CI/CD with GitHub Actions (Advanced)

If you add linting or build steps later, GitHub Actions will auto-run on every push.

For now, the site uses **simple static hosting** - no build process needed.

---

## Analytics (Optional)

Want to track usage? Add these free services:

### Google Analytics
Add to `<head>` section of `index.html`:
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_ID');
</script>
```

### Plausible Analytics (Privacy-Friendly)
```html
<script defer data-domain="yourdomain.com" src="https://plausible.io/js/script.js"></script>
```

---

## Support & Issues

- **Question?** Open a GitHub Discussion
- **Bug?** Open an Issue with details
- **Want to add games?** Open a Pull Request

---

## Performance Tips

1. **Compress index.html** before commit (optional)
2. **Browser caching** is automatic - users benefit from GitHub's CDN
3. **File size** - currently ~100KB (single HTML file)

---

## Next Steps

1. ✅ Deployed to GitHub Pages
2. 📝 Update README with your username
3. 🎮 Test with your game folder
4. 🌟 Star the repo if you like it!

Enjoy! 🚀
