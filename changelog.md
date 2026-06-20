# Changelog

## 2026-06-20 - Slovak localization + UI/UX theme improvements

### Slovak localization completed

A complete Slovak localization package was finalized and prepared for contribution.

- Localization scope: 9 translation files
- Total translated entries: 994

Breakdown:

- `localization/sk_SK/strings.po`: 768
- `localization/sk_SK/demo_data.po`: 117
- `localization/sk_SK/locales.po`: 34
- `localization/sk_SK/permissions.po`: 31
- `localization/sk_SK/userfield_types.po`: 15
- `localization/sk_SK/stock_transaction_types.po`: 10
- `localization/sk_SK/chore_period_types.po`: 8
- `localization/sk_SK/component_translations.po`: 6
- `localization/sk_SK/chore_assignment_types.po`: 5

Additionally added Slovak translations for newly introduced UI strings related to night mode theme variants in `localization/sk_SK/strings.po`.

### Night mode redesign and theme variants

Night mode was redesigned to feel less sterile and more aligned with a sustainable, warm visual identity.

Implemented per-user night mode theme selection (radio buttons in View settings):

- Forest organic (default)
- Clean modern
- Calm premium

Technical changes:

- Added user setting default:
  - `night_mode_theme = forest-organic`
  - file: `config-dist.php`
- Added night mode theme selector in the UI:
  - file: `views/layout/default.blade.php`
- Added JS logic for dynamic stylesheet switching by selected user profile theme:
  - file: `public/js/grocy_nightmode.js`
- Added two new night mode variant stylesheets:
  - `public/css/grocy_night_mode_clean_modern.css`
  - `public/css/grocy_night_mode_calm_premium.css`
- Extended server-side initial stylesheet loading so selected variant is applied immediately after page load:
  - file: `views/layout/default.blade.php`

### General UI polish

Improved readability and visual quality in base styling:

- Better text rhythm and rendering (`line-height`, subtle `letter-spacing`, antialiasing)
- Slightly increased content text readability
- Improved spacing in forms and headers
- Unified softer border radii for controls/cards/modals/dropdowns
- Subtle card elevation/hover polish

Main files:

- `public/css/grocy.css`
- `public/css/grocy_night_mode.css`

### UX details

Added short explanatory descriptions under each night mode theme option to make profile selection easier.

Location:

- `views/layout/default.blade.php`

---

Prepared as a contribution summary for the upstream Grocy author.
