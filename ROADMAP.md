# ROADMAP — Cowlsly Simple Settings

## Mission

Provide one safe, accessible Android settings hub for the Cowlsly suite: frequently used controls first, regular Android settings shortcuts next, and sensitive/developer functions behind explicit gates.

Active and only branch: `root`.

## Current status

Phase 1 Android app exists in `app/` with Compose pages, search, usage-based ranking, system-setting intents, volume controls, CASMEA information entry, and a gated developer shortcut. The last recorded successful build used Java 21.

The complete reusable Simple Settings asset set is canonical and byte-verified in `Cowlsly/cowlsly-ui-assets-and-data-files`. `UI_ASSET_SOURCE.md` and `ui_asset_dependencies.json` define canonical paths and generated Android destinations. Existing local copies remain protected until deterministic sync and a fresh build pass.

## Phase 1 — Existing foundation

- [x] Compose application scaffold.
- [x] Paged settings catalogue and search.
- [x] Usage-based ordering.
- [x] Volume steps, mute, and hearing warning.
- [x] CASMEA information entry provider.
- [x] Explicitly gated developer shortcut.
- [x] Suite settings sync foundation.

## Phase 2 — Canonical assets and build health

- [x] Import shared branding, icons, volume controls, and animated background into the canonical UI repository.
- [x] Verify source/canonical SHA-256 and byte identity for all 16 reusable assets.
- [x] Pin immutable canonical release `acf7ffaab736283daccd286d01abf60a8f2a80a2` on branch `root`.
- [ ] Synchronise generated Android resources and write `.cowlsly_ui_generated.json`.
- [ ] Repair resource references only where generated paths differ.
- [ ] Run `./gradlew assembleDebug`, tests, and lint with Java 21.
- [ ] Add or confirm drift/checksum validation in CI.
- [ ] Remove only exact obsolete local masters after validation.

## Phase 3 — Settings reliability

- [ ] Review all Android intents and unavailable-screen fallbacks against current Android versions.
- [ ] Add unit tests for ranking, search, settings serialization, and access tiers.
- [ ] Add instrumentation tests for system-intent launch behavior.
- [ ] Version the suite settings contract and add migrations.

## Phase 4 — Security and privacy hub

- [ ] Complete PIN/biometric/session-unlock integration without storing secrets in settings exports.
- [ ] Add permissions and privacy-dashboard navigation.
- [ ] Keep account and medical information scoped, consent-aware, and encrypted where appropriate.
- [ ] Keep developer access explicit, session-limited, and unavailable by default.

## Phase 5 — Reusable module integration

- [ ] Document integration contracts for Cowlsly Vault, Authenticator, CASMEA, and the website.
- [ ] Add stable deep links and ContentProvider/API contracts only where necessary.
- [ ] Avoid duplicating Android private settings storage.

## Source-of-truth documents

1. `PATH.of.TRUTH.md`
2. `README.md`
3. `ROADMAP.md`
4. `TODO.md`
5. `UI_ASSET_SOURCE.md`
6. `ui_asset_dependencies.json`
7. `dev/dat/doc/SIMPLE_SETTINGS_VISION.md`

Historical local asset catalogues remain useful migration records but do not override the canonical UI repository.