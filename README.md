[![Release](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/release.yml/badge.svg)](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/release.yml)
[![Lint](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/lint.yml/badge.svg)](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/lint.yml)
[![Pages](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/pages.yml/badge.svg)](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/pages.yml)

# Cyberpunk 2077

> [Deutsche Readme Version hier](./README.de.md)
>
> [Release Changelog](./CHANGELOG.md)

PC mod setup for Cyberpunk 2077 patch 2.5 (Steam, GOG and Epic).

## Mods for patch 2.5

This release links to six core frameworks, Equipment-EX and Native Settings UI. See `MODS.md` in the [Releases](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/releases) for exact versions, dependencies, sources and licenses. Find the manifest and documentation in `fullrelease.zip`. Download mod files directly from their authors.

[Update 2.5](https://www.cyberpunk.net/en/news/52120/check-out-whats-coming-to-night-city-in-the-edgerunners-2-update-for-cyberpunk-2077) also added an in-game **Mods** menu with a curated, cross-platform catalog powered by mod.io. For mods from that catalog, follow the [CD PROJEKT RED setup guide](https://support.cdprojektred.com/en/cyberpunk/pc/gameplay/issue/3034/cross-platform-mod-support-how-to-1). The PC frameworks here use the authors’ installation steps.

## Installing PC mods

1. Close the game and download `MODS.md` from the release.
2. Install the linked frameworks in the listed order. Follow each author's instructions, especially when replacing an older version.
3. Launch to the main menu before adding optional mods. On Steam Deck or Linux, check the authors’ Proton instructions.

If the game fails to launch after updating, follow the [patch 2.5 troubleshooting guide](./docs/PATCH_2_5.md).

See [config and mod paths](./docs/CONFIG_PATHS.md) for installation locations.

## General Advice

- Put custom engine tweaks into a new `.ini` file in `engine/config/platform/pc/` and keep `user.ini` intact.

## Development

```bash
npm install
npm run validate
npm run build
npm test
```

Manifest reference: [docs/GAME_MANIFEST.md](./docs/GAME_MANIFEST.md).
