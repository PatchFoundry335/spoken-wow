# Spoken Audio Packs :: WoW 3.3.5a Compatibility

Spoken supports separately downloaded audio packs for Quests, Zones,
and Books, in multiple languages.

Some audio packs require two small changes to their `.toc` files to
work with the original World of Warcraft 3.3.5a (build 12340) client.

These changes do not require modifying the audio files.

## 1. Locate the audio pack

Open your WoW installation's `Interface/AddOns` directory.

Find the audio pack you downloaded. Examples:

- `SpokenBooksAudio`
- `SpokenZonesAudio`
- `SpokenZonesAudio_ptBR`
- `SpokenQuestsAudioAlliance`
- `SpokenQuestsAudioHorde`
- `SpokenQuestsAudioShared`
- `SpokenQuestsAudioGossip`

The folder names may differ for other languages.

## 2. Set the interface version

Open the `.toc` file inside the audio pack's folder.

Find the line beginning with `## Interface:` and replace it with:

    ## Interface: 30300

The original 3.3.5a client requires a single interface version.

## 3. Correct file path separators

In the TOC's file-loading entries, replace forward slashes (`/`)
with backslashes (`\`).

For example:

Before:

    Data/Sounds.lua

After:

    Data\Sounds.lua

The same applies to other `.lua` or `.xml` file references.

Do not modify metadata (`##` lines) or comments (`#` lines).

## 4. Save and restart WoW

Save the TOC and restart World of Warcraft.

At the character-selection screen, check the AddOns list.

Quest audio packs may use `## LoadOnDemand: 1`. Leave that setting
unchanged; it is intentional.

## Troubleshooting

### Spoken Zones: No Voice Pack Installed

If the audio pack appears installed but Spoken Zones reports
"No Voice Pack Installed", check the TOC's file references.

For example, `Data/Sounds.lua` must be `Data\Sounds.lua` on the
original 3.3.5a client.

If that Lua file does not load, the audio pack cannot register itself.

### Audio pack appears out of date

Verify that its TOC contains exactly:

    ## Interface: 30300

### Audio stopped working after an update

Updating or reinstalling an audio pack may overwrite your edited
TOC. Repeat the two compatibility fixes if necessary.

## Notes

- These instructions apply to original WoW 3.3.5a, not modern Wrath Classic.
- Preserve language, quality, bitrate, LoadOnDemand, and other metadata.
- You do not need to change the audio files.
- Not every pack requires both changes; inspect its TOC first.
- These TOC changes address loading compatibility only. Other
  incompatibilities may require separate fixes.
