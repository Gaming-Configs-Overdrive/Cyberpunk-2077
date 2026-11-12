# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
This file is based on the Semver-Model ('Added', 'Changed', 'Removed')

## [Unreleased]

### Changed

- build: migrate to the new `game-config-skeleton`: plain Node 24 build with npm (`npm run build`), manifest check (`npm run validate`) and tests (`npm test`)
- ci: workflows are thin callers of the reusable workflows in `Gaming-Configs-Overdrive/.github`; `publish-readme.yml` renamed to `pages.yml`
- docs: README (EN/DE) rewritten for Cyberpunk 2077

### Added

- `game.yml` for Cyberpunk 2077: Steam/GOG/Epic ids, executable, process and mod folders (no configs or mods yet)
- `docs/CONFIG_PATHS.md`: settings, engine INI and mod paths incl. Proton
- `docs/ARCHITECTURE.md`, `docs/GAME_MANIFEST.md`, `schema/`, `test/`, `template-sync.yml`, `.templatesyncignore`, `renovate.json`, `_config.yml`, `.nvmrc`, `.prettierignore`

### Removed

- Rollup config, build plugins, `src/` utils, `yarn.lock` and `docs/ROLLUP_CONFIGURATION.md`
- `README.template.md` and the placeholder `1.0.0` changelog entry
