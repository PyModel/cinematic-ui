# Repository Custom Instructions for GitHub Copilot

This repository contains a reusable AI skill named `cinematic-layout`.

## Project Goal

This skill helps AI agents generate websites with:

- stronger high-end design quality
- better pacing, spatial composition, and lighting logic
- less template repetition across multiple demos
- a director + film based workflow instead of generic luxury prompting

## Important Context

- This is not a generic web design prompt pack.
- The emotional source must remain `director + specific film`.
- When web access is available, research the chosen director and film before locking the first phase.
- Treat the film as cinema research, not as a spec sheet. Formalize only the web translation artifacts.
- The workflow must remain:
  - `decisions -> storyboard -> compiled-spec -> build`
- Shared systems must come after page-level compositions are defined.
- `Demo Uniqueness Protocol` is a core feature, not an optional extra.
- Operate autonomously: infer, choose, and justify rather than asking for every detail. `Surprise me` is the default start option; proceed on justified assumptions when input is thin (`references/autonomous-direction.md`).
- Universal and brand-agnostic: never assume or default to a specific brand. Honor the user's own brand if given; otherwise generate fresh. No skill-core file names a specific brand.
- Make every invocation a visibly different style: seed director+film selection from the project across the full library and rotate the palette lead (`references/anti-convergence.md`, Cross-Invocation Variation).
- Work in the saturated, primary-leaning color space but rotate the lead per project (red-led / green-led / cobalt-led / tension pair) — never a fixed blue+red+green trio, and never default to brown/sepia/amber unless the film demands it. Land one tasteful surprise and self-critique before presenting.

## If You Edit Workflow Rules

Also check and keep aligned:

- `SKILL.md`
- `references/autonomous-direction.md`
- `references/output-templates.md`
- `references/premium-calibration.md`
- `references/anti-garbage.md`

## Writing Style

- Prefer concise, precise language.
- Keep repo-facing docs friendly to humans.
- Keep skill-facing docs optimized for agents.
