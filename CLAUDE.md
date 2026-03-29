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
- `amount` is stored as a string, so `reduce` on `totalIncome`/`totalExpenses` uses string concatenation instead of numeric addition
- "Freelance Work" is marked `type: "income"` in the seed data but has `category: "salary"` and is rendered as an expense in the UI (type mismatch bug)
- No delete functionality
- Minimal styling with no responsive design
