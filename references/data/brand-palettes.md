# Brand Palette Integration (Bring Your Own Brand)

Use this **only when the user supplies their own brand** and wants the site to honor it. This is not a default look — the skill is brand-agnostic, and with no brand given you generate a fresh palette via the Color Direction and Cross-Invocation Variation rules instead.

How to use any brand here:

1. Take the user's brand colors (or extract them from their logo / existing site).
2. Map them onto the token roles below — background, surface, text, muted text, primary/secondary/tertiary accent, border.
3. Validate contrast (target WCAG AA: 4.5:1 for body text, 3:1 for large text and UI) and fill gaps with neutral steps.
4. Translate that palette *through the chosen film*, the same as any film-derived grade — do not let the brand flatten the cinematic direction.

The values below are a **neutral, illustrative example** showing the shape of a dark + light token system. They are placeholders — swap in the user's actual brand colors and re-validate contrast. Do not ship these example values as a default.

## Token Roles

| Role | Token | Used for |
|---|---|---|
| Background | `--brand-bg` | page background |
| Surface | `--brand-surface` | cards, frames, elevated panels |
| Surface (nested) | `--brand-surface-2` | nested surfaces, frame faces |
| Primary text | `--brand-text` | headings and body |
| Muted text | `--brand-text-muted` | secondary text |
| Dim text | `--brand-text-dim` | captions, metadata |
| Primary accent | `--brand-accent` | primary CTA, brand mark |
| Secondary accent | `--brand-accent-2` | highlight, secondary CTA (optional) |
| Tertiary accent | `--brand-accent-3` | link, info, calm emphasis (optional) |
| Rule | `--brand-rule` | hairlines, dividers |

## Example — Dark Theme (illustrative)

| Token | Hex | Used for |
|---|---|---|
| `--brand-bg` | `#0B0E12` | page background |
| `--brand-surface` | `#161B22` | cards, frames, elevated panels |
| `--brand-surface-2` | `#1F2630` | nested surfaces, frame faces |
| `--brand-text` | `#F2F5F8` | primary text |
| `--brand-text-muted` | `#C2C9D2` | secondary text |
| `--brand-text-dim` | `#8B97A6` | captions, metadata |
| `--brand-accent` | `#3B82F6` | primary CTA, brand mark |
| `--brand-accent-2` | `#22C55E` | highlight (only if a tension pair is wanted) |
| `--brand-accent-3` | `#8B97A6` | link, calm emphasis |
| `--brand-rule` | `#2A313B` | hairlines, dividers |

## Example — Light Theme (illustrative)

| Token | Hex | Used for |
|---|---|---|
| `--brand-bg` | `#FAFBFC` | page background |
| `--brand-surface` | `#FFFFFF` | cards, frames |
| `--brand-text` | `#0B0E12` | primary text |
| `--brand-text-muted` | `#3A424D` | secondary text |
| `--brand-text-dim` | `#5B6573` | captions, metadata |
| `--brand-accent` | `#2563EB` | primary CTA, brand mark |
| `--brand-accent-2` | `#16A34A` | highlight (optional) |
| `--brand-accent-3` | `#2563EB` | link, info |
| `--brand-rule` | `#E3E7EC` | hairlines, dividers |

> Near-white text on the near-black background reads AAA. Every **accent** above is illustrative — when you swap in the user's brand, verify each accent against its background reaches AA before shipping, and darken or lighten it if it falls short.

## Accent Discipline

- One main accent is usually enough. Add a secondary accent only when it creates meaningful tension.
- One accent per region (header, section, footer); reserve the primary accent for the main CTA and brand mark.
- Use a loud secondary accent at most once per screen.

**Avoid:**
- Stacking all accents in a single small component (visual noise).
- Using a low-contrast accent for body text — verify AA at body size first.
- Tinting the pure background or text tokens — use the next neutral step instead.

## CSS Variables (drop-in, replace with the user's brand)

```css
:root[data-theme="dark"] {
  --brand-bg: #0B0E12;
  --brand-surface: #161B22;
  --brand-surface-2: #1F2630;
  --brand-text: #F2F5F8;
  --brand-text-muted: #C2C9D2;
  --brand-text-dim: #8B97A6;
  --brand-accent: #3B82F6;
  --brand-accent-2: #22C55E;
  --brand-accent-3: #8B97A6;
  --brand-rule: #2A313B;
}

:root[data-theme="light"] {
  --brand-bg: #FAFBFC;
  --brand-surface: #FFFFFF;
  --brand-text: #0B0E12;
  --brand-text-muted: #3A424D;
  --brand-text-dim: #5B6573;
  --brand-accent: #2563EB;
  --brand-accent-2: #16A34A;
  --brand-accent-3: #2563EB;
  --brand-rule: #E3E7EC;
}
```

## When to use

Use this integration path when:
- The user brings their own brand and asks the site to honor "our colors" / "the brand palette" — map their tokens onto the roles above.
- The site needs to feel confident and on-brand rather than purely film-graded.

Use `color-grades.md` instead when there is no brand to honor and you want a film-derived cinematic grade. Don't mix — pick one source of truth. With no brand and no specific grade chosen, generate a fresh palette per the Color Direction and Cross-Invocation Variation rules; never fall back to this example as a default.
