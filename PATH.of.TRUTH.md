# PATH.of.TRUTH.md — Cowlsly Simple Settings Repo

Repo: `Cowlsly/cowlsly_console_simple_settings_repo_03`
Default branch: `main`
Created: 2026-07-09
Purpose: per-repo asset and documentation checklist for Simple Settings.

## Product scope

Simple Settings is the shared master settings module for Cowlsly apps. It owns the closest controls first: volume, mute, panel tint, hearing warning, personal/CASMEA entry, regular Android settings shortcuts, gated developer options, and future suite sync.

Do not store ALI-Key/API secrets in this repo. That belongs to the Vault/Marla Keyring repo.

## Required files to read before work

- `README.md`
- `ROADMAP.md`
- `assets/README.md`
- `assets/ASSET_MANIFEST.md`
- `dev/dat/doc/SIMPLE_SETTINGS_VISION.md`
- `dev/dat/doc/ROADMAP.ORIGINAL.md`
- `Cowlsly/BRANDING.md`

## Agent instruction block

When prompted to work in this repo:

1. Read this file.
2. Read `assets/ASSET_MANIFEST.md`.
3. Search this repo for the next unchecked or missing Simple Settings asset.
4. Compare against the website repo master list in `Cowlsly/cowlsly-console-web-repo-01/FULL.PATH.of.TRUTH.md` if available.
5. If the chosen asset is web-facing, place/copy the final web version into the website repo under the matching `assets/` path.
6. If the chosen asset is native-app-only, keep it in this repo and log it here.
7. Update this work log and any asset manifest touched.
8. Report exact changed paths and factual security notes only.

## Existing DONE assets from manifest

### Icons in `assets/images/icons/`

- `simple_settings_app_icon_transparent.svg` — DONE
- `simple_settings_volume_steps_icon_transparent.svg` — DONE
- `simple_settings_volume_mute_icon_transparent.svg` — DONE
- `simple_settings_hearing_warning_icon_transparent.svg` — DONE
- `simple_settings_casmea_info_entry_icon_transparent.svg` — DONE
- `simple_settings_developer_shortcut_icon_transparent.svg` — DONE
- `simple_settings_security_privacy_icon_transparent.svg` — DONE
- `simple_settings_device_settings_icon_transparent.svg` — DONE

### UI badges in `assets/images/ui/volume_steps/`

- `simple_settings_volume_step_0_percent_transparent.svg` — DONE
- `simple_settings_volume_step_25_percent_transparent.svg` — DONE
- `simple_settings_volume_step_50_percent_transparent.svg` — DONE
- `simple_settings_volume_step_75_percent_transparent.svg` — DONE
- `simple_settings_volume_step_90_percent_transparent.svg` — DONE

### Shared branding in `assets/branding/`

- `cowlsly_logo_small.png` — DONE
- `cowlsly_logo_small_transparent.svg` — DONE
- `cowlsly_cogs_background_animated.svg` — DONE

## Suggested next asset/documentation queue

1. Confirm any missing settings-zone button state sets for website integration.
2. Create web-facing Simple Settings button states only if absent from website master list:
   - `assets/images/buttons/cowlsly_button_simple_settings_base_transparent.png`
   - `assets/images/buttons/cowlsly_button_simple_settings_pressed_transparent.png`
3. Create panel tint preview assets only if needed by `ROADMAP.md` or website master list.
4. Create accessibility companion icons only if not already covered by website `L001-L007`.
5. Keep Simple Settings native icons readable, simple, and transparent.

## Palette

Use suite palette:

- Midnight machine base: `#020610`, `#071321`, `#17304d`
- Gold accent: `#fff2a8`, `#d7a93d`, `#815b18`
- Cyan accent: `#20f0ff`
- Warning: `#ff5c78` with gold/cream stroke

## Rules

- Use lower_snake_case filenames.
- Transparent UI pieces should be SVG or true-alpha PNG.
- No checkerboard backgrounds.
- Do not duplicate DONE assets.
- Settings must remain user-consent-led and cannot quietly enable hidden developer/admin access.

## Required work log format

```text
YYYY-MM-DD | agent/tool | action
- searched: files/folders searched
- selected asset: id + filename, or SKIPPED with reason
- generated/copied/edited/deleted: exact paths
- placed final file: exact path
- quality checks: transparency/build/docs checks completed
- ledger updates: files updated
- security/evidence notes: factual observations only; no accusations, no secrets, no private keys
```

## Work log

2026-07-09 | Marla / ChatGPT connector | created repo-level checklist
- searched: repo metadata, `ROADMAP.md`, `assets/ASSET_MANIFEST.md`, website master asset ledger references
- selected asset: none; documentation control file only
- generated/copied/edited/deleted: created `PATH.of.TRUTH.md`
- placed final file: `PATH.of.TRUTH.md`
- quality checks: no binary assets created; no DONE asset status changed
- ledger updates: none
- security/evidence notes: confirmed ALI-Key/API secret storage remains out of scope for this repo

END
