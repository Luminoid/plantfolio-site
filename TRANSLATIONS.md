# Translation Sync Reference

Keep EN, ES, ZH-Hans, and ZH-Hant content aligned. When updating one locale, update all four.

## Locale paths

| Locale | Index | Custom Plants | Privacy |
|--------|-------|---------------|---------|
| EN | `index.html` | `custom-common-plants.html` | `privacy.html` |
| ES | `es/index.html` | `es/custom-common-plants.html` | `es/privacy.html` |
| ZH-Hans | `zh/index.html` | `zh/custom-common-plants.html` | `zh/privacy.html` |
| ZH-Hant | `zh-Hant/index.html` | (none) | `zh-Hant/privacy.html` |

## Index page strings

| Key | EN | ES | ZH |
|-----|----|----|-----|
| app_name | Plantfolio Plus | Plantfolio Plantas | Plantfolio 植物志 |
| section_features | What You Can Do | Qué puedes hacer | 你可以做什么 |
| section_highlights | Why Plantfolio Plus | Por qué Plantfolio Plantas | 为什么选 Plantfolio 植物志 |
| section_instructions | Instructions | Instrucciones | 使用说明 |
| section_support | Support | Soporte | 联系与支持 |
| btn_ios_download | Download on the App Store | Disponible en App Store | App Store 下载 |
| btn_mac_download | Download on the Mac App Store | Disponible en Mac App Store | Mac App Store 下载 |
| footer_privacy | Privacy Policy | Política de Privacidad | 隐私政策 |

## Feature cards (9 total)

Same structure in all locales, in this order: Plants & Collections, Watering & Calendar, Care Journal & Photos, Sightings & Map, Reminders, Home Screen Widgets, Sharing, Language & Settings, Your Data & Privacy.

## Highlight items (3 total)

Trimmed to differentiators not already covered by the feature cards.

1. Works without internet / Funciona sin internet / 离线也能用
2. One app, every device / Una app, todos los dispositivos / 一个应用，所有设备
3. Private by design / Privada por diseño / 隐私至上

## Sync checklist

When editing content:

- [ ] Update `index.html` (EN)
- [ ] Update `es/index.html` (ES)
- [ ] Update `zh/index.html` (ZH-Hans)
- [ ] Update `zh-Hant/index.html` (ZH-Hant)
- [ ] If custom-common-plants: update EN/ES/ZH-Hans (no ZH-Hant page)
- [ ] If privacy: update all 4
- [ ] Verify lang switcher links and hreflang alternates
