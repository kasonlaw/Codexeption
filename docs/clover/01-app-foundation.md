# Phase 1 — App Foundation

## Goal

Set up a local Next.js app that Clover will run on.

This phase should NOT include any complex product logic.

---

## Requirements

- Next.js App Router project
- TypeScript enabled
- Tailwind CSS (or equivalent)
- Local SQLite setup (Drizzle or Prisma)
- Basic folder structure

---

## Required structure

```
/app
/components
/lib
/local-data
/docs
```

---

## Tasks

1. Create Next.js project.
2. Add TypeScript.
3. Install Tailwind CSS.
4. Set up SQLite connection.
5. Create placeholder DB schema file.
6. Create homepage `/`.

---

## Homepage

The homepage should render:

- simple centered layout
- text: "Clover MVP"

---

## Constraints

Do NOT implement:

- outfit rendering
- wardrobe upload
- recommendation engine
- weather API
- calendar
- image processing

---

## Done criteria

- `npm run dev` starts the app
- `/` route loads successfully
- project structure matches spec
- no runtime errors

---

## After completion

Proceed to Phase 2 — Static Outfit Prototype.
