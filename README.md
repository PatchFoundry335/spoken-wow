# Spoken 3.5.1 — WotLK 3.3.5a Compatibility Port

> **Unofficial compatibility port** of [Spoken by rusty-key](https://github.com/rusty-key/spoken-wow) for the original World of Warcraft: Wrath of the Lich King **3.3.5a (build 12340)** client.

## Download

**[Download Spoken 3.5.1 for WotLK 3.3.5a](https://github.com/PatchFoundry335/spoken-wow/releases/download/wotlk-v3.5.1/Spoken-v3.5.1-WotLK-3.3.5a.zip)**

[View release notes](https://github.com/PatchFoundry335/spoken-wow/releases/tag/wotlk-v3.5.1)

Use the release ZIP for installation, **not** GitHub's automatically generated source-code ZIP. The repository contains development tools and files for multiple WoW clients.

## Included addons

The 3.5.1 release includes four folders, all ported to WotLK 3.3.5a:

| Folder | Purpose |
| --- | --- |
| `Spoken` | Core voice player, narration UI, settings, playback queue, and Azeroth's Compendium |
| `Spoken_Quests` | Quest dialogue and NPC gossip |
| `Spoken_Places` | Zone and subzone lore narration |
| `Spoken_Readables` | Books, letters, notes, plaques, and other readable objects |

These are the current module names. Earlier addon folders such as `Spoken_Zones`, `Spoken_Books`, `SpokenQuests`, `SpokenZones`, and `SpokenBooks` are **not** part of this release.

## Installation

1. Download the [WotLK 3.5.1 release ZIP](https://github.com/PatchFoundry335/spoken-wow/releases/download/wotlk-v3.5.1/Spoken-v3.5.1-WotLK-3.3.5a.zip).
2. Close World of Warcraft.
3. Remove older Spoken **addon module folders** before replacing them. Keep separately installed audio packs.
4. Extract the ZIP directly into `World of Warcraft/Interface/AddOns/`.
5. At the character selection screen, open **AddOns** and enable the four Spoken modules.

The folder layout should be:

```text
Interface/
└── AddOns/
    ├── Spoken/
    │   └── Spoken.toc
    ├── Spoken_Quests/
    │   └── Spoken_Quests.toc
    ├── Spoken_Places/
    │   └── Spoken_Places.toc
    └── Spoken_Readables/
        └── Spoken_Readables.toc
```

Make sure there is no extra outer directory between `AddOns/` and these four folders.

### Voice packs

**Voice recordings are separate downloads** and are not included in this release ZIP. Spoken and its content modules need compatible audio packs to play recorded narration. Existing compatible packs may be reused.

For audio packs, see the [upstream Spoken releases](https://github.com/rusty-key/spoken-wow/releases) and CurseForge listings for [quests](https://www.curseforge.com/wow/addons/spoken-quests-audio-all), [places](https://www.curseforge.com/wow/addons/spoken-audio-places), and [readables](https://www.curseforge.com/wow/addons/spoken-audio-readables). Packs intended for newer clients are not necessarily compatible with original WotLK 3.3.5a.

## Features in this port

- Voiced quest dialogue and NPC gossip
- Zone and subzone lore narration through **Spoken Places**
- Books, plaques, and other readable text through **Spoken Readables**
- Narration controls, settings, and playback queue adapted for WotLK
- **Azeroth's Compendium** for browsing and replaying supported quests, places, and readables
- Compatibility changes for WotLK's older game APIs and Lua 5.1

All four modules, settings, and the Compendium have been tested in-game on WotLK 3.3.5a. Some UI details may differ from the modern-client version.

## Source branches

| Branch | Description |
| --- | --- |
| [`wotlk-3.5.1`](https://github.com/PatchFoundry335/spoken-wow/tree/wotlk-3.5.1) | Current 3.5.1 compatibility port |
| [`wotlk-3.3.5a`](https://github.com/PatchFoundry335/spoken-wow/tree/wotlk-3.3.5a) | Previous WotLK compatibility port |

This is a compatibility fork rather than a clean merge of upstream Git history. GitHub's ahead/behind commit counts reflect that history and do not, by themselves, indicate whether the port includes current addon files.

The repository also contains the upstream project's web application, build tools, tests, and other development infrastructure. **Install from the WotLK release ZIP**, not the repository source tree.

## Credits and licensing

Spoken is developed by **[rusty-key](https://github.com/rusty-key/spoken-wow)** and upstream contributors. This fork supplies unofficial compatibility changes for the original 3.3.5a client and is not an official upstream release or affiliated with Blizzard Entertainment.

See [THIRD_PARTY.md](THIRD_PARTY.md) and the upstream project for licensing and attribution of third-party code, game text, artwork, and other materials.
