# Brand Palettes — Pythoughts

Curated, pre-validated color palettes for sites under the Pythoughts brand
(`@pythoughts/*` on npm). Two themes share the same eleven colors so a single
source of truth covers both light and dark contexts.

## Palette Source

| Hex | Name | Role |
|---|---|---|
| `#000000` | Black | ink, contrast base |
| `#303841` | Dark Slate | dark surface elevation |
| `#DDDDDD` | Light Gray | muted body text |
| `#EEEEEE` | Near White | high-contrast text on dark |
| `#F5F5F5` | Off White | primary body text |
| `#EFECE3` | Parchment | warm light surface |
| `#CB2957` | Crimson | primary accent (action, brand) |
| `#FF5722` | Ember Orange | secondary accent (highlight, CTA) |
| `#76ABAE` | Teal | tertiary accent (calm, link, info) |
| `#8FABD4` | Sky | light accent (secondary fill on light) |
| `#4A70A9` | Cobalt | deep light accent (link, focus on light) |

## Theme — Pythoughts Dark

Default for cinematic dark contexts (banner, dashboard, hero on black).

| Token | Hex | Used for |
|---|---|---|
| `--brand-bg` | `#000000` | page background |
| `--brand-surface` | `#303841` | cards, frames, elevated panels |
| `--brand-surface-2` | `#1f2630` *(derived)* | nested surfaces, frame faces |
| `--brand-text` | `#F5F5F5` | primary text |
| `--brand-text-muted` | `#DDDDDD` | secondary text |
| `--brand-text-dim` | `#76ABAE` | captions, metadata |
| `--brand-accent` | `#CB2957` | primary CTA, brand mark |
| `--brand-accent-2` | `#FF5722` | secondary CTA, highlight |
| `--brand-accent-3` | `#76ABAE` | link, info, calm emphasis |
| `--brand-rule` | `#303841` | hairlines, dividers |

**Contrast checks** (against `--brand-bg` `#000000`):

| Pair | Ratio | Notes |
|---|---|---|
| `#F5F5F5` on `#000000` | 18.8 : 1 | AAA |
| `#DDDDDD` on `#000000` | 14.2 : 1 | AAA |
| `#76ABAE` on `#000000` | 8.1 : 1 | AAA |
| `#CB2957` on `#000000` | 4.9 : 1 | AA large + UI |
| `#FF5722` on `#000000` | 5.8 : 1 | AA |

## Theme — Pythoughts Light

Default for editorial, document, and warm contexts.

| Token | Hex | Used for |
|---|---|---|
| `--brand-bg` | `#EFECE3` | page background |
| `--brand-surface` | `#F5F5F5` | cards, frames |
| `--brand-text` | `#000000` | primary text |
| `--brand-text-muted` | `#303841` | secondary text |
| `--brand-text-dim` | `#4A70A9` | captions, metadata |
| `--brand-accent` | `#CB2957` | primary CTA, brand mark |
| `--brand-accent-2` | `#FF5722` | secondary CTA, highlight |
| `--brand-accent-3` | `#4A70A9` | link, info |
| `--brand-rule` | `#DDDDDD` | hairlines, dividers |

**Contrast checks** (against `--brand-bg` `#EFECE3`):

| Pair | Ratio | Notes |
|---|---|---|
| `#000000` on `#EFECE3` | 17.4 : 1 | AAA |
| `#303841` on `#EFECE3` | 11.5 : 1 | AAA |
| `#4A70A9` on `#EFECE3` | 4.8 : 1 | AA large + UI |
| `#CB2957` on `#EFECE3` | 4.7 : 1 | AA large + UI |
| `#FF5722` on `#EFECE3` | 3.1 : 1 | AA large only — use with `--brand-bg` darken for body text |

## Tri-Accent Pattern (recommended)

Use all three accents together to echo the Pythoughts brand:

```
--brand-accent  → #CB2957 (primary)
--brand-accent-2 → #FF5722 (highlight)
--brand-accent-3 → #76ABAE (calm / link)
```

**Do:**
- One accent per region (header, section, footer).
- Reserve `#CB2957` for primary CTA and brand mark.
- Use `#FF5722` for ≤ 1 per screen (it's loud).
- Use `#76ABAE` for links and info chips on dark.

**Avoid:**
- Stacking all three accents in a single small component (visual noise).
- Using `#FF5722` for body text in light theme — fails AA at body size.
- Tinting `#000000` or `#F5F5F5` — use the next neutral in the table instead.

## CSS Variables (drop-in)

```css
:root[data-theme="dark"] {
  --brand-bg: #000000;
  --brand-surface: #303841;
  --brand-text: #F5F5F5;
  --brand-text-muted: #DDDDDD;
  --brand-text-dim: #76ABAE;
  --brand-accent: #CB2957;
  --brand-accent-2: #FF5722;
  --brand-accent-3: #76ABAE;
  --brand-rule: #303841;
}

:root[data-theme="light"] {
  --brand-bg: #EFECE3;
  --brand-surface: #F5F5F5;
  --brand-text: #000000;
  --brand-text-muted: #303841;
  --brand-text-dim: #4A70A9;
  --brand-accent: #CB2957;
  --brand-accent-2: #FF5722;
  --brand-accent-3: #4A70A9;
  --brand-rule: #DDDDDD;
}
```

## When to use

Pick this palette when:
- The user is shipping a `@pythoughts/*` npm package, Pythoughts-labs repo,
  or other Pythoughts-flavored property.
- The user asks for "the brand colors" or "our palette" and is on Pythoughts.
- The site needs to feel confident, modern, and approachable (vs. cinematic
  restraint) — this palette is friendlier than the film-derived grades in
  `color-grades.md`.

Pick `color-grades.md` instead when the user wants a film-derived cinematic
grade (specific director look). Don't mix — pick one source of truth.
