# Changelog

All notable changes to this project are documented here. This project is under
active development and follows the versioning rules in `CLAUDE.md`
(patch-by-default).

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
