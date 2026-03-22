# Aveola.live Quiz Funnel

A polished, bilingual (EN/ES) quiz funnel built with React + Vite. It keeps the existing quiz logic/branching and now presents it in a premium iPhone-style onboarding flow.

## Highlights
- iPhone-first layout with centered device frame on desktop
- Visible EN/ES toggle + browser-language detection (Spanish browsers load ES by default)
- Age split branches (25–35, 36–55) with unchanged quiz content and CTA to https://aveola.live/cab/video-chat/
- Strong top bar with back arrow + step counter, slim animated progress bar, large centered questions, stacked rounded answer cards
- Smooth fade/slide transitions, animated progress updates, tap-friendly states, back navigation with preserved answers
- Lightweight analytics hook placeholders (`src/utils/analytics.js`)
- Quiz copy and structure centralized in `src/data/quizConfig.js`

## Getting Started
1. **Install dependencies**
   ```bash
   npm install
   ```
2. **Run locally (dev server)**
   ```bash
   npm run dev
   ```
   Open the printed localhost URL (default http://localhost:5173).
3. **Build for production**
   ```bash
   npm run build
   ```
   Output goes to `dist/`.
4. **Preview the production build**
   ```bash
   npm run preview
   ```

## Deploying
- **Vercel**: Import the repo, framework auto-detects Vite. Build command: `npm run build`. Output dir: `dist`.
- **Netlify**: New site from Git. Build command: `npm run build`. Publish directory: `dist`.
- **GitHub Pages**: Run `npm run build` and publish `dist` (e.g., `npm install -g serve` then `serve dist`, or use `gh-pages`).

## Customizing
- Update quiz text, branching, and translations in [`src/data/quizConfig.js`](/Users/ilakaspruk/Documents/New%20project/src/data/quizConfig.js).
- Visual system (colors, typography, radii, shadows, animations) lives in [`src/styles/global.css`](/Users/ilakaspruk/Documents/New%20project/src/styles/global.css). Top tokens are in `:root`.
- Hero/bridge imagery: swap the Unsplash URLs in `.hero-image` and `.bridge-image` (same CSS file) with your own asset or local file in `public/` (e.g. `url('/hero.jpg')`).
- Typography: heading/body use Plus Jakarta Sans + Inter via Google Fonts; change the `@import` in `global.css` if you prefer different pairings.
- Swap analytics in [`src/utils/analytics.js`](/Users/ilakaspruk/Documents/New%20project/src/utils/analytics.js).
- Language toggle renders only on the intro screen; styles for it remain in `global.css` (`.language-row-intro`).

## Notes
- Single-page frontend; no backend required.
- Mobile-first with a centered phone-like shell on desktop.
- Accessibility: semantic elements, focus states, keyboard navigation, reduced-motion support.
