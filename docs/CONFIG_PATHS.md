# Config and mod paths

`{GAME_DIR}` is the install folder (the one that contains `bin/x64/Cyberpunk2077.exe`).

## Settings (`UserSettings.json`)

| Platform                             | Folder                                                                                                  |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------- |
| Windows (Steam, GOG, Epic, MS Store) | `%LOCALAPPDATA%\CD Projekt Red\Cyberpunk 2077\`                                                         |
| Linux / Steam Deck (Proton)          | `steamapps/compatdata/1091500/pfx/drive_c/users/steamuser/AppData/Local/CD Projekt Red/Cyberpunk 2077/` |

The path is the same for all stores. The Proton path is the Windows path inside the Proton prefix of Steam app 1091500.

## Engine INIs

INI tweaks go into `{GAME_DIR}\engine\config\platform\pc\`. Add a new, own `.ini` file there; never overwrite an existing `user.ini`.

## Mod folders (relative to `{GAME_DIR}`)

| Folder                                     | Content                            |
| ------------------------------------------ | ---------------------------------- |
| `archive/pc/mod`                           | `.archive` / `.xl` mods            |
| `r6/scripts`                               | Redscript mods (`.reds`)           |
| `r6/tweaks`                                | TweakXL tweaks (`.tweak`, `.yaml`) |
| `bin/x64/plugins/cyber_engine_tweaks/mods` | Cyber Engine Tweaks Lua mods       |
| `red4ext/plugins`                          | RED4ext plugins                    |

## Sources

- [PCGamingWiki: Cyberpunk 2077](https://www.pcgamingwiki.com/wiki/Cyberpunk_2077) (config location, INI folder)
- [REDmodding wiki: Modding Cyberpunk 2077](https://wiki.redmodding.org/cyberpunk-2077-modding/for-mod-users/users-modding-cyberpunk-2077) (mod folders)
- [Cyber Engine Tweaks: Installing](https://wiki.redmodding.org/cyber-engine-tweaks/getting-started/installing) (CET mods folder)
- [RED4ext: Installing a plugin](https://docs.red4ext.com/getting-started/installing-a-plugin) (`red4ext/plugins`)
