# TODO — Cowlsly Simple Settings

## Authority rule for every agent and contributor

The Guardian reviews proposals and gives recommendations. Only the authenticated human Anchor may verify **YES** or **NO**. A Guardian recommendation, AI response, silence, inferred intent, timeout, or failed verification is never approval.

## P0 — Anchor Verification System foundation

- [ ] Define the immutable versioned proposal schema: ID, version, action, target, reason, permissions, data touched, risk, reversibility, expiry, and payload digest.
- [ ] Define Guardian review output as `RECOMMEND_APPROVE`, `RECOMMEND_DENY`, or `REQUEST_REVISION`, with evidence, warnings, missing information, confidence, effects, and safer alternatives.
- [ ] Ensure Guardian code cannot set approval state or call privileged execution.
- [ ] Build the Anchor review screen showing the complete proposal and Guardian recommendation as separate information.
- [ ] Add large explicit YES and NO controls with clear consequences.
- [ ] Require an authenticated Anchor session before accepting the decision.
- [ ] Bind approval to the proposal ID, version, digest, scope, and expiry.
- [ ] Treat NO, cancel, timeout, app closure, failed verification, ambiguity, and missing data as denial without side effects.
- [ ] Require a new review and new Anchor decision after any material proposal change.
- [ ] Add a controlled executor that accepts only a valid, unused Anchor approval token for the same proposal digest.
- [ ] Reject expired, replayed, duplicate, malformed, or previously consumed approvals.
- [ ] Record proposal digest, Guardian recommendation, Anchor decision, verification method, timestamp, execution result, and failure state in a local audit trail.
- [ ] Exclude secrets, credentials, tokens, medical contents, and unnecessary personal data from audit entries.
- [ ] Add cancel-before-execution, permission revocation, emergency lockout, and kill-switch behavior.

## P0 — Acceptance tests for basic use

- [ ] Guardian recommendation is visibly labelled as advice, never approval.
- [ ] YES executes only the exact approved proposal.
- [ ] NO prevents execution and leaves no partial side effects.
- [ ] Timeout, app closure, biometric/PIN failure, or unavailable verification prevents execution.
- [ ] Changing action, target, permissions, payload, or risk invalidates earlier approval.
- [ ] Replaying an approval or proposal is rejected.
- [ ] Direct executor calls without valid Anchor approval are rejected.
- [ ] Audit entries accurately record proposal, recommendation, decision, and result.
- [ ] Accessibility tests confirm the proposal and YES/NO controls are understandable with screen readers, keyboard navigation, large text, and reduced motion.

## Completed canonical asset work

- [x] Import the complete reusable Simple Settings asset set into the canonical UI repository.
- [x] Verify byte identity and SHA-256 for the PNG logo, SVG logo/background, eight icons, and five volume-step controls.
- [x] Pin verified immutable release `acf7ffaab736283daccd286d01abf60a8f2a80a2` and final canonical paths in `ui_asset_dependencies.json`.
- [x] Retarget the canonical dependency branch to `root`.
- [x] Convert local asset paths to declared generated consumer copies.
- [x] Add root-only Java 21 build, tests, lint, and APK artifact CI.
- [x] Merge all reviewed branch histories into `root`.
- [x] Delete all non-root branches after ancestry verification.

## Remaining asset validation

- [ ] Run deterministic canonical sync and write `.cowlsly_ui_generated.json`.
- [ ] Synchronise vault-transition resources into valid `res/drawable-nodpi` and `res/raw` paths when the transition is enabled in the app.
- [ ] Confirm the newest Java 21 CI run passes after final dependency and documentation updates.
- [ ] Repair Compose/XML references only where generated paths differ.
- [ ] Remove obsolete local masters only after sync receipt, reference checks, and Java 21 validation pass.

## Application validation

- [ ] Verify system-intent handling, unavailable-setting fallbacks, search, usage ranking, and access tiers on current Android.
- [ ] Add or run instrumentation tests where emulator/device behavior is required.
- [ ] Verify accessibility, reduced motion, hearing warnings, and safe volume behavior.
- [ ] Confirm no API keys or private medical data are exported through UI assets or suite-sync files.

## Product work

- [ ] Review every system-setting shortcut against current Android behavior and permissions.
- [ ] Complete the security/privacy hub without duplicating Android private-settings storage.
- [ ] Keep developer options explicitly gated and session-limited.
- [ ] Route privileged developer, security, privacy, account, export, and external-app actions through Anchor verification.
- [ ] Version the suite settings contract and add migration tests.

## Repository administration

- [x] Keep active development on `root`.
- [x] Convert README and asset docs to the canonical UI consumer model.
- [x] Retire the every-repository-carries-branding policy.
- [x] Close known PRs after integrating their work.
- [x] Confirm `root` as the default and only branch.

## Completion rules

- Do not mark an item complete without repository evidence and relevant tests.
- Any path that allows the Guardian, an AI, plugin, background service, or developer shortcut to bypass the Anchor is a critical security defect.
- Do not store approval secrets or sensitive proposal contents in logs.
