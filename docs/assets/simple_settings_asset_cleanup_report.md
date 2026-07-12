# Simple Settings asset cleanup report

Date: 2026-07-11  
Integrated into `main`: 2026-07-12  
Status: non-destructive audit, build, tests, lint, and APK-size validation completed

## Confirmed findings

- The repository is a compact Android consumer application with a small reusable asset collection.
- The audit scanned 106 files totalling 627,467 bytes.
- Two exact SHA-256 duplicate groups were confirmed.
- `Cowlsly/.gitbook/assets/cowlsly_logo_small.png`, `assets/branding/cowlsly_logo_small.png`, and `app/src/main/res/drawable/cowlsly_logo_small.png` are byte-identical with SHA-256 `47ad737f851010f6e475cf3e517ab70af5fdb6ce0ef11ceec40d333851b73ae3`.
- `Cowlsly/README.md` and `Cowlsly/BRANDING.md` are byte-identical.
- No APK, AAB, Gradle build tree, or other generated build output was committed in the audited tree.

## Security review

- The value-redacted scan found zero credential or privacy indicators in the audited current tree.
- Findings record only path, category, and severity. Matching values are never written to reports.
- This does not prove that Git history never contained sensitive data. No history rewrite or destructive history scan was performed.

## Validation evidence

- Android build: passed on Java 21.
- Unit tests: passed.
- Android lint: passed.
- Debug APK: 18,632,680 bytes.
- Debug APK SHA-256: `1e8f5cc8b7bc42ef14adb9ea17127790a5ad4a02e21919b1dc808007fa52a3a1`.
- APK artifact digest: `sha256:bde955b692b124fb4c65c6f493244b4a879ef27ac47f017f35c91dacd985f56f`.
- Codespaces used: none.

## Actions now active on main

- Java 21 Android CI with read-only permissions, timeout, concurrency control, tests, lint, and short-lived debug APK artifact.
- Value-redacted public repository audit and read-only workflow.
- Canonical UI consumer policy and immutable dependency contract.
- All runtime and reusable assets preserved pending canonical binary transfer.

## Remaining migration gate

1. Preserve the canonical logo, icons, badges, and animated background in the canonical UI repository through a binary-capable transfer.
2. Record original SHA-256, provenance, licence, and consumer destinations.
3. Synchronise generated Android resources.
4. Rebuild and retest.
5. Retain the Android runtime copy and only useful documentation previews.
6. Remove exact duplicates only after reference and build checks pass.

The persistent measured summary is `simple_settings_public_audit_summary_2026_07_11.json`.
