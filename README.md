[![Release](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/release.yml/badge.svg)](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/release.yml)
[![Lint](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/lint.yml/badge.svg)](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/lint.yml)
[![Pages](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/pages.yml/badge.svg)](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/pages.yml)

# Cyberpunk 2077

> [Deutsche Readme Version hier](./README.de.md)
>
> [Release Changelog](./CHANGELOG.md)

Optimized configs and QoL mods for Cyberpunk 2077 (Steam, GOG, Epic; Windows and Linux/Proton).

## What is this about?

No configs or mods are included yet. The manifest [game.yml](./game.yml) already describes the game (stores, executable, mod folders), so the installer `gco-install` can detect it once content is added.

Where the game keeps its settings, INIs and mods: [docs/CONFIG_PATHS.md](./docs/CONFIG_PATHS.md).

## Installing (recommended)

1. Download `fullrelease.zip` from the [Releases](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/releases) and extract it.
2. Close the game.
3. Run `install.bat` (Windows) or `install.sh` (Linux/Steam Deck), or use the installer directly:
   ```bash
   gco-install install --dry-run
   gco-install install
   ```
   The installer detects the game (Steam/Epic/GOG, Proton), shows a plan and backs up every file it touches.
4. Undo everything with `gco-install restore`.

## Installing manually

1. Download `config.zip` (configs) and, if needed, `modpack.zip` (mods, relative to the game folder).
2. Copy the config files to the paths in [docs/CONFIG_PATHS.md](./docs/CONFIG_PATHS.md).
3. Extract `modpack.zip` into the game folder.
4. Download the mods listed as `link` in `MODS.md` from their source.

Verify downloads with `sha256sum -c SHA256SUMS`.

## Mods

See `MODS.md` in the release for versions, sources and licenses.

## General Advice

- Put own engine tweaks into a new `.ini` file in `engine/config/platform/pc/`; never overwrite `user.ini`.
- Game updates can reset config files; run the installer again after a patch.

## Development

```bash
npm install
npm run validate
npm run build
npm test
```

Manifest reference: [docs/GAME_MANIFEST.md](./docs/GAME_MANIFEST.md).
