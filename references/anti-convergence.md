# Anti-Convergence System

## Film Selection — Reasoning Requirement

The failure mode is not picking the wrong film. The failure mode is **picking a film through association instead of analysis**.

Association: niche is "tech startup" → The Social Network comes to mind → recommend it.
Analysis: what specific lighting behavior, framing logic, scene rhythm, and material sense does this niche need? Which film in this director's catalog contains those qualities most precisely?

**Before committing to any film, answer these three questions:**

1. **What specific visual problem does this film solve for this niche?**
   Name a concrete cinematographic quality — not "it feels premium" or "it has a dark aesthetic." Something like: "Tarkovsky's *Stalker* uses extreme horizontal negative space and slow lateral reveals that match this architecture firm's need for spatial patience."

2. **Would this same film work equally well for three unrelated niches?**
   If yes, the selection is too generic. A film that "works for any premium brand" is not a director's choice — it is a mood board. Pick a film that fits this niche specifically because of what it shows, not because of what it is famous for.

3. **Are you picking the film or picking the film's reputation?**
   Films that are heavily discussed in design, tech, or film culture writing carry a reputation bias. If your reasoning relies on that reputation ("everyone knows this film has a dark, sharp aesthetic") rather than on specific scenes, shots, or director decisions — that is association, not analysis. Rebuild the justification from the film itself.

If any answer is unsatisfactory, choose a different film before proceeding to decisions.md.

Use this during Phase 2 when choosing hero archetypes, narrative arcs, and section archetypes.

The goal is to stop the agent from drifting toward the same shell, the same rhythm, or the same section logic across repeated projects or across multiple pages in the same site.

## Hash-Based Selection

When a library offers multiple director-compatible options, do not always pick the first or most obvious one.

- Build a director-compatible pool first.
- Use a stable site-name hash as the starting position.
- Walk the pool from that position, skipping entries that violate page-role or uniqueness constraints.

## Cross-Invocation Variation

The goal: every separate use of this skill should produce a visibly different style, even when there is no shared workspace history. Style is derived from the director + film, so a wide, non-repeating director+film draw is the load-bearing lever — palette, type, composition, and motion all follow from it. Do not rely on soft "be more varied" intentions; rotate the seed-driven selection below.

**Project seed.** Build a stable seed from `project/site name + niche` (lowercase, trimmed). This is the cross-invocation entropy: different project name or niche → different seed → different start index → different director → different downstream style. With no project name yet, seed on the niche plus the user's one-line brief.

**Director draw — span the full library, not the famous few.**

- The 200-director library is bucketed by genre, era, and region. From the niche, build a pool of *director-fit* candidates, then start at `seed mod pool length` and walk forward, skipping entries that violate page-role or uniqueness constraints.
- Do not keep landing on the same over-referenced names — Nolan, Villeneuve, Fincher, Wong Kar-wai, Kubrick, Wes Anderson, Ridley Scott, Tarantino and similar marquee directors. If the seed lands on one of these, you may keep it, but write a one-line justification in `decisions.md` for why this specific film solves this niche's visual problem better than a less obvious director in the pool. No justification → re-roll to the next pool entry.
- Across a user's repeated projects, the new director must come from a different genre/era/region bucket than their most recent comparable output unless they asked for a sequel.

**Palette lead — its own rotation axis.** Palette is semi-independent of the film (a film constrains mood, not the exact accent), so rotate it separately or palette becomes a hidden convergence vector. Derive a palette-lead index from `seed + a fixed offset` and rotate the lead across projects: red-led, green-led, cobalt/blue-led, viridian/teal-led, or a deliberate two-color tension pair. Stay in the saturated, primary-leaning space (not warm earth tones unless the chosen film demands it), keep AA contrast, and never repeat the previous project's lead. See the Color Direction rule in `SKILL.md`.

**Convergence audit (record in `decisions.md`).** Name, for this project versus the most recent comparable one: director bucket, palette lead, primary composition family, and motion language. If two or more match, re-roll the weakest axis before Phase 2.

## Minimum Rules

- Hero archetype: choose from Tier 1 and Tier 2 director-fit pools, then select via site-name hash.
- Narrative arc: select the director's default or variant arc via hash, not personal agent preference.
- Section archetype: choose via director pool plus hash, then apply page-role constraints.

## Cross-Page Anti-Convergence

For multi-page sites:

- The same function type should prefer a different archetype on different pages.
- The same archetype id may appear at most 2 times across the whole site, excluding footer-like repeats.
- Add page index offset to the site hash so each page starts at a different pool position.
- If two pages still converge, the lower-priority page must re-roll within the same director-compatible pool.

## Required Checks

Before Phase 2 is complete, confirm:

- Beat sequence matches the director's template instead of generic marketing flow.
- Beat count fits the director's typical range.
- Every section has a camera reference and an interaction reference, or an intentional `none`.
- At least 2 sections per page are structurally different from default marketing layouts.
- The homepage and interior pages do not reuse the same shell with only superficial changes.
