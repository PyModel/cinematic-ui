# Cleanup Plan — cinematic-ui → Pythoughts / Mohamed Elkholy

## Goal

Repoint this skill repo from `akseolabs-seo/cinematic-ui` to the `Pythoughts`
org, ship as a real npm package (`@Pythoughts/cinematic-ui`), and credit
Mohamed Elkholy as author and maintainer.

## Steps

- [x] 1. Add `LICENSE` (MIT) — currently referenced but missing.
- [x] 2. Add `package.json` (scoped `@Pythoughts/cinematic-ui`, Mohamed Elkholy, MIT, `files` whitelist, no deps, `engines.node`).
- [x] 3. Refresh `package-lock.json` to match.
- [x] 4. Rewrite `skill.json` — author/repo/homepage → Pythoughts; keep version in sync.
- [x] 5. Rewrite `agents/openai.yaml` — author + repository → Pythoughts.
- [x] 6. Sweep `CLAUDE.md`, `CODEX.md` for repo URLs → `github.com/Pythoughts/cinematic-ui`. Removed zh READMEs per request.
- [x] 7. Update `SECURITY.md` maintainer contact.
- [x] 8. Add primary `README.md` (English) — currently missing, only zh variants exist.
- [x] 9. Drop broken `docs/banner.svg` references from zh READMEs; remove the empty `docs/` folder.
- [x] 10. Extend `.gitignore` with `node_modules/`, `dist/`.
- [x] 11. Append rebrand / npm-publish entry to `CHANGELOG.md`.
- [x] 12. Verify: `npm pack --dry-run` lists the right files; no `akseolabs` strings remain. Result: 46 files, 703 KB packed, 3 MB unpacked.

## Out of scope (YAGNI)

- No `postinstall` script that mutates the user's home dir.
- No `bin/` CLI — `npx cinematic-ui` would just print help; users `cp -r` or symlink instead.
- No CI workflow — repo owner can add `.github/workflows/publish.yml` if desired.
- No actual `npm publish` — sandbox has no npm auth and no org membership proof. Owner runs `npm publish --access public` after `npm login` and adding `Pythoughts` to their orgs.

## Publish command (for the owner)

```bash
npm login
npm publish --access public
```
