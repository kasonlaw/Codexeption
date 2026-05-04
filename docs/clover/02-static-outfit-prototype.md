# Phase 2 — Static Outfit Prototype

## Goal

Render a mannequin with modular clothing layers and allow instant slot swapping.

This phase proves the core visual interaction.

---

## Requirements

- Base model (mannequin image)
- 3 tops
- 3 bottoms
- 3 shoes
- Layered rendering system
- Slot controls

---

## Tasks

1. Create `OutfitCanvas` component.
2. Render base model.
3. Add layered images:
   - bottom
   - top
   - shoes
4. Add hardcoded anchor positions.
5. Create slot controls:
   - change top
   - change bottom
   - change shoes
6. Ensure slot changes do NOT affect other layers.

---

## Constraints

Do NOT implement:

- database
- API routes
- recommendation logic
- uploads
- weather

---

## Done criteria

- mannequin is visible
- clothing layers stack correctly
- slot swapping is instant
- each slot changes independently

---

## After completion

Proceed to Phase 3 — Data Model and Local Storage.
