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

## Next actions
- Continue chunked analysis in next Forge leafs (`web/src/views/*` or `web/src/hooks/*`) while preserving bottom-up rollups.
- Add targeted protocol/reliability notes where frontend transport handling is coupled to view components.
