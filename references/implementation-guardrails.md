# Implementation Guardrails

Use this during Phase 3 and Phase 4.

This file restores the concrete anti-laziness rules that prevent the agent from collapsing back to generic web output while compiling and building.

## External Library Decision

Read the external-library section of `data/interaction-effects-50.md` before deciding whether to add outside dependencies.

Record this block in `compiled-spec.md` for every page or for the site-wide motion system:

```markdown
## External Library Decision

### Q1: What is the core motion experience of this page?
- [scroll narrative / shader surface / 3D depth / text performance / particles / page transition / other]

### Q2: Can the native library entries do it?
- [yes, no external library]
- or [no, specify which scene needs more and why native entries are insufficient]

### Q3: If an external library is used, why this one and how will it be re-directed through the chosen film language?
- [library choice, collision risk, how to avoid generic output]

### Decision
- External libraries: [name + CDN/import] (maximum 3)
- or: no external library, native effects only
```

## JS-Required Interaction Effects

These interaction entries require JavaScript and may not be downgraded to a generic CSS hover:

- `#1`
- `#2`
- `#8`
- `#15`
- `#23`
- `#26`
- `#35`
- `#36`
- `#37`
- `#38`
- `#39`
- `#46`
- `#48`
- `#50`
- `#54`

If one of these ids is selected in the storyboard or compiled spec:

- include the complete JS in `compiled-spec.md`
- include the final JS in the build output
- adapt timing, colors, and thresholds to the site's tokens

## Entrance Map

Before writing the page spec, create an entrance map for that page.

Example:

```markdown
## Entrance Map
- Scene 1: scale-in
- Scene 2: clip-wipe-right
- Scene 3: fade-from-black
- Scene 4: slide-left
- Scene 5: curtain-reveal
```

Rules:

- No two adjacent sections may use the same entrance type.
- `fadeUp` / `opacity + translateY` may appear at most 2 times per page.
- Each page must use at least 4 different entrance types when the page has enough sections to support that range.

## Phase 3 Quality Checklist

Do not treat Phase 3 as complete until all checks pass:

- Every section has complete layout CSS.
- Every section has complete entrance behavior.
- Every section has complete interaction behavior or an intentional `none`.
- If a JS-required effect is selected, the complete JS appears in `compiled-spec.md`.
- Global design tokens are used instead of stray hardcoded values.
- Entrance variety rules are satisfied.
- The compiled spec includes the `External Library Decision` block.
- Library source ids are present for major interactions, reveals, compositions, and atmosphere moves.
- Anti-garbage constraints still hold.

## Screening Room

After implementation, verify:

- layout matches the spec
- motion matches the spec
- interaction matches the spec
- reduced-motion support exists
- responsive behavior exists
- the page still feels like the chosen director in grayscale wireframe form

## Production Craft

The difference between "looks like a template" and "looks professionally art-directed" is craft the Phase 3 checklist does not catch. Before final QA, confirm each — these are additive to, not a repeat of, the checklist above:

- **Type craft:** a deliberate type scale (not browser defaults), tightened tracking on large display text, controlled line length (~60–75ch for body), no orphan/widow headlines, consistent vertical rhythm.
- **Spacing precision:** spacing comes from the scale, not stray pixel values; optical alignment where mathematical alignment looks off; consistent section padding logic across the page.
- **Interactive states are complete:** every interactive element has hover, focus-visible, active, and disabled states; forms have error and empty states; async surfaces have a loading state. No dead hovers.
- **Accessibility as craft:** visible keyboard focus, logical tab order, AA contrast on every text/UI pair, `prefers-reduced-motion` honored, real alt text, semantic landmarks.
- **Responsive integrity:** the composition is re-thought at small widths, not just reflowed; no horizontal scroll; tap targets ≥ 44px; the signature composition still reads on mobile.
- **Performance feel:** fonts use `font-display: swap`; the largest hero asset is sized and lazy-loaded where appropriate; motion stays on `transform`/`opacity`; no layout-shift jank on load.

If any item is weak, fix it before declaring the build done — a single broken focus state or default-looking type scale reads as amateur regardless of how strong the concept is.

## Post-Screening Adjustments

### Punch Up

Use when the user asks for:

- more dramatic
- bolder
- stronger
- more cinematic

Adjustment moves:

- increase scale contrast between key sections
- replace weak repeated entrances with more directed reveal types
- add one more film-appropriate visual element where a section feels too thin
- strengthen the director's signature device
- sharpen contrast or hierarchy without turning the page into an effect sampler

### Pull Back

Use when the user asks for:

- quieter
- cleaner
- too much
- too busy
- more restrained

Adjustment moves:

- remove one secondary visual layer from overloaded sections
- reduce glow, blur, or motion amplitude
- increase breathing room
- lower saturation toward the film's neutral zone
- keep the page thesis, but delete decorative support moves that do not strengthen it
