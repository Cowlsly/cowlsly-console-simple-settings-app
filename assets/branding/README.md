# Cowlsly shared branding kit

Small embeddable assets every Cowlsly Console repo carries. See `Cowlsly/BRANDING.md` for suite-wide rules.

## Files

| File | Labels | Purpose |
|------|--------|---------|
| `cowlsly_logo_small.png` | `branding`, `logo`, `cyberpunk` | Official 512px Cowlsly Production badge — use in README headers and docs |
| `cowlsly_logo_small_transparent.svg` | `branding`, `logo`, `cyberpunk`, `transparent` | Compact SVG badge for web and design tooling |
| `cowlsly_cogs_background_animated.svg` | `branding`, `background`, `cyberpunk`, `animated` | Forever-turning cog machine — suite signature background |

## README embed (copy-paste)

```markdown
<p align="center">
  <img src="assets/branding/cowlsly_logo_small.png" alt="Cowlsly Production" width="220"/>
</p>
```

## Background usage

Place `cowlsly_cogs_background_animated.svg` behind cyberpunk panels in docs, mockups, or UI previews. The gears rotate forever. Add a 40–60% dark scrim over the background so foreground content stays readable.

For Android runtime, use the looping `cogs_background.mp4` from the Vault repo via `CogVideoBackground`.