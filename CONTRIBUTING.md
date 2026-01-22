# Contributing to Tech of Our Own

Thanks for helping build non-extractive, user-owned technology.

This document is the **organization-wide** contributing guide for all repositories in the
`techofourown` GitHub organization. Individual repos may add *extra* repo-specific instructions,
but they should not contradict this baseline.

## 1) The rules that matter most

1. **No surprise extraction.** Proposals that add telemetry, dark patterns, lock-in, subscriptions,
   or hostage mechanics will be rejected on sight.
2. **Local-first is the default.** Network features must not become dependency.
3. **Be auditable.** Prefer changes that increase inspectability, reproducibility, and clarity.
4. **Be kind and rigorous.** Follow the Code of Conduct.

Code of Conduct:
https://github.com/techofourown/.github/blob/main/CODE_OF_CONDUCT.md

## 2) Where to start

- Read the org docs and decision process:
  https://github.com/techofourown/org-techofourown/blob/main/docs/README.md
- For OurBox OS: start in `sw-ourbox-os`
- For OurBox hardware: start in `pf-ourbox` (contains Matchbox + Tinderbox models)
- For image builds: start in `img-ourbox-mini-rpi`

## 3) How changes get made (the default workflow)

### 3.1 Small changes (docs, fixes, cleanup)
1. Open a Pull Request directly.
2. Keep scope tight.
3. Explain the "why" in the PR description.

### 3.2 Big changes (architecture, governance, security posture, naming, licensing)
Use the RFC/ADR process:

- **RFC** = explore options + tradeoffs before we decide
- **ADR** = record the decision after we decide

Each repo already has `docs/rfcs/` and `docs/decisions/` conventions; follow them.

## 4) Pull request standards

A PR must include:

- A clear title and summary (what + why).
- Any docs updates needed so the repo stays self-explanatory.
- If behavior changes: notes on compatibility and migration.
- If it touches security or privacy: explicit threat/impact notes.

### 4.1 Review etiquette
- Ask questions; don't assume malice.
- Critique the work, not the person.
- If you think something violates the mission, say so plainly and cite the relevant founding docs.

## 5) Repo types: hardware vs software vs images

### 5.1 Hardware repos (`hw-*`)
Hardware contributions should update documentation alongside design decisions.

Minimum expectations for hardware PRs:
- Update `docs/specs/` (BOM, system requirements, etc.) when relevant.
- Add an ADR for material design choices (components, enclosure, storage strategy, etc.).
- Keep part choices legible and supportable (avoid fragile single-vendor traps when practical).

### 5.2 Software repos (`sw-*`)
Minimum expectations for software PRs:
- Keep builds reproducible; avoid "works on my machine" instructions.
- Update specs/docs when behavior changes.
- Prefer secure defaults.

### 5.3 Image repos (`img-*`) and firmware repos (`fw-*`)
Image/firmware changes must be:
- repeatable (documented build steps)
- reviewable (clear diffs; avoid giant opaque blobs)
- release-friendly (changes should map cleanly to tagged releases)

## 6) Commit conventions

Use Conventional Commit style. Examples:
- `feat: add X`
- `fix: correct Y`
- `docs: clarify Z`
- `chore: maintenance`

Many repos use semantic-release. Clean commit history helps releases stay boring.

## 7) Licensing (inbound = outbound)

Unless a repository explicitly states otherwise, contributions are accepted under the repository's
license. Do not contribute code/designs you don't have the right to license.

## 8) Security issues

Do not open public issues for vulnerabilities or sensitive security problems.
Follow:
https://github.com/techofourown/.github/blob/main/SECURITY.md
