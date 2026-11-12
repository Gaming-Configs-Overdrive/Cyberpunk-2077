[![Release](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/release.yml/badge.svg)](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/release.yml)
[![Lint](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/lint.yml/badge.svg)](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/lint.yml)
[![Pages](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/pages.yml/badge.svg)](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/pages.yml)

# Cyberpunk 2077

> [English Readme version here](./README.md)
>
> [Release Changelog](./CHANGELOG.md)

Optimierte Configs und QoL-Mods für Cyberpunk 2077 (Steam, GOG, Epic; Windows und Linux/Proton).

## Worum geht es?

Noch sind keine Configs oder Mods enthalten. Das Manifest [game.yml](./game.yml) beschreibt das Spiel bereits (Stores, Executable, Mod-Ordner), damit der Installer `gco-install` es erkennt, sobald Inhalte dazukommen.

Wo das Spiel Einstellungen, INIs und Mods ablegt: [docs/CONFIG_PATHS.md](./docs/CONFIG_PATHS.md) (Englisch).

## Installation (empfohlen)

1. `fullrelease.zip` aus den [Releases](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/releases) herunterladen und entpacken.
2. Spiel schließen.
3. `install.bat` (Windows) oder `install.sh` (Linux/Steam Deck) ausführen oder den Installer direkt nutzen:
   ```bash
   gco-install install --dry-run
   gco-install install
   ```
   Der Installer erkennt das Spiel (Steam/Epic/GOG, Proton), zeigt einen Plan und sichert jede Datei, die er ändert.
4. Alles rückgängig machen mit `gco-install restore`.

## Manuelle Installation

1. `config.zip` (Configs) und bei Bedarf `modpack.zip` (Mods, relativ zum Spielordner) herunterladen.
2. Die Config-Dateien an die Pfade aus [docs/CONFIG_PATHS.md](./docs/CONFIG_PATHS.md) kopieren.
3. `modpack.zip` in den Spielordner entpacken.
4. Die in `MODS.md` als `link` gelisteten Mods von ihrer Quelle herunterladen.

Downloads prüfen mit `sha256sum -c SHA256SUMS`.

## Mods

Versionen, Quellen und Lizenzen stehen in `MODS.md` im Release.

## Allgemeine Hinweise

- Eigene Engine-Tweaks als neue `.ini`-Datei in `engine/config/platform/pc/` ablegen; `user.ini` nie überschreiben.
- Spiel-Updates können Configs zurücksetzen; nach einem Patch den Installer erneut ausführen.

## Entwicklung

```bash
npm install
npm run validate
npm run build
npm test
```

Manifest-Referenz: [docs/GAME_MANIFEST.md](./docs/GAME_MANIFEST.md).
