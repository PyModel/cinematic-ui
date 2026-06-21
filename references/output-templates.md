# Output Templates

Use these files as working artifacts inside the target project directory.

## decisions.md

```markdown
# Design Decisions

- Entry mode:
- Genre:
- Director:
- Film:
- Niche:
- Pages:
- Major page roles:
- Image placeholders:
- Sub-agent delegation plan (optional):
- Autonomous assumptions made (items inferred rather than asked):

## Creative Directions

- Direction A (name / concept / why non-generic / risk):
- Direction B (name / concept / why non-generic / risk):
- Direction C (name / concept / why non-generic / risk):
- Chosen direction:
- Why it has the strongest identity-to-usability ratio:

## Demo Uniqueness Audit

- Previous-work audit:
- Recurring traits to avoid:
- Shell-ban list:
- Primary composition family:
- Why this family differs from the most recent output:
- Wireframe-level uniqueness test:

## Research Notes

### Research Boundary
- Film research is observational input, not a spec:
- What is being translated into web language:
- What must not be flattened into product-template logic:

### Research Sources
- Director source:
- Film source:
- Secondary analysis:
- Niche source 1:
- Niche source 2:

### Film Palette
- Primary:
- Secondary:
- Accent:
- Shadow:
- Text:

### Color Direction
- Palette family + lead (one primary-leaning direction — red-led / green-led / cobalt-led / tension pair, rotated from the project seed; avoid brown/sepia/amber and avoid a fixed blue+red+green trio):
- How this family and lead differ from the user's most recent demo:
- If a warm/earthy palette was chosen anyway, the film reason:
- Contrast check (AA for text and UI):

### Director Signatures
1.
2.
3.

### Film Translation Notes
- Framing:
- Rhythm:
- Lighting:
- Space:
- Materiality:
- What should stay ambiguous or restrained:

### Niche References
- URL:
- URL:

### Reference Decomposition
- Reference A contributes:
- Reference B contributes:
- Reference C contributes:
- What will not be copied:

### Optional Reference Site Analysis
- Section map:
- Interaction inventory:
- Background techniques:
- Color and type cues:
```

## storyboard.md

```markdown
# Director's Treatment

## Director Brief
- Visual thesis:
- Signature technique 1:
- Signature technique 2:
- Signature technique 3:
- Motion rules:
- Typography rules:
- Color direction (primary-anchored palette family; warm only if the film demands it):
- Surprise signal (the one tasteful move the user would not have asked for):

## Site Cinematic Grammar
- Page-shell logic:
- Navigation posture:
- Framing discipline:
- Density cadence:
- Recurring material layers:
- Allowed composition families:
- What may repeat:
- What must vary page to page:
- Demo uniqueness guardrail:

## Page Arc

### Page: Home
- Page-role scene:
- Page scene thesis:
- One big idea:
- Hero dominance statement:
- Restraint statement:
- Material thesis:
- Typography thesis:
- Narrative arc:
- Hero archetype:
- Signature composition:
- Grid fallback test:
- Shared system holdback:
- UI exposure guardrail:
- What this page must not inherit from previous demos:
- Section sequence:

### Scene 1
- Beat:
- Function:
- Archetype:
- Composition ref:
- Camera ref:
- Interaction ref:
- Visual elements:
- Why this exists:
```

## compiled-spec.md

```markdown
# Compiled Spec

## Page: Home
- Page scene thesis:
- Signature composition:
- Signature composition source id:
- Why this cannot collapse into a default grid:
- One big idea:
- Heavy interaction:
- Heavy interaction source id:
- Showy reveals:
- Showy reveal source id(s):
- Restraint notes:
- Typography source id(s):
- Atmosphere/background source id(s):

## Entrance Map
- Scene 1:
- Scene 2:
- Scene 3:
- Scene 4:

### Scene 1
- Beat:
- Function:
- Archetype:
- Entrance:
- Camera source id:
- Interaction:
- Interaction source id:
- Composition source id:
- Visual element source id(s):
- Typography source id(s):
- Background/texture source id(s):

```css
/* layout */
/* entrance */
/* interaction */
```

```html
<!-- structure hint -->
```

```js
// include only if the chosen interaction requires JS
```

## External Library Decision

### Q1: What is the core motion experience of this page?
- 

### Q2: Can the native library entries do it?
- 

### Q3: If an external library is used, why this one and how will it be redirected through the chosen film language?
- 

### Decision
- 

## Palette Candidates
- Restrained candidate (bg / surface / text / muted / accent / accent-hover / border / optional secondary):
- Unusual candidate:
- Tension-based candidate:
- Selected palette and why (rarity, readability, primary anchor, holds across the page):

## Shared System
- Navigation:
- Footer:
- Spacing rhythm:
- Typography system:
- Utility primitives:
- Repeated motifs allowed only after page compositions are locked:
- Uniqueness check against previous demos:

## Self-Critique (Phase 4)

Score each strong / mixed / weak, then list the 5 highest-impact upgrades and the grouped passes applied.

- Originality and point of view:
- Typography and palette quality:
- Hierarchy and section rhythm:
- Motion restraint:
- Mobile intention:
- Accessibility and contrast:
- Non-generic identity (does it look AI-generated?):
- Top 5 upgrades:
- Refinement passes applied:

## Phase 3 Quality Check
- [ ] Every section has complete layout CSS
- [ ] Every section has complete entrance behavior
- [ ] Every section has complete interaction behavior or intentional `none`
- [ ] JS-required effects include complete JS
- [ ] Entrance variety rules pass
- [ ] `fadeUp` appears at most 2 times on the page
- [ ] External Library Decision block is complete
- [ ] Library source ids are present for all major visual moves

## Derived Global Tokens
```css
/* Replace --accent with the selected palette's accent. Default anchors on a
   saturated primary (blue/red/green), not a warm tan — see Color Direction. */
:root {
  --bg: #000000;
  --text: #f3f3f3;
  --accent: #2f6df6; /* primary-anchored placeholder (cobalt); set per chosen palette */
  --radius-card: 8px;
  --transition-fast: 0.35s;
  --transition-slow: 1s;
  --ease: cubic-bezier(0.22, 1, 0.36, 1);
}
```
```
