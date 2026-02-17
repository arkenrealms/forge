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
- Added `web/src/components/guilds/{README.md,ANALYSIS.md}` after full source read of guild cards/components; documented Forge↔Seer profile-query contract coupling, loose typing (`team: any`), and status/icon semantics drift risk.
- Added `web/src/components/Menu/icons/{README.md,ANALYSIS.md}` after source read of menu icon files; documented static SVG ownership and `Logo.tsx` browser-coupled timing/styling outlier risks.
- Added `web/src/views/royale/{README.md,ANALYSIS.md}` after source read of `royale/index.tsx`; confirmed the route is a thin activation wrapper delegating runtime behavior to `components/Royale`.
- Added `web/src/components/Logo/{README.md,ANALYSIS.md}` after source read of `Logo/index.tsx`; documented global failed-URL suppression behavior, fallback semantics, and typing/observability gaps.
- Added `web/src/components/Menu/{README.md,ANALYSIS.md}` after source read of `Menu.tsx`, `config.ts`, `theme.ts`, and `types.ts`; documented dormant top-level container behavior and menu-config duplication drift.

## Risks
- Architectural drift between intended module boundaries and actual runtime behavior.
- Live-event/socket logic in UI component scope increases protocol-hardening test friction.

## Next test/protocol checks
- Run `web` typecheck/tests for regression baseline.
- Add targeted tests for Royale filter/state-transition behavior after extraction into testable utilities.
