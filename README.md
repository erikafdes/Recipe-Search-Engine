# 🌿 Savory — Recipe Search Engine

**CODTECH Internship — Project 4 (Task 4)**

## Intern Details
| Field | Detail |
|---|---|
| **Intern ID** | *[Add your CODTECH Intern ID here]* |
| **Full Name** | Erika |
| **Domain** | Web Development |
| **Duration** | *[Add number of weeks here]* |
| **Project Name** | Savory — Recipe Search Engine |

## Project Scope
Savory is a single-page recipe search engine that lets users discover real recipes by name, ingredient keyword, category, or cuisine (area). It's built as a self-contained HTML file — no build step, no server, no API key required — and is powered live by the free [TheMealDB](https://www.themealdb.com/api.php) public API.

The project focuses on a warm, editorial "recipe card" aesthetic (sage/emerald/lavender palette, Playfair Display + Inter typography), a fully responsive layout, and a genuinely usable cooking experience: an ingredient checklist you can tick off while you cook, one-click favorites saved to your browser, and a light/dark theme toggle.

## Features
- 🔍 **Live search** — search TheMealDB's full catalog by dish name or ingredient keyword
- 🗂️ **Filter by category & cuisine** — dropdowns populated dynamically from the API; combinable filters
- 🎲 **Surprise Me** — fetches a random recipe
- 💡 **Quick suggestion chips** — one-tap searches for popular dishes
- 📖 **Recipe detail modal** — full ingredient list with quantities, a checkable "pantry" checklist, step-by-step instructions, and links to the original source / YouTube video when available
- ❤️ **Favorites** — save recipes locally (`localStorage`) and filter the grid to favorites-only
- 🌗 **Light / dark mode** — toggle with preference saved across visits
- 💀 **Loading skeletons, empty states & error states** — no blank screens while data loads or fails
- 📱 **Fully responsive** — from mobile to desktop
- ♿ **Accessible** — visible keyboard focus states, semantic markup, respects `prefers-reduced-motion`

## Tech Stack
- **HTML5 / CSS3** — single self-contained file, CSS custom properties for theming
- **Vanilla JavaScript (ES6+)** — no frameworks, no build tools
- **[TheMealDB API](https://www.themealdb.com/api.php)** — free tier, test key `1`
- **Google Fonts** — Playfair Display (display) + Inter (body/UI)
- **Browser `localStorage`** — persists favorites and theme preference

## Project Structure
```
recipe-search-engine/
├── index.html          # Complete application (structure + styles + logic)
├── README.md            # This file
└── screenshots/          # Output screenshots (add your own before submitting)
```

## How to Run
1. Download or clone this repository.
2. Open `index.html` directly in any modern browser (Chrome, Edge, Firefox, Safari).
3. That's it — no installation, no `npm install`, no server needed. An internet connection is required so the app can reach the TheMealDB API.

## API Reference (TheMealDB, test key `1`)
| Purpose | Endpoint |
|---|---|
| Search by name/keyword | `search.php?s=<query>` |
| List all categories | `list.php?c=list` |
| List all cuisines/areas | `list.php?a=list` |
| Filter by category | `filter.php?c=<category>` |
| Filter by cuisine | `filter.php?a=<area>` |
| Full recipe details | `lookup.php?i=<id>` |
| Random recipe | `random.php` |

## Notes
- TheMealDB's free tier supports filtering by **one** dimension (category *or* area) per request. When both filters are selected, the app fetches candidates by category and cross-checks each recipe's cuisine to combine both filters client-side.
- No API key/signup is needed — this project uses the publicly documented test key (`1`), suitable for development and educational use.

---
Built by Erika as part of the CODTECH internship program.
