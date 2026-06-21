# AGENTS.md

This repository contains a reusable Skill for AI coding/design agents.

## What This Project Is

`cinematic-layout` helps agents generate websites with:

- stronger high-end visual direction
- better control of pacing, space, light, and composition
- less template drift across repeated demos
- a director + film based research-and-translation workflow instead of generic luxury UI prompting

## Primary Goal

The main pain point this project solves is:

> AI often produces websites that are technically clean but visually average, weak in rhythm, weak in spatial control, and too dependent on generic hero/feature/CTA patterns.

This skill pushes agents to solve those problems through a computer-operable workflow:

0. complete the start questionnaire for this invocation
1. research a director + film with external sources when available
2. extract cinematic grammar from that research
3. define page scenes
4. lock signature compositions
5. derive shared system last
6. implement and verify

Important boundary:

> The film is not the computer workflow. The film is the research substrate. The computer-operable workflow starts when the agent translates those observations into decisions, storyboard, spec, and implementation.

## Read Order

When working on this repo or using this skill, read in this order:

1. [README.md](./README.md)
2. [SKILL.md](./SKILL.md)
3. [references/autonomous-direction.md](./references/autonomous-direction.md)
4. [references/output-templates.md](./references/output-templates.md)
5. [references/premium-calibration.md](./references/premium-calibration.md)
6. [references/anti-garbage.md](./references/anti-garbage.md)

## Rules For Agents

- Do not turn this into a generic premium-brand website skill.
- Universal and brand-agnostic: never assume or default to a specific brand's identity. Honor the user's own brand if given; otherwise generate fresh. No skill-core file names a specific brand.
- Make every invocation produce a visibly different style: drive director+film selection from the project seed across the full library, and rotate the palette lead — see `references/anti-convergence.md` (Cross-Invocation Variation).
- Keep the director + film mechanism as the emotional source.
- Operate autonomously: infer, propose, choose, and justify rather than asking for every detail. `Surprise me` is the default start option; proceed on justified assumptions when input is thin. See `references/autonomous-direction.md`.
- Work in the saturated, primary-leaning color space but rotate the lead per project (red-led, green-led, cobalt-led, or a tension pair) — never a fixed blue+red+green trio, and never default to brown/sepia/amber unless the chosen film demands it. Bias on defaults, not an override.
- Land one controlled, tasteful surprise per project; self-critique and refine in grouped passes before presenting.
- Every invocation must complete the start questionnaire before Phase 1.
- Research the chosen director and film before locking the phase when web access is available.
- Preserve the `decisions -> storyboard -> compiled-spec -> build` workflow.
- Maintain the `Demo Uniqueness Protocol`.
- If you change workflow rules, also check:
  - `references/autonomous-direction.md`
  - `references/output-templates.md`
  - `references/premium-calibration.md`
  - `references/anti-garbage.md`
- Prefer progressive disclosure:
  - keep `SKILL.md` lean
  - move details into `references/`

## Cross-Agent Compatibility

This repo is intentionally structured so multiple agent tools can use the same project context:

- `AGENTS.md` — cross-tool / agent-standard workflows (this file)
- `CLAUDE.md` — Claude Code (primary platform)
- `CODEX.md` — OpenAI Codex / ChatGPT
- `GEMINI.md` — Gemini / Antigravity-style workflows
- `.github/copilot-instructions.md` — GitHub Copilot repository instructions
- `.cursor/rules/cinematic-ui.mdc` — Cursor (auto-loaded on clone)
- `.windsurf/rules/cinematic-ui.md` — Windsurf (auto-loaded on clone)

These files should stay aligned in meaning, even if wording differs slightly by tool.
