[![Release](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/release.yml/badge.svg)](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/release.yml)
[![Lint](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/lint.yml/badge.svg)](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/lint.yml)
[![Pages](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/pages.yml/badge.svg)](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/actions/workflows/pages.yml)

# Cyberpunk 2077

> [English Readme version here](./README.md)
>
> [Release Changelog](./CHANGELOG.md)

PC-Mod-Setup für Cyberpunk 2077 Patch 2.5 (Steam, GOG und Epic).

## Mods für Patch 2.5

Dieses Release verlinkt sechs grundlegende Frameworks, Equipment-EX und Native Settings UI. Die genauen Versionen, Abhängigkeiten, Quellen und Lizenzen stehen in `MODS.md` unter [Releases](https://github.com/Gaming-Configs-Overdrive/Cyberpunk-2077/releases). Das Manifest und die Dokumentation liegen in `fullrelease.zip`. Lade die Mod-Dateien direkt bei den jeweiligen Autoren herunter.

[Update 2.5](https://www.cyberpunk.net/en/news/52120/check-out-whats-coming-to-night-city-in-the-edgerunners-2-update-for-cyberpunk-2077) hat außerdem das Menü **Mods** mit einem plattformübergreifenden Katalog von mod.io eingeführt. Für Mods aus diesem Katalog gilt die [Anleitung von CD PROJEKT RED](https://support.cdprojektred.com/en/cyberpunk/pc/gameplay/issue/3034/cross-platform-mod-support-how-to-1). Die hier aufgeführten PC-Frameworks installierst du nach den Anleitungen der Autoren.

## PC-Mods installieren

1. Schließe das Spiel und lade `MODS.md` aus dem Release herunter.
2. Installiere die verlinkten Frameworks in der angegebenen Reihenfolge. Beachte die Anleitungen der Autoren, insbesondere beim Austausch älterer Versionen.
3. Starte das Spiel bis zum Hauptmenü, bevor du optionale Mods hinzufügst. Unter Linux oder auf dem Steam Deck gelten die Proton-Hinweise der Autoren.

Falls das Spiel nach dem Update nicht startet, hilft die [Fehlersuche für Patch 2.5](./docs/PATCH_2_5.md) auf Englisch.

Die [Config- und Mod-Pfade](./docs/CONFIG_PATHS.md) zeigen die Installationsorte.

## Allgemeine Hinweise

- Lege eigene Engine-Tweaks als neue `.ini`-Datei in `engine/config/platform/pc/` ab und behalte die bestehende `user.ini` bei.

## Entwicklung

```bash
npm install
npm run validate
npm run build
npm test
```

Manifest-Referenz: [docs/GAME_MANIFEST.md](./docs/GAME_MANIFEST.md).
