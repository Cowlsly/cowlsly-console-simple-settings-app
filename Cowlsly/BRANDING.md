# Cowlsly suite branding standard

Every Cowlsly Console repo must include the shared branding kit and follow these rules when mentioning Cowlsly logos, cyberpunk imagery, or background motion.

## Required in every repo

| Asset | Path | Use |
|-------|------|-----|
| Small logo (PNG) | `assets/branding/cowlsly_logo_small.png` | README headers, docs, PR descriptions |
| Small logo (SVG) | `assets/branding/cowlsly_logo_small_transparent.svg` | Web/docs where SVG is preferred |
| Forever-turning cogs | `assets/branding/cowlsly_cogs_background_animated.svg` | Doc backgrounds, UI previews, cyberpunk backplates |
| Branding readme | `assets/branding/README.md` | Local usage notes |
| This standard | `Cowlsly/BRANDING.md` | Suite-wide rules (this file) |

## When to show the small logo

Embed the small Cowlsly logo at the top of every repo `README.md` and in any doc that references:

- Cowlsly logos or production marks
- Cyberpunk UI panels, neon glass, chrome trim, or gold circuit frames
- The Cowlsly Console suite or Cowlsly.com

Markdown pattern:

```markdown
<p align="center">
  <img src="assets/branding/cowlsly_logo_small.png" alt="Cowlsly Production" width="220"/>
</p>
```

## Forever-turning machine (background)

The signature Cowlsly background is the **forever-turning cog machine** — interlocking gears that rotate continuously behind cyberpunk UI panels.

- **Docs / README previews:** `assets/branding/cowlsly_cogs_background_animated.svg`
- **Android app runtime:** `cogs_background.mp4` looped via `CogVideoBackground` (see Vault repo)

Never ship a Cowlsly screen or doc hero without either the animated SVG or the looping cogs video behind the content. Apply a dark scrim (40–60% opacity) so foreground text stays readable.

## Cyberpunk design language

Shared palette (from Vault `assets/ui/cowlsly_vault_palette`):

- Neon cyan accent: `#20f0ff`
- Gold gradient: `#fff2a8` → `#d7a93d` → `#815b18`
- Deep background: `#17304d` → `#071321` → `#020610`
- Warning/hot: `#ff5c78`

Visual rules: dark carbon backplates, chrome trim, shiny gold buttons, diamond-bright highlights, glass panel overlays.

## Full logo pack (canonical source)

The complete layered Cowlsly Production logo with CP-SIG v1 fingerprint lives in:

`cowlsly-the-keys-to-marlas-heart-me-repo/assets/res/cowlsly_productions_logo/`

Other repos carry the **small embed kit** only. Copy from the Vault repo when the full layered sigil is needed.

## Repo checklist

- [ ] `assets/branding/` contains all three branding files + README
- [ ] `README.md` shows the small logo at the top
- [ ] Docs mentioning Cowlsly cyberpunk imagery reference the cogs background
- [ ] `Cowlsly/BRANDING.md` present (this file)