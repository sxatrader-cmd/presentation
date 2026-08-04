# GitHub Repository Setup

## Files Structure (All in root directory)

```
presentation/
├── index.html                        ← MAIN FILE (open this in browser)
├── Belka_Travel_Concierge_AR.pdf     ← Full Arabic PDF
├── README.md                         ← Documentation
├── pg_ru_01.png to pg_ru_16.png      ← Russian pages (16 files)
├── pg_ar_01.png to pg_ar_16.png      ← Arabic pages (16 files)
└── .gitattributes                    ← Git config for large files
```

## GitHub Pages Setup

### Step 1: Create Repository
```bash
# On GitHub.com
1. Create new repo: "presentation"
2. Make it PUBLIC
3. DO NOT add README (we have one)
```

### Step 2: Push Files
```bash
cd /path/to/outputs

git init
git add .
git commit -m "Initial commit: Belka Travel Concierge 3-language presentation"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/presentation.git
git push -u origin main
```

### Step 3: Enable GitHub Pages
```
1. Go to Settings → Pages
2. Source: Deploy from a branch
3. Branch: main / (root)
4. Save
```

### Your Live URL
```
https://YOUR_USERNAME.github.io/presentation/
```

## File Sizes
- 📄 index.html: 12 KB
- 📊 PNG images: ~38 MB total (17 RU + 17 AR)
- 📄 PDF: 22 MB
- 📄 README: 3 KB

**Total: ~60 MB** (within GitHub's limits)

## Testing Locally
```bash
# Simple Python server
python3 -m http.server 8000

# Then open: http://localhost:8000/
```

## Troubleshooting

### Images not loading?
- Check all `pg_*.png` files are uploaded
- Verify filenames match exactly (case-sensitive)
- Check browser console (F12) for errors

### Slideshow not working?
- Verify index.html is in root directory
- Check JavaScript is enabled
- Try different browser
- Clear cache (Ctrl+Shift+Del)

### Page takes too long to load?
- First load: normal (downloads ~38 MB images)
- Subsequent loads: instant (cached)
- Consider using CDN if on slow network

---
**Ready to deploy! 🚀**
