# Clover Development Workflow Instructions

These instructions define how Codex should work when developing Clover.

Clover is developed through a docs-based phase queue. Each phase document describes the next implementation target, validation checks, and done criteria.

---

## Workflow mode

Use an iterative engineering workflow:

- read the phase queue,
- complete the current phase,
- validate the implementation,
- commit coherent changes,
- then continue to the next phase when the execution environment supports it.

The implementation may refactor earlier code when it improves correctness, simplicity, maintainability, or future compatibility.

---

## Refactor rules

Refactoring is allowed when:

- current architecture blocks the active phase,
- duplicated logic appears,
- component boundaries are unclear,
- type definitions are drifting,
- schema names conflict with future phases,
- rendering code becomes difficult to extend,
- tests reveal brittle implementation,
- a simpler implementation can satisfy the same requirements.

Do not refactor only for cosmetic preference. Each refactor should support a phase goal, reduce complexity, or prepare a necessary future path.

---

## Development sequence

Start with `docs/clover/README.md`.

Then proceed in this order:

1. `00-product-architecture.md`
2. `01-app-foundation.md`
3. `02-static-outfit-prototype.md`
4. `03-data-model-local-storage.md`
5. `04-recommendation-engine.md`
6. `05-weather-calendar-context.md`
7. `06-wardrobe-ingestion-mvp.md`
8. `07-model-privacy-flow.md`
9. `08-photorealistic-tryon-prep.md`
10. `09-testing-polish.md`

---

## Completion protocol for each phase

For each phase:

1. Read the phase file fully.
2. Check current repo state.
3. Implement the smallest complete version of the phase.
4. Refactor when it helps the current or next phase.
5. Run available checks.
6. Fix errors.
7. Update docs only when implementation meaningfully changes the plan.
8. Commit changes.
9. Continue to the next phase if the environment supports continuous execution.

---

## Validation hierarchy

Prefer these checks, depending on what exists:

1. `npm run lint`
2. `npm run typecheck`
3. `npm test`
4. `npm run test`
5. `npm run build`
6. phase-specific tests

If scripts do not exist yet, add useful scripts when appropriate.

---

## Product priorities

Clover's priority order:

1. useful outfit decision loop,
2. local-first privacy,
3. instant modular swapping,
4. deterministic explainable recommendations,
5. future photorealistic try-on readiness,
6. visual polish.

Do not reverse this order.

---

## What to avoid

Do not start with:

- production auth,
- cloud sync,
- Google Calendar OAuth,
- full AI image generation,
- local diffusion,
- complex mask painting,
- marketplace or shopping features,
- social sharing,
- mobile native app.

These are outside the MVP queue.

---

## Photorealistic final direction

The final product direction is photorealistic try-on.

However, live generation should not be required for every outfit change.

The future architecture is:

1. create or upload a consistent user model,
2. lock pose, camera, framing, and lighting,
3. generate item-specific try-on assets,
4. remove background and isolate wearable layer,
5. align the transparent layer to the model,
6. reuse it instantly in the preview renderer.

The MVP should keep data structures and renderers ready for this pipeline.

---

## Commit style

Use concise commits such as:

- `Add Clover app foundation`
- `Add static outfit renderer`
- `Add local data schema`
- `Add recommendation scoring engine`
- `Add weather and calendar context`
- `Add wardrobe ingestion flow`

---

## Stop conditions

Stop and report instead of continuing if:

- package installation is impossible,
- tests cannot run due to missing environment assumptions,
- a destructive migration would delete user data,
- external API keys are required unexpectedly,
- implementation requires user photos or private assets that are not present.

For non-blocking uncertainty, make a reasonable local-first assumption and continue.
