# Patch 2.5 startup troubleshooting

The Edgerunners 2 Update introduced a cross-platform mod catalog powered by mod.io. On PC, mods installed through Vortex or copied into the game directory still depend on their own loaders and frameworks. [CD PROJEKT RED patch notes](https://www.cyberpunk.net/en/news/52120/check-out-whats-coming-to-night-city-in-the-edgerunners-2-update-for-cyberpunk-2077) · [Official modding guide](https://www.cyberpunk.net/en/modding-support)

RED4ext 1.31.0 added support for using the in-game mod menu with redscript mods. [RED4ext release notes](https://github.com/WopsS/RED4ext/releases/tag/v1.31.0)

## Recover a modded PC install

1. Close the game. Back up `%USERPROFILE%\Saved Games\CD Projekt Red\Cyberpunk 2077\` and keep the current Vortex profile and downloads.
2. Purge the deployed mods using Vortex. Move any remaining manually installed mod files out of the game directory into a backup folder. Use the authors’ file lists to identify manual files, including loader DLLs in `bin/x64`. Keep the game’s `bin/x64/cyberpunk2077_addresses.json`, which the loaders use for that exact game build. Then verify game files in your store client. [CD PROJEKT RED file verification guide](https://support.cdprojektred.com/en/cyberpunk/pc/sp-technical/issue/1562/verify-integrity-of-game-files-1)
3. Launch to the main menu from your store client. Keep existing modded saves backed up and use a new game or a clean save for testing. If the unmodded game still fails to launch, follow [CD PROJEKT RED’s clean-install guide](https://support.cdprojektred.com/en/cyberpunk/pc/sp-technical/issue/2233/how-do-i-perform-a-clean-install-of-the-game).
4. Install the patch 2.5 frameworks linked in [game.yml](../game.yml) in their listed order. Launch with the frameworks alone and check the new logs.
5. Re-enable compatible mods in small batches and launch after each batch. If a batch fails, disable it and test its mods in smaller groups.

## What the local Steam logs showed

For the 2026-11-26 startup attempt, `bin/x64/Cyberpunk2077.exe` reported product version 2.50 and file version `3.0.88.46235`.

- `bin/x64/plugins/cyber_engine_tweaks/cyber_engine_tweaks.log` reports that CET 1.37.1 only supports game version 2.31. The author added support for this 2.5 build in [CET 1.38.0](https://github.com/maximegmd/CyberEngineTweaks/releases/tag/v1.38.0).
- The log in `red4ext/logs/` shows RED4ext 1.30.0 initializing, then ends while loading ArchiveXL. The deployed `ArchiveXL.dll` was 1.27.1. This identifies the point where logging stopped. The author’s [ArchiveXL 1.28.12 requirements](https://github.com/psiberx/cp2077-archive-xl/tree/v1.28.12#compatibility) list game version 2.5 and RED4ext 1.31.0 or newer.
- The same deployment contained Codeware 1.20.3 and TweakXL 1.11.3. The authors’ patch 2.5 versions are linked in [game.yml](../game.yml). The catalog pins [redscript 0.5.32](https://github.com/jac3km4/redscript/releases/tag/v0.5.32) because its release explicitly adds support for patch 2.5 and the linked frameworks list it as compatible.

The catalog records compatibility stated by the authors. Each mod and the combined load order still need a launch test on the target installation.
