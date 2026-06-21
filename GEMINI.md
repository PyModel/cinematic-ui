# GEMINI.md

Shared project instructions for Gemini-compatible agent tools and Antigravity-style workflows.

## Project Summary

This repository contains `cinematic-layout`, a reusable skill/workflow for generating cinematic websites.

The project is designed to help agents create results that feel:

- more premium
- more directed
- less template-like
- more aware of pacing, space, light, and composition
- more grounded in real director/film research when web access is available

## Core Workflow

Always preserve this order:

1. start questionnaire
2. research director + film
3. decisions
4. storyboard
5. compiled-spec
6. build and verify

Inside storyboard/spec work, preserve:

1. site cinematic grammar first
2. per-page scene thesis
3. signature composition per page
4. shared system last

## Primary Platform Note

This skill is primarily designed for **Claude Code**. The Claude Code-specific configuration lives in [`CLAUDE.md`](./CLAUDE.md). Codex-specific context lives in [`CODEX.md`](./CODEX.md).

## Repo Guidance

- Read [README.md](./README.md) first (English default).
- Use [AGENTS.md](./AGENTS.md) as the cross-tool reference.
- Use [SKILL.md](./SKILL.md) as the source of truth for the skill workflow.
- Keep `Demo Uniqueness Protocol` intact.
- Avoid turning this into a generic luxury landing page generator.
- Operate autonomously: infer, choose, and justify rather than asking for every detail. `Surprise me` is the default start option; proceed on justified assumptions when input is thin. See [references/autonomous-direction.md](./references/autonomous-direction.md).
- Universal and brand-agnostic: never assume or default to a specific brand. Honor the user's own brand if given; otherwise generate fresh. No skill-core file names a specific brand.
- Make every invocation a visibly different style: seed director+film selection from the project across the full library and rotate the palette lead — see [references/anti-convergence.md](./references/anti-convergence.md) (Cross-Invocation Variation).
- Work in the saturated, primary-leaning color space but rotate the lead per project (red-led / green-led / cobalt-led / tension pair) — never a fixed blue+red+green trio, and never default to brown/sepia/amber unless the film demands it. Land one tasteful surprise per project and self-critique before presenting.
- Every invocation must finish the start questionnaire before entering Phase 1.
- Treat the film as research input, not as a spec artifact. The formal workflow starts when film observations are translated into web artifacts.

## If You Modify This Repo

- keep `SKILL.md` lean
- update `references/` when workflow rules change
- keep `README.md` aligned with `SKILL.md` and `references/`
- keep agent instruction files (CLAUDE.md, CODEX.md, AGENTS.md) aligned in intent
