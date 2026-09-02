# Chapter Seventeen

An interactive 13-chapter romantic storybook web app — a personal gift, built as a single-page-at-a-time experience with flip cards, quizzes, a vision board, secret messages, a love letter, and a grand finale reveal.

**Live:** https://tanmaykhariwal.github.io/ChapterSeventeen/

## Tech Stack

- [React 19](https://react.dev/) + [TypeScript](https://www.typescriptlang.org/)
- [Vite 6](https://vitejs.dev/) for dev/build tooling
- [Tailwind CSS v4](https://tailwindcss.com/)
- [Framer Motion](https://motion.dev/) (`motion/react`) for page transitions and micro-interactions
- [lucide-react](https://lucide.dev/) for icons
- [canvas-confetti](https://github.com/catdad/canvas-confetti) for celebration effects

## Getting Started

```bash
npm install
npm run dev
```

The dev server starts on port 3000 by default and auto-falls-back to a free port if it's taken.

## Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start the Vite dev server |
| `npm run build` | Production build to `dist/` |
| `npm run preview` | Preview the production build locally |
| `npm run lint` | Type-check with `tsc --noEmit` |
| `npm run clean` | Remove `dist/` |

## Deployment

Pushing to `main` triggers [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml), which builds the app and publishes `dist/` to GitHub Pages automatically. One-time setup on GitHub: **Settings → Pages → Source → GitHub Actions**.

## Project Structure

```
src/
  App.tsx                 # Page navigation, transitions, wheel/touch/keyboard handling
  components/              # Shared UI (NavigationHUD, ErrorBoundary, KeepsakeModal, ...)
  components/pages/        # One component per chapter (Page1Hero ... Page13GrandFinale)
  data/chaptersData.ts     # Chapter metadata and per-chapter content
  utils/                   # Audio, haptics, and confetti helpers
```
