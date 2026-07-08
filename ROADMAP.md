# ROADMAP — cowlsly_console_simple_settings_repo_03

## Status
Planning — second "quick win" build, designed to be reused across the whole app suite.

## Latest Asset / Documentation Log
- 2026-07-08 — Added `assets/images/icons/simple_settings_volume_steps_icon_transparent.svg` as the first real transparent Simple Settings icon. Added `assets/README.md` with suite-safe asset naming rules.
- 2026-07-08 — Completed Phase 1 asset set: module icon, volume/mute/warning icons, CASMEA entry icon, developer shortcut icon, and five volume-step UI badges (0–90%). Added `assets/ASSET_MANIFEST.md` with labels and phase mapping.
- 2026-07-08 — Added shared Cowlsly branding kit (`assets/branding/`) with small logo, forever-turning cogs background SVG, and `Cowlsly/BRANDING.md` suite standard.

## Purpose
A single, shared settings module that other Cowlsly apps point to or include, rather than each app rebuilding its own settings screen from scratch.

## Phase 1 Scope
- **A) Volume control**: mute, plus stepped levels (0% / 25% / 50% / 75% / 90%) — no 100% option, with a built-in hearing-damage warning for headphone/earbud use.
- **B) Base information entry screen**: the single source of truth for personal/medical info displayed by `cowlsly_console_medical_emergency_assistant_casmea_repo_02`. Note: the CASMEA app itself has no data-entry screen — entry only happens here, for security.
- **C) Developer options shortcut**: a fast-access button to developer tools, visible only if developer access has already been explicitly granted.

## Explicitly Out of Scope (for now)
- Anything beyond these three settings — additional settings are added only as other apps need them.

## Dependencies
- Consumed by `cowlsly_console_medical_emergency_assistant_casmea_repo_02` and, later, `cowlsly_console_authenticator_repo_04`.

## Current Asset Notes
- `assets/README.md` — asset naming, folder layout, and reuse notes.
- `assets/ASSET_MANIFEST.md` — labeled catalog mapping every asset to Phase 1 scope.
- `assets/branding/` — shared Cowlsly small logo + forever-turning cogs background (required in every suite repo).
- `Cowlsly/BRANDING.md` — suite-wide rules for logo embeds and cyberpunk backgrounds.
- `assets/images/icons/` — six transparent SVG icons (module, volume, mute, warning, CASMEA entry, developer shortcut).
- `assets/images/ui/volume_steps/` — five transparent step badges (0%, 25%, 50%, 75%, 90%).

## Related Documents
- See `dev/dat/doc/ROADMAP.ORIGINAL.md` for the original founding notes and full context behind this repo.