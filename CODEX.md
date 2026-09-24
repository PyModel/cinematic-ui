# CODEX.md

Project instructions for OpenAI Codex and ChatGPT agent workflows.

## Project Summary

This repository contains `cinematic-layout`, a reusable skill/workflow for generating cinematic websites.

The project helps agents produce websites that feel:

- more premium and directed
- less template-like
- stronger in pacing, space, light, and composition
- grounded in real director/film research when web access is available

## Primary Platform Note

This skill is primarily designed for **Claude Code**. The Claude Code-specific configuration lives in [`CLAUDE.md`](./CLAUDE.md).

For Codex and ChatGPT environments, use [`AGENTS.md`](./AGENTS.md) as the cross-tool workflow reference. This file adds Codex-specific context on top of that shared base.

## Installation for Codex

If your Codex environment supports a local skills or instructions folder, place the entire `cinematic-layout` directory there:

```
$CODEX_HOME/skills/cinematic-ui
```

Or clone directly from the repository:

```bash
git clone https://github.com/PyModel/cinematic-ui
```

Or install as an npm package:

```bash
npm install -g @pythoughts/cinematic-ui
```

Then point your Codex agent at the folder as a project context or instruction source.

## Core Workflow

Always preserve this order:

1. complete the start questionnaire
2. research director + film (use web access when available)
3. decisions → `decisions.md`
4. storyboard → `storyboard.md`
5. compiled-spec → `compiled-spec.md`
6. build and verify → HTML / CSS / JS

Inside storyboard and spec work, preserve this internal order:

1. site-wide cinematic grammar first
2. per-page scene thesis
3. signature composition per page
4. shared system last

## Repo Guidance

- Read [README.md](./README.md) for the full project overview.
- Use [AGENTS.md](./AGENTS.md) as the cross-tool workflow reference.
- Use [SKILL.md](./SKILL.md) as the source of truth for the skill logic.
- Keep the `Demo Uniqueness Protocol` intact across all invocations.
- Treat the film as research input, not as a spec sheet. The formal workflow starts when film observations are translated into web artifacts.
- Operate autonomously: infer, choose, and justify rather than asking for every detail. `Surprise me` is the default start option; proceed on justified assumptions when input is thin. See [references/autonomous-direction.md](./references/autonomous-direction.md).
- Universal and brand-agnostic: never assume or default to a specific brand. Honor the user's own brand if given; otherwise generate fresh. No skill-core file names a specific brand.
- Make every invocation a visibly different style: seed director+film selection from the project across the full library and rotate the palette lead — see [references/anti-convergence.md](./references/anti-convergence.md) (Cross-Invocation Variation).
- Work in the saturated, primary-leaning color space but rotate the lead per project (red-led / green-led / cobalt-led / tension pair) — never a fixed blue+red+green trio, and never default to brown/sepia/amber unless the film demands it. Land one tasteful surprise per project and self-critique before presenting.
- Every invocation must complete the start questionnaire before Phase 1.

## If You Modify This Repo

- Keep `SKILL.md` lean; push workflow details into `references/`.
- Update `references/` when workflow rules change.
- Keep agent instruction files aligned in intent with `CLAUDE.md` and `AGENTS.md`.
