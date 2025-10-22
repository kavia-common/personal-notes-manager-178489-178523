# Ocean Notes (Astro)

A simple notes manager built with Astro. Create, read, update, and delete notes with a clean Ocean Professional theme. Data is persisted in your browser using localStorage—no backend required.

## Features
- Notes list with search by title
- Create and edit notes in a modal editor
- Delete with confirmation
- Smooth transitions, rounded corners, subtle shadows
- Responsive layout with sidebar and header
- Theme toggle (light/dark) via the existing ThemeToggle component

## Run locally
- Port is configured to 3000 in astro.config.mjs

```bash
npm install
npm run dev
# open http://localhost:3000
```

## Data persistence
Notes are stored under the localStorage key `notes.store.v1`. You can clear site data to reset.

## Code structure
- src/pages/index.astro — Main page wiring components and client-side logic
- src/styles/theme.css — Ocean Professional theme tokens and utilities
- src/components/Header.astro — Header with global search and add button
- src/components/Sidebar.astro — Sidebar with tips and labels (static)
- src/components/NotesList.astro — (presentational island; main list is rendered client-side for simplicity)
- src/components/NoteEditorModal.astro — Accessible modal for editing notes
- src/lib/storage.ts — Note CRUD helpers using localStorage

## Accessibility
- Modal supports Esc to close and Ctrl/Cmd+S to save
- ARIA roles and labels on interactive elements
