# Portfolio Frontend

Single-page personal portfolio for **Siva Sakthi Velan R** — a dark, cyberpunk-inspired site with an animated anime character, typewriter speech bubbles, and sections for skills, experience, projects, and contact.

Built with React 19, Tailwind CSS, and Framer Motion. Content is driven from a single data file for easy updates without touching component logic.

## Features

- **Hero** — SVG anime character with float/blink animations and cycling typewriter taglines
- **About** — Profile summary, pillars, and animated stat counters
- **Skills** — Bento-style grid with categorized tech chips
- **Experience** — Vertical timeline across companies
- **Projects** — Filterable gallery (Delivered + AI Lab projects)
- **Achievements** — Awards and education cards
- **Contact** — Email, phone, LinkedIn, and location with copy-to-clipboard (no form)
- **Responsive** — Mobile-friendly layout with smooth scroll navigation

## Tech Stack

| Layer | Tools |
|---|---|
| Framework | React 19, React Router 7 |
| Styling | Tailwind CSS 3, PostCSS, custom CSS animations |
| Motion | Framer Motion |
| Icons | Lucide React |
| Fonts | Azeret Mono, Manrope (Google Fonts) |
| Data fetching | TanStack React Query (ready for API integration) |
| Build | Create React App 5 + CRACO |

## Project Structure

```
frontend/
├── public/
│   └── index.html          # HTML shell
├── src/
│   ├── components/
│   │   └── portfolio/      # Section components (Hero, About, Skills, …)
│   ├── data/
│   │   └── portfolio.js    # Profile, skills, projects, experience, etc.
│   ├── App.js              # Route + page layout
│   ├── App.css
│   ├── index.js            # React entry + QueryClient provider
│   └── index.css           # Tailwind directives + global theme
├── craco.config.js         # Webpack @ path alias
├── postcss.config.js
├── tailwind.config.js
├── jsconfig.json           # IDE support for @/ imports
└── package.json
```

## Getting Started

### Prerequisites

- Node.js 18+ (Node 20+ recommended)
- npm or Yarn

### Install

```bash
cd frontend
npm install
```

### Development

```bash
npm start
```

Runs at [http://localhost:3000](http://localhost:3000) with hot reload.

### Production Build

```bash
npm run build
```

Output is written to `build/`:

```
build/
├── index.html
└── static/
    ├── css/
    └── js/
```

### Run Tests

```bash
npm test
```

## Environment Variables

Create a `.env` file in the `frontend/` directory:

```env
REACT_APP_BACKEND_URL=http://localhost:8000
ENABLE_HEALTH_CHECK=false
```

| Variable | Description |
|---|---|
| `REACT_APP_BACKEND_URL` | Base URL for the FastAPI backend (optional; used when API features are enabled) |
| `ENABLE_HEALTH_CHECK` | Reserved for health-check integrations |

> Only variables prefixed with `REACT_APP_` are exposed to the browser. Never commit secrets.

## Updating Content

Most site content lives in `src/data/portfolio.js`:

- `profile` — name, title, contact links, taglines
- `stats` — animated counters in About
- `skills` — skill groups and chips
- `experience` — work history timeline
- `projects` — project cards with `type: "delivered"` or `"ai-lab"`
- `achievements`, `education` — awards and degrees

After editing, save the file — the dev server will hot-reload.

## Path Aliases

Imports use the `@/` alias mapped to `src/`:

```js
import Hero from "@/components/portfolio/Hero";
import { profile } from "@/data/portfolio";
```

Configured in `craco.config.js` and `jsconfig.json`.

## Deployment

The `build/` folder is a static site suitable for:

- **GitHub Pages**
- **Netlify / Vercel**
- **AWS S3 + CloudFront**
- Any static file host

### GitHub Pages (project site)

If deploying to `https://<username>.github.io/<repo-name>/`, add to `package.json`:

```json
"homepage": "https://<username>.github.io/<repo-name>"
```

Then rebuild so asset paths resolve correctly:

```bash
npm run build
```

Deploy the **contents** of `build/` (not the `frontend/` folder itself).

> GitHub Pages serves static files only. The FastAPI backend must be hosted separately if you enable API features.

## Scripts

| Command | Description |
|---|---|
| `npm start` | Start development server |
| `npm run build` | Create optimized production build |
| `npm test` | Run test suite in watch mode |

## Related

- Backend API: see `../backend/` (FastAPI + MongoDB)
- Product requirements: see `../PRD.md`
