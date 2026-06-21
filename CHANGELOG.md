# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

### Changed

- Repointed: GitHub repo and homepage are now `github.com/Pythoughts-labs/cinematic-ui`; npm package is `@pythoughts/cinematic-ui`.
- Author and maintainer is Mohamed Elkholy.
- Added `package.json` for npm publishing (scoped `@pythoughts/cinematic-ui`, MIT, `files` whitelist, no runtime deps).
- Added `LICENSE` (MIT) — was previously referenced but missing.
- Added primary English `README.md`; removed Chinese READMEs.
- Removed empty `docs/` folder and broken banner reference.
- `SECURITY.md` reporting channel switched to GitHub private security advisories.

## [1.0.0] - 2026-04-02

### Added

- **4-phase workflow**: decisions → storyboard → compiled-spec → build & verify
- **SKILL.md**: lean main entry with progressive loading from `references/`
- **Director + film research**: web search integration for cinematography analysis before locking Phase 1
- **Start questionnaire gate**: every invocation must complete the opening questionnaire first
- **Demo Uniqueness Protocol**: history audit, shell-ban list, primary composition family enforcement
- **Premium Calibration** (`references/premium-calibration.md`): post-brief quality self-check
- **Anti-Garbage rules** (`references/anti-garbage.md`): common AI design degradation patterns
- **Anti-Convergence system** (`references/anti-convergence.md`): hash-based selection to prevent repeated shells
- **Implementation Guardrails** (`references/implementation-guardrails.md`): JS effect list, entrance map rules, Phase 3 checklist, Punch Up / Pull Back protocol
- **Reference Protocol** (`references/reference-protocol.md`): decompose references without copying
- **Output Templates** (`references/output-templates.md`): standard artifact formats for all phases
- **Library Index** (`references/library-index.md`): per-phase file loading guide
- **18 design data libraries** in `references/data/` (~600KB total):
  - 200+ directors, 30 hero archetypes, 25 narrative beats, 18 director arc templates
  - 91+ section archetypes, 50 section functions, 80 compositions
  - 55 camera shots, 55+ interaction effects, 40 visual elements
  - 50+ background techniques, 40+ typography treatments, 40+ color grades
  - 30+ font pairings, 30+ textures, 1,486-site Design DNA index
- **Cross-agent compatibility**:
  - `AGENTS.md` — cross-tool agent instructions
  - `CLAUDE.md` — Claude Code project memory
  - `GEMINI.md` — Gemini / Antigravity workflows
  - `.github/copilot-instructions.md` — GitHub Copilot repository instructions
  - `agents/openai.yaml` — OpenAI-style skill metadata
- **English README**: `README.md` is the primary readme
- **GitHub infrastructure**: issue templates, PR template, CONTRIBUTING.md, SECURITY.md, CODE_OF_CONDUCT.md, LICENSE (MIT)
