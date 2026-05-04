# Phase 00 — Product Architecture

## Goal

Understand Clover's product direction and technical structure before implementation.

---

## Product summary

Clover is a local-first outfit suggestion system.

MVP:
- modular outfit preview
- deterministic recommendations
- local storage

Final direction:
- photorealistic try-on
- AI-generated clothing layers
- reusable modular assets

---

## Core architecture

Clover is composed of 4 systems:

1. Wardrobe Library
2. Context Engine (weather + calendar)
3. Recommendation Engine
4. Preview Renderer

---

## Key rule

Do not generate full outfit images on every interaction.

Instead:

- use reusable modular layers
- swap instantly
- generate assets offline when needed

---

## Future pipeline (important)

1. user model (fixed pose)
2. AI generate clothing-on-model
3. remove background
4. extract layer
5. align to anchors
6. reuse instantly

---

## Done criteria

- developer understands system direction
- no code required

---

## After completion

Proceed to Phase 01 — App Foundation
