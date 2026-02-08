# plantfolio-site

Static marketing site for [Plantfolio Plus](https://apps.apple.com/us/app/plantfolio-plus/id6757148663). Landing page, features, and privacy policy. No build step—plain HTML and CSS.

## Structure

```
plantfolio-site/
├── index.html          # English landing (root)
├── privacy.html        # English privacy policy
├── styles.css          # Shared styles
├── es/                 # Spanish
│   ├── index.html
│   └── privacy.html
├── zh/                 # Chinese (Simplified)
│   ├── index.html
│   └── privacy.html
├── .nojekyll           # GitHub Pages
└── .cursor/            # Cursor context and rules
```

## Locales

| Locale | Path |
|--------|------|
| English | `/` (index.html, privacy.html) |
| Spanish | `/es/` |
| Chinese (Simplified) | `/zh/` |

## Content

- **Features**: Plants & Collections, Watering & Calendar, Photos, Reminders, Care Logs, Your Data (export/import, iCloud)
- **Highlights**: Seasonal watering, plant care library, collections, data control
- **App Store**: [Plantfolio Plus](https://apps.apple.com/us/app/plantfolio-plus/id6757148663)

Feature alignment with the app: site highlights match app capabilities. Widgets and Mac Catalyst are app-only and not emphasized on the site.

## Context & Rules

- **Context**: [.cursor/CONTEXT.md](.cursor/CONTEXT.md) — project overview, structure, conventions
- **Rules**: [.cursor/rules/](.cursor/rules/) — HTML/CSS conventions

## Ecosystem

Part of the Plantfolio ecosystem. See [Projects/README.md](../README.md). If hosting plantfolio-common-plants for custom URL, serve at `/plantfolio-common-plants/` per the plantfolio-common-plants README.
