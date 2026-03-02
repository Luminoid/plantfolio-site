# plantfolio-site

Static marketing site for [Plantfolio Plus](https://apps.apple.com/us/app/plantfolio-plus/id6757148663). Landing page, features, custom plants guide, and privacy policy. No build step—plain HTML and CSS.

## Structure

```
plantfolio-site/
├── index.html                  # English landing (root)
├── privacy.html                # English privacy policy
├── custom-common-plants.html    # Guide: add custom common plants source
├── css/
│   └── styles.css               # Shared styles
├── TRANSLATIONS.md              # Translation sync reference
├── resources/
│   ├── app_icon.png             # App icon (quantized)
│   ├── screenshots/             # App screenshots (quantized 90-100%)
│   │   └── app-1.png … app-6.png
│   └── custom-common-plants-source/  # Step images for custom plants guide
│       └── step1.png … step5.png
├── es/                          # Spanish
│   ├── index.html
│   ├── custom-common-plants.html
│   └── privacy.html
├── zh/                          # Chinese (Simplified)
│   ├── index.html
│   ├── custom-common-plants.html
│   └── privacy.html
├── .gitignore
└── .nojekyll                    # GitHub Pages
```

## Locales

| Locale | Path | Pages |
|--------|------|-------|
| English | `/` | index, privacy, custom-common-plants |
| Spanish | `/es/` | index, privacy, custom-common-plants |
| Chinese (Simplified) | `/zh/` | index, privacy, custom-common-plants |

## Translation sync

When editing content, update all three locales. See `TRANSLATIONS.md` for string mapping.

## Scripts

**Compress PNGs (pngquant 90%)** — pass the file(s) or glob so you only run it on what you need (avoid re-compressing already quantized images):

```bash
pngquant --quality=90-100 --ext .png --force <files-or-glob>
```

## Content

- **Hero**: App name, tagline, description; lang switcher and App Store badge (alternative white, links to `#download`) top right.
- **Features**: Plants & Collections (AI + ML identification), Watering & Calendar, Photos & Care Logs, Home Screen Widgets (Up Next + Calendar + Scan & Identify), Reminders, Sightings & Map, Your Data, Sharing (plant cards, ICS export), Language & Settings
- **Why Choose**: Works without internet, adapts to your seasons, beyond the garden, one app every device, own your data
- **Download**: Section `id="download"` with app icon, App Store + Mac App Store badges
- **Platforms**: iPhone, iPad, Mac (Catalyst)
- **App Store**: [iOS](https://apps.apple.com/us/app/plantfolio-plus/id6757148663) · [Mac](https://apps.apple.com/us/mac-app/plantfolio-plus/id6757148663)
