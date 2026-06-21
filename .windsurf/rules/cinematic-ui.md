# Cinematic Layout — Windsurf Rule

Apply when the user asks for a cinematic website, film-style landing page, director-inspired UI, or any design framed around a movie aesthetic.

## Core Principle

This is not a style picker. Do not select a visual theme from a menu.
This is a reasoning workflow. Research a real director and a specific film, extract cinematic grammar, and translate it into page structure, composition, and motion.

The film is research input, not a spec sheet. The formal workflow begins when observations are turned into artifacts.

## Four-Phase Workflow

```
Phase 1: DECISIONS  → Start questionnaire → decisions.md
Phase 2: STORYBOARD → Grammar → scene per page → signature composition → storyboard.md
Phase 3: SPEC       → Extract CSS/JS from libraries → compiled-spec.md
Phase 4: BUILD      → Implement from spec → HTML / CSS / JS
```

Never jump from request to HTML without the artifacts.

## Phase 2 Internal Order

1. Site-wide cinematic grammar
2. Per-page scene thesis
3. Irreplaceable signature composition per page
4. Shared system last

## Start Questionnaire

Ask at every invocation (present all at once with defaults; proceed autonomously when input is thin):
1. How to start: **Surprise me (default)** / Step-by-step / Screenshot
2. Image placeholders: Yes (default) / No
3. Site niche and page list (default: infer, then confirm)

## Key Rules

- Director + film drives color, type, spacing, composition, motion
- Operate autonomously — infer, choose, justify; `Surprise me` is the default. See `references/autonomous-direction.md`
- Universal and brand-agnostic — never assume or default to a specific brand; honor the user's own brand if given, else generate fresh
- Make every invocation a visibly different style — seed director+film from the project across the full library, rotate the palette lead (`references/anti-convergence.md`, Cross-Invocation Variation)
- Work in the saturated, primary-leaning color space but rotate the lead per project (red / green / cobalt / tension pair) — never a fixed blue+red+green trio, never brown/sepia/amber unless the film demands it. One tasteful surprise; self-critique and refine before presenting
- Every page needs one signature composition — no collapse to default grid
- `fadeUp` max 2× per page; at least 4 distinct entrance types per page
- Max 1 heavy interaction per page
- Grid is invisible infrastructure — never the visible composition
- Do not expose director names or workflow labels in the final UI

## Demo Uniqueness Protocol

When the user has prior outputs: run a uniqueness audit, write a shell-ban list, pick a different primary composition family.

## Reference Files

Read `references/library-index.md` first. Load only what the current phase needs.

Full skill logic: `SKILL.md`
