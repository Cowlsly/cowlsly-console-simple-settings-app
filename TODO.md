# TODO — Cowlsly Simple Settings

## Canonical asset migration

- [ ] Import shared branding, module icons, volume-step controls, animated background, and UI audio into the canonical UI repository.
- [ ] Pin the final canonical commit and paths in `ui_asset_dependencies.json`.
- [ ] Synchronise valid Android resources directly into `res/drawable-nodpi`, `res/mipmap-*`, and `res/raw`.
- [ ] Repair Compose/XML references and remove verified obsolete local masters only after a Java 21 build passes.

## Application validation

- [ ] Run `./gradlew assembleDebug` with Java 21.
- [ ] Run unit and instrumentation tests where available.
- [ ] Verify system-intent handling, unavailable-setting fallbacks, search, usage ranking, and access tiers.
- [ ] Verify accessibility, reduced motion, hearing warnings, and safe volume behavior.
- [ ] Confirm no API keys or private medical data are exported through UI asset or suite-sync files.

## Product work

- [ ] Review every system setting shortcut against current Android behavior and permissions.
- [ ] Complete the security/privacy hub without duplicating Android private settings storage.
- [ ] Keep developer options explicitly gated and session-limited.
- [ ] Version the suite settings contract and add migration tests.

## Repository administration

- [x] Convert README and asset docs to the canonical UI consumer model.
- [x] Retire the every-repository-carries-branding policy.
- [x] Add dependency and source-policy files.
- [ ] Make `root` the default branch after GitHub administration is available.
- [ ] Remove obsolete `main` only after workflows, protections, and references are verified.
