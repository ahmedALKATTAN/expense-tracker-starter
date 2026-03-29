# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm install       # Install dependencies
npm run dev       # Start dev server at http://localhost:5173
npm run build     # Production build
npm run lint      # Run ESLint
npm run preview   # Preview production build
```

## Architecture

This is a single-component React app (Vite + React 19). All logic lives in `src/App.jsx` — there are no child components, routing, or external state management.

**Known bugs and issues (intentional — this is a course starter project):**
- "Freelance Work" is marked `type: "expense"` in the seed data but should be `type: "income"` (type mismatch bug — not yet fixed)
- Minimal styling with no responsive design

**Fixed:**
- `amount` values are now stored as numbers; `parseFloat` used in reduce calls to ensure correct numeric addition
- Delete button added to each transaction row with a confirmation dialog before removing
