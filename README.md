# plantfolio-site

Static marketing site for [Plantfolio Plus](https://apps.apple.com/us/app/plantfolio-plus/id6757148663). Landing page, features, custom plants guide, and privacy policy. No build step—plain HTML and CSS, hosted on Cloudflare Pages.

## Structure

```
plantfolio-site/
├── index.html                       # English landing (root)
├── privacy.html                     # English privacy policy
├── custom-common-plants.html        # Guide: add custom common plants source
├── css/
│   └── styles.css                   # Shared styles (CSS variables, responsive)
├── resources/
│   ├── app_icon.png                 # App icon (quantized)
│   ├── screenshots/                 # App screenshots (quantized 90-100%)
│   │   └── app-1.png … app-6.png
│   └── custom-common-plants-source/ # Step images for custom plants guide
│       └── step1.png … step5.png
├── es/                              # Spanish
│   ├── index.html
│   ├── custom-common-plants.html
│   └── privacy.html
├── zh/                              # Chinese (Simplified)
│   ├── index.html
│   ├── custom-common-plants.html
│   └── privacy.html
├── _headers                         # Cloudflare Pages security headers (CSP, X-Frame-Options, etc.)
├── TRANSLATIONS.md                  # Translation sync reference
├── .gitignore
└── .nojekyll
```

## Locales

| Locale | Path | Pages |
|--------|------|-------|
| English | `/` | index, privacy, custom-common-plants |
| Spanish | `/es/` | index, privacy, custom-common-plants |
| Chinese (Simplified) | `/zh/` | index, privacy, custom-common-plants |

All pages include `hreflang` alternate links for SEO. Language switcher in the top-left of each page.

## Translation sync

When editing content, update all three locales. See `TRANSLATIONS.md` for string mapping.

## Hosting

Cloudflare Pages — no build command, serves static files directly. Security headers configured in `_headers`.

### Security headers (`_headers`)

- **CSP**: Restricts scripts/styles/fonts/images to self + Google Fonts + Apple badge CDN
- **X-Frame-Options**: DENY (no iframe embedding)
- **X-Content-Type-Options**: nosniff
- **Referrer-Policy**: strict-origin-when-cross-origin
- **Permissions-Policy**: camera, microphone, geolocation all disabled

## Scripts

**Compress PNGs (pngquant 90%)** — pass the file(s) or glob so you only run it on what you need (avoid re-compressing already quantized images):

```bash
pngquant --quality=90-100 --ext .png --force <files-or-glob>
```

## Content

- **Hero**: App name, tagline, description; lang switcher and App Store badge (alternative white, links to `#download`) top right.
- **App Preview**: 6 screenshots in responsive grid (6 columns desktop, 3 tablet, auto-fill mobile)
- **Features** (9 cards): Plants & Collections (AI + ML identification), Watering & Calendar, Care Journal & Photos, Sightings & Map, Home Screen Widgets (Up Next + Calendar + Scan & Identify), Reminders, Sharing (plant cards, Share Extension, ICS export), Your Data (iCloud, ZIP export/import, Spotlight), Language & Settings
- **Why Choose** (5 highlights): Works without internet, adapts to your seasons, beyond the garden, one app every device, own your data
- **Guides**: Link to custom common plants source guide
- **Download**: Section `id="download"` with app icon, App Store + Mac App Store badges, version, system requirements
- **Support**: Contact email, system requirements
- **Footer**: Copyright, privacy policy link
- **Platforms**: iPhone, iPad, Mac (Catalyst)
- **App Store**: [iOS](https://apps.apple.com/us/app/plantfolio-plus/id6757148663) · [Mac](https://apps.apple.com/us/mac-app/plantfolio-plus/id6757148663)

## Fonts

[DM Sans](https://fonts.google.com/specimen/DM+Sans) (body) and [Outfit](https://fonts.google.com/specimen/Outfit) (headings) loaded from Google Fonts. System font fallback: `-apple-system, BlinkMacSystemFont, sans-serif`.

## Design

- CSS custom properties in `:root` for colors, spacing, and border radius
- Primary color: `#166534` (dark green)
- Responsive breakpoints: 960px (desktop), 768px (tablet), 480px (mobile)
- Drop-shadow filters on screenshots (CSS, follows image alpha)
- No external CSS/JS frameworks
