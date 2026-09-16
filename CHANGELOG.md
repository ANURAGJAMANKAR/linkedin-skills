# Changelog

All notable changes to this project are documented here. This project follows
the versioning rules in `CLAUDE.md` (patch-by-default).

## [1.1.13] - 2026-09-16

### Changed
- Ownership transferred to **Anurag Jamankar**. Authorship and copyright
  metadata updated across `LICENSE`, `.claude-plugin/plugin.json`,
  `.claude-plugin/marketplace.json`, `.codex-plugin/plugin.json`, and the
  commit-author rules in `CLAUDE.md` / `AGENTS.md`.
- `SECURITY.md` contact updated to the maintainer's email.

### Fixed
- Restored the `.claude/skills/` symlink mirror (all 12 skills), which had been
  flattened into plain text files during packaging. Claude Code now discovers
  every skill again.

### Added
- `CONTRIBUTORS.md` crediting the maintainer, the original author, and
  contributors.
- This `CHANGELOG.md`.

## [1.1.12] - prior

- Baseline bundle: 12 LinkedIn marketing skills for Claude Code and Codex, with
  the Publora publish layer, Apify read layer, and optional Pixfaro image layer.
