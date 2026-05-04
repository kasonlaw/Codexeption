# Clover Development Queue

Clover is a local-first outfit suggestion and visual try-on system.

The MVP should prove the outfit decision loop first:

1. show a model/mannequin,
2. render modular outfit layers,
3. allow instant slot swapping,
4. recommend outfits using weather, mock calendar context, and wear history,
5. preserve the future path toward photorealistic AI-generated try-on layers.

The name **Clover** does not need to be prominent in the UI. It may appear subtly in a side menu, settings panel, app metadata, or internal docs.

---

## How Codex should use this queue

Work through the phase docs in order.

After finishing one phase:

1. run the required checks,
2. update the phase checklist if possible,
3. commit the implementation,
4. move to the next phase document.

Do not jump ahead unless the current phase explicitly requires preparation for a later phase.

---

## Queue

| Order | Phase | File | Goal |
|---:|---|---|---|
| 0 | Product architecture | [`00-product-architecture.md`](./00-product-architecture.md) | Understand Clover's product and technical direction |
| 1 | App foundation | [`01-app-foundation.md`](./01-app-foundation.md) | Create the local Next.js app foundation |
| 2 | Static outfit prototype | [`02-static-outfit-prototype.md`](./02-static-outfit-prototype.md) | Render mannequin + modular seed clothing layers |
| 3 | Data model and local storage | [`03-data-model-local-storage.md`](./03-data-model-local-storage.md) | Add SQLite schema, seed data, and file structure |
| 4 | Recommendation engine | [`04-recommendation-engine.md`](./04-recommendation-engine.md) | Build deterministic outfit scoring and reason generation |
| 5 | Weather and mock calendar | [`05-weather-calendar-context.md`](./05-weather-calendar-context.md) | Add Open-Meteo and local mock calendar context |
| 6 | Wardrobe ingestion MVP | [`06-wardrobe-ingestion-mvp.md`](./06-wardrobe-ingestion-mvp.md) | Add upload, metadata editing, and review flow |
| 7 | Model and privacy flow | [`07-model-privacy-flow.md`](./07-model-privacy-flow.md) | Add model asset handling and privacy controls |
| 8 | Photorealistic try-on preparation | [`08-photorealistic-tryon-prep.md`](./08-photorealistic-tryon-prep.md) | Prepare the asset-generation pipeline for final product |
| 9 | Testing and polish | [`09-testing-polish.md`](./09-testing-polish.md) | Add tests, polish, and acceptance checks |

---

## Non-negotiable build principle

Do not block the MVP on segmentation, local diffusion, AI generation, OAuth, authentication, or production cloud sync.

Clover should first become a useful local outfit planner. The photorealistic AI try-on pipeline comes later as an upgrade to the asset layer system.
