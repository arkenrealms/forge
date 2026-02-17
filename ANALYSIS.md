# arken/packages/forge/ANALYSIS.md

## Folder
`arken/packages/forge`

## Snapshot
- Files: 7
- Subfolders: 1

## Notable contents
- files: .git, .gitignore, .gitmodules, LICENSE, NOTES.md, README.md, package.json
- dirs: packages

## Latest rotation update
- Initialized nested submodule `packages/web`.
- Completed deepest-first analysis chunk in `packages/web/src/modules/royale` and bubbled summaries through `src/modules` and `src`.
- Continued Forge rotation with deepest-first pass in `packages/web/src/views/games/infinite` and added new `README.md` + `ANALYSIS.md` rollups for `views`, `views/games`, and `views/games/infinite`.
- Added next Forge leaf-first pass in `packages/web/src/views/games/evolution/{leaderboard,tournament}` with new leaf docs and parent rollups.
- Added `packages/web/src/views/games/isles/{README.md,ANALYSIS.md}` from direct `isles/index.tsx` analysis and bubbled summary updates to parent docs.
- Added `packages/web/src/components/{README.md,ANALYSIS.md}` and traced Isles runtime ownership into `components/MemeIsles.tsx` (socket + Unity + wallet lifecycle coupling).
- Added `packages/web/src/views/games/oasis/{README.md,ANALYSIS.md}` after reading Oasis route sources directly; captured wrapper-vs-monolith split around `tutorial.tsx`.
- Added `packages/web/src/components/Sanctuary/{README.md,ANALYSIS.md}` from a full component-level pass; confirmed Oasis routes are mostly thin wrappers over Sanctuary components that currently mix static generated data, direct Envoy fetches, and seer tRPC queries.
- Added `packages/web/src/components/guilds/{README.md,ANALYSIS.md}` from a guild-component pass; documented TeamCard profile query coupling to Seer, loose typing/dead-code debt, and profile-status rendering ambiguity.
- Added `packages/web/src/components/Menu/icons/{README.md,ANALYSIS.md}` from a menu-icons pass; documented mostly static SVG icon ownership and `Logo.tsx` browser-coupled load-timing/styling behavior as the outlier.
- Added `packages/web/src/views/royale/{README.md,ANALYSIS.md}` from a direct route-source pass; confirmed route layer is a thin active-gate wrapper over `components/Royale` runtime ownership.
- Added `packages/web/src/components/Menu/components/{README.md,ANALYSIS.md}` from a menu runtime-component pass; documented wallet/account modal bridge ownership, nav config rendering flow, and typing/imperative-navigation testability gaps.
- Added `packages/web/src/components/Logo/{README.md,ANALYSIS.md}` from direct source analysis of `Logo/index.tsx`; documented multi-source logo fallback behavior, module-global failed-src suppression tradeoffs, and lightweight typing gaps.
- Added `packages/web/src/components/Menu/{README.md,ANALYSIS.md}` from direct source analysis of menu root primitives (`Menu.tsx`, `config.ts`, `theme.ts`, `types.ts`); documented dormant container ownership and duplicated social-config entries.
- Added `packages/web/src/hooks/{README.md,ANALYSIS.md}` from direct hook-layer analysis (`useWindows`, `useAuth`, `useWeb3`, `useNotice`, `useLive`, `index`); documented monolithic route-registry/auth coupling and loose typing risks.

## Next actions
- Continue chunked analysis in next Forge leafs (`web/src/views/*`, `web/src/hooks/*`, or remaining `web/src/components/*` leaves) while preserving bottom-up rollups.
- Add targeted protocol/reliability notes where frontend transport handling is coupled to view components.
