# CLAUDE.md

Project memory for Claude Code.

## Purpose

This repository ships a reusable Skill named `cinematic-layout`.

Its purpose is to help AI agents create websites with:

- stronger premium design direction
- better rhythm, spatial composition, and lighting logic
- less repetition across multiple demos
- a director + film based research-and-translation workflow rather than generic luxury prompting

## Read First

- [README.md](./README.md)
- [AGENTS.md](./AGENTS.md)
- [SKILL.md](./SKILL.md)

## Installation

**Windows:**
```powershell
git clone https://github.com/Pythoughts-labs/cinematic-ui "$env:USERPROFILE\.claude\skills\cinematic-ui"
```

**macOS / Linux:**
```bash
git clone https://github.com/Pythoughts-labs/cinematic-ui ~/.claude/skills/cinematic-ui
```

Or install as an npm package:

```bash
npm install -g @pythoughts/cinematic-ui
```

Then invoke with `/cinematic-ui` inside Claude Code.

## Cross-Agent Files

- [`CODEX.md`](./CODEX.md) — Codex / ChatGPT specific context
- [`GEMINI.md`](./GEMINI.md) — Gemini / Antigravity workflows
- [`AGENTS.md`](./AGENTS.md) — shared cross-tool reference

These files must stay aligned in intent with `CLAUDE.md` when workflow rules change.

## Claude-Specific Notes

- Treat this repo as a skill package, not as a normal app repo.
- If editing skill logic, keep `SKILL.md` concise and push details into `references/`.
- If changing workflow rules, sync the templates and guardrails in:
  - `references/autonomous-direction.md`
  - `references/output-templates.md`
  - `references/premium-calibration.md`
  - `references/anti-garbage.md`
- Preserve `Demo Uniqueness Protocol`.
- Run autonomously: infer, choose, and justify rather than asking for every detail. `Surprise me` is the default start option; proceed on justified assumptions when input is thin. Logic in `references/autonomous-direction.md`.
- Universal and brand-agnostic: never assume or default to a specific brand. Honor the user's own brand if given; otherwise generate fresh. Keep brand names out of the skill core (`SKILL.md`, `references/`).
- Make every invocation a visibly different style: seed director+film selection from the project across the full library and rotate the palette lead — see `references/anti-convergence.md` (Cross-Invocation Variation).
- Work in the saturated, primary-leaning color space but rotate the lead per project (red-led / green-led / cobalt-led / tension pair) — never a fixed blue+red+green trio, and never default to brown/sepia/amber unless the film demands it (a bias, not an override). Land one tasteful surprise per project and self-critique before presenting.
- Every invocation must complete the start questionnaire before Phase 1.
- When web access is available, research the chosen director and film before locking Phase 1.
- Treat the film as cinema research, not as a spec sheet. Formalize only the web translation artifacts.
- Do not collapse this project into a generic “high-end website prompt”.

## Design Intent

The core pain point this project addresses:

AI website outputs often fail at:

- pacing
- space
- light
- hierarchy
- premium restraint
- cross-demo uniqueness

This skill solves those through a structured, artifact-based workflow.

Important boundary:

The film is not the computer workflow. The film is the source material. The computer-operable workflow starts when the agent turns that research into `decisions.md`, `storyboard.md`, `compiled-spec.md`, and implementation.
