# arken/packages/forge/packages/ANALYSIS.md

## Folder
`arken/packages/forge/packages`

## Purpose
- Container for Forge package submodule (`web`).

## Key files
- `README.md`
- child path: `web/` (submodule initialized in this run)

## Child summary (latest chunk)
- `web/src/modules/royale` contains placeholder module files (`royale.router.ts`, `royale.service.ts`) with no executable code.
- Active Royale runtime path currently lives outside `src/modules`:
  - `web/src/views/royale/index.tsx`
  - `web/src/components/Royale.tsx`
  - `web/src/hooks/useWindows.tsx` route registration.
- New `web/src/views/games/infinite` leaf analysis confirms route shell + tutorial/static-data composition, with core runtime delegated to shared component layer.
- Extended leaf-first analysis into `web/src/views/games/evolution/{leaderboard,tournament}`; identified leaderboard as a monolithic view with direct remote polling and query-state orchestration.
- Added `web/src/views/games/isles/{README.md,ANALYSIS.md}` after source-level read of `isles/index.tsx` (thin wrapper over `~/components/MemeIsles`).
- Added `web/src/views/games/oasis/{README.md,ANALYSIS.md}` after full route-source read; identified wrapper-heavy topology with a monolithic `tutorial.tsx` outlier.
- Added `web/src/components/{README.md,ANALYSIS.md}` with a focused deep-dive on `MemeIsles.tsx` as a high-risk transport/runtime ownership surface.
- Added `web/src/components/Sanctuary/{README.md,ANALYSIS.md}` after full source read of Sanctuary components; documented Oasis runtime ownership and mixed data authority across generated node JSON, Envoy fetches, and seer tRPC hooks.

## Risks
- Architectural drift between intended module boundaries and actual runtime behavior.
- Live-event/socket logic in UI component scope increases protocol-hardening test friction.

## Next test/protocol checks
- Run `web` typecheck/tests for regression baseline.
- Add targeted tests for Royale filter/state-transition behavior after extraction into testable utilities.
