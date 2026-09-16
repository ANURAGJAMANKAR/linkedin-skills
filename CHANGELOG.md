# Changelog

All notable changes to this project are documented here. This project is under
active development and follows the versioning rules in `CLAUDE.md`
(patch-by-default).

## [1.2.0] - 2026-09-16

Two new skills. The bundle grows from 12 to 14.

### Added
- **`linkedin-brand-manager`** — sets your overall LinkedIn strategy before you
  draft: niche positioning, target audience, content pillars, a cadence sized to
  your real weekly bandwidth, success metrics with 30/60/90 targets, and a growth
  roadmap. Writes `references/brand-profile.md`, which the planner and post writer
  read so every draft ladders up to the strategy.
- **`linkedin-content-log`** — the bundle's memory. Keeps
  `references/content-log.md`, a running record of every post, comment, and reply
  you draft. The writing skills check it before drafting to catch an accidental
  repeat (a genuine update on an evolving topic is allowed) and append to it after
  you approve.

### Changed
- `linkedin-post-writer`, `linkedin-repurposer`, and `linkedin-comment-drafter`
  now run the content-log repeat check before drafting and append after approval.
- `linkedin-content-planner` reads the brand profile for pillars and cadence, and
  the content log to avoid scheduling a topic just covered.
- Hero banner and README are now count-agnostic so the bundle can grow without
  stale numbers.

## [1.1.13] - 2026-09-16

Maintenance and improvement pass.

### Fixed
- Restored the `.claude/skills/` symlink mirror (all 12 skills), so Claude Code
  reliably discovers every skill again.

### Changed
- Refreshed project documentation (README, maintainer info) and regenerated the
  `.codex-marketplace` package via `scripts/sync_codex_marketplace.py`.

### Added
- `CONTRIBUTORS.md` and this `CHANGELOG.md`.

## [1.1.12] - prior

- Baseline bundle: 12 LinkedIn marketing skills for Claude Code and Codex, with
  the Publora publish layer, Apify read layer, and optional Pixfaro image layer.
