# Simple Settings Asset Cleanup Report

Date: 2026-07-11
Branch: `maintenance/simple-settings-asset-cleanup`
Visibility: Public
Status: Non-destructive audit, build, test, lint, and APK-size validation complete

## Confirmed findings

- The repository is a compact Android application with a small reusable asset collection.
- Reusable masters include settings icons, volume-step badges, an animated cogs background, and small Cowlsly logo exports.
- The automated audit scanned 106 files totalling 627,467 bytes.
- It confirmed two exact SHA-256 duplicate groups.
- `Cowlsly/.gitbook/assets/cowlsly_logo_small.png`, `assets/branding/cowlsly_logo_small.png`, and `app/src/main/res/drawable/cowlsly_logo_small.png` are byte-identical with SHA-256 `47ad737f851010f6e475cf3e517ab70af5fdb6ce0ef11ceec40d333851b73ae3`.
- `Cowlsly/README.md` and `Cowlsly/BRANDING.md` are also byte-identical.
- No APK, AAB, Gradle build directory, or other generated build output was committed in the audited tree.

## Public-repository security review

- No secret value is printed or copied by the audit or this report.
- The value-redacted scan found zero credential or privacy indicators in the audited current tree.
- This does not prove that Git history never contained sensitive data; a destructive history scan or rewrite was not performed.

## Validation results

- Public Asset and Privacy Audit: passed.
- Android build: passed on Java 21.
- Unit tests: passed.
- Android lint: passed.
- Debug APK: 18,632,680 bytes.
- Debug APK SHA-256: `1e8f5cc8b7bc42ef14adb9ea17127790a5ad4a02e21919b1dc808007fa52a3a1`.
- APK artifact digest: `sha256:bde955b692b124fb4c65c6f493244b4a879ef27ac47f017f35c91dacd985f56f`.
- Codespaces used: none.

The persistent audit summary is `docs/assets/simple_settings_public_audit_summary_2026_07_11.json`.

## Actions completed

- Created a maintenance branch and draft pull request.
- Added a consumer manifest, cleanup report, public audit summary, value-redacted scanner, and read-only audit workflow.
- Hardened Android CI with read-only permissions, Java 21, timeout, concurrency control, and a seven-day debug APK artifact.
- Preserved every runtime resource and reusable master.

## Pending

- Reference-map each of the three identical logo copies.
- Preserve the canonical logo and reusable icon/background masters in the canonical UI repository through a binary-capable transfer.
- Retain the Android runtime copy and only the documentation preview that remains useful.
- Compare APK and repository sizes after a later removal commit.
- Assess Git history separately if human approval is given.

## Rollback

Close draft PR #1 or delete `maintenance/simple-settings-asset-cleanup`. The public `main` branch remains unchanged.
