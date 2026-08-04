# SWArmada

![Version](https://img.shields.io/badge/version-0.1.2-00d9ff)
![Platform](https://img.shields.io/badge/platform-Windows%20x64%20%7C%20Linux%20x86__64-6e7b8b)
![Status](https://img.shields.io/badge/status-early%20development-f08b32)

**An unofficial digital adaptation of the *Star Wars: Armada* tabletop game.**

Build a custom fleet, command capital ships and squadrons, and fight tactical
battles across a fully 3D battlespace. SWArmada translates the tabletop game's
movement, firing arcs, range bands, commands, defense tokens, upgrades, and
objectives into a playable digital format wrapped in a retro tactical CRT
interface.

[Download](#download-and-install) · [Features](#features) ·
[Screenshots](#screenshots) · [Project status](#project-status) ·
[Credits](#credits-and-acknowledgements)

## Screenshots

### 1. Main menu

![SWArmada main menu with worldwide player list](media/screenshots/1menu-online.png)

### 2. Fleet builder

![A completed Rebel Alliance fleet roster](media/screenshots/2fleet-builder.png)

### 3. Ship browser

![The fleet builder ship browser](media/screenshots/3ship-roster.png)

### 4. Squadron information

![A squadron information panel for the HWK-290](media/screenshots/4squadron-info.png)

### 5. Map editor

![Building a custom battlefield in the map editor](media/screenshots/5map-maker.png)

### 6. Command dial

![Programming a navigation command dial during battle](media/screenshots/6cmd-dial.png)

### 7. Tactical unit dossier

![A Hammerhead Corvette selected with its tactical dossier open](media/screenshots/7ship-dossier.png)

### 8. Firing arcs and range

![Selecting a target using firing arcs and range bands](media/screenshots/8range-arcs.png)

### 9. Capital ship combat

![Resolving damage during a capital ship attack](media/screenshots/9combat.png)

### 10. Squadron combat

![Squadrons engaged in close combat](media/screenshots/91squadron-combat.png)

### 11. Plotting movement

![Plotting a capital ship movement path](media/screenshots/92plot-movement.png)

### 12. Intel Retrieval

![A light ship choosing whether to begin downloading an Intel token](media/screenshots/10intel-retrieval.png)

### 13. Seize the Station

![An online Seize the Station objective battle](media/screenshots/11seize-the-station.png)

### 14. Escort the VIP

![A Gozanti VIP Command Transport en route to extraction](media/screenshots/12escort-the-vip.png)

### 15. Online lobby

![An Escort the VIP online lobby with fleets, roles, objective card, and chat](media/screenshots/13online-lobby.png)

## Features

- A fully 3D tactical battlespace for capital ships and squadrons
- Tabletop-inspired movement tools, firing arcs, and close, medium, and long
  range bands
- Attack dice, accuracy results, shields, hull damage, and defense tokens
- Command dials, ship activation, squadron activation, and round-based play
- Fleet creation and editing with ship, squadron, and upgrade libraries, plus
  text-list importing from Ryan Kingston and Star Forge formats
- Saved fleet archives and a fleet sandbox for testing compositions
- Local hotseat play and experimental online multiplayer support with Default,
  Escort the VIP, Seize the Station, and Intel Retrieval scenarios
- An opt-in worldwide player list with locally persistent `Username#NNNN`
  handles, direct match invitations, and persistent direct comms
- Custom battlefield and map-editing tools
- Laser fire, combat effects, spatial sound, and event-driven UI audio
- A global scanline/CRT presentation inspired by retro tactical displays

## What's new in 0.1.2

- Three playable objective modes: Escort the VIP, Seize the Station, and Intel
  Retrieval
- Scenario-aware custom maps, Fleet Sandbox, local setup, and online lobbies
- Fleet-text importing with catalog-based validation and point recalculation
- Official/Custom fleet rules across Fleet Builder and match setup
- Persistent direct comms, stronger presence expiry, and more reliable invites
- Automatic verified update downloads for Windows and Linux
- Tabletop ruler-correct squadron movement, ship-overlap handling, speed-0 yaw,
  huge-base range fixes, and extensive combat/UI corrections

See [the complete 0.1.2 release notes](RELEASE_NOTES_0.1.2.md) for the full
breakdown.

## Download and install

The current public build is **SWArmada 0.1.2** for **Windows x64** and
**Linux x86-64**.

1. Open the [`v0.1.2` release](https://github.com/thetrufflegouda/SWArmada/releases/tag/v0.1.2).
2. Download the archive for your platform.

### Windows x64

1. Download `SWArmada-0.1.2-Windows-x64.zip`.
2. Extract the entire ZIP to a writable folder.
3. Run `SWArmada.exe`.

Keep `SWArmada.exe` beside `SWArmada_Data`, `UnityPlayer.dll`, and the other
packaged files. Windows may show a security prompt because this early build is
not code-signed.

### Linux x86-64

1. Download `SWArmada-0.1.2-Linux-x86_64.tar.gz`.
2. Extract the entire archive.
3. Run `./SWArmada.x86_64` from the extracted folder.

The executable permission is stored in the archive. If your extraction tool
does not preserve it, run `chmod +x SWArmada.x86_64` first.

### Verify the download

SHA-256 checksums:

```text
605303C2D28A4C5A5A768D7E546BD503DD494B9FE9120AA6B6D3B472028DB782  SWArmada-0.1.2-Windows-x64.zip
8014EB09A9246C709185BD494137BD1C1B625D0E67CC71F469F4F73A31F34E37  SWArmada-0.1.2-Linux-x86_64.tar.gz
```

In PowerShell, compare it with:

```powershell
Get-FileHash .\SWArmada-0.1.2-Windows-x64.zip -Algorithm SHA256
```

On Linux, compare it with:

```bash
sha256sum SWArmada-0.1.2-Linux-x86_64.tar.gz
```

## How it plays

Start by creating a fleet from the available ships, squadrons, upgrades, and
objectives. During battle, deploy your forces, reveal commands, maneuver ships
with the navigation tool, activate squadrons, and resolve attacks through the
appropriate firing arc and range band. Unit dossiers keep the selected ship or
squadron's condition, speed, shields, firepower, and abilities visible while
you make decisions.

SWArmada aims to preserve the deliberate, measurement-driven character of the
tabletop game while letting the computer handle scene presentation, state
tracking, and online synchronization.

## Project status

Version `0.1.2` adds objective modes, scenario-aware setup, importing, direct
comms, verified update downloads, and a substantial tabletop-rules and UI pass
to the public baseline. It is an early build, not a finished commercial
release. Features, rules behavior, balance, presentation, saved data, and
multiplayer compatibility may change as the game develops. Bugs and incomplete
content should be expected.

This repository is the public release home for SWArmada. It contains project
information and release metadata; downloadable Windows and Linux builds are
attached to GitHub Releases.

## Feedback and bug reports

When the repository is live, use
[GitHub Issues](https://github.com/thetrufflegouda/SWArmada/issues) for a bug
report or feature request. Include the game version, what you were doing, what
you expected, and what happened. Screenshots are especially useful for visual
or gameplay-state problems.

## Credits and acknowledgements

### Project

- **Design and development:** [thetrufflegouda](https://github.com/thetrufflegouda)
- **Engine:** [Unity](https://unity.com/) with the Universal Render Pipeline,
  Input System, Netcode for GameObjects, and Unity Multiplayer Services

### Visuals and interface

- **Retro Shaders Pro for URP:** Daniel Ilett — used for the global CRT and
  retro display treatment
- **Aldrich:** Matthew Desmond / MADType — SIL Open Font License 1.1
- **Inter:** The Inter Project Authors — SIL Open Font License 1.1

### Game data, models, and source references

- **Star Forge:** [Polkadoty's Armada fleet builder](https://star-forge.tools/)
  and its public data were used as a reference for official fleet content
- **Tabletop Simulator Armada source material:**
  [Valadian / Jesse Berger's TabletopSimulatorIncludeDir](https://github.com/Valadian/TabletopSimulatorIncludeDir)
  was used as a source reference for portions of the model and texture library

Thank you to the *Star Wars: Armada* community, tool creators, mod authors,
playtesters, and everyone preserving and expanding the tabletop game.

More detailed attribution and licensing notes are available in
[THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md). If a credit is incomplete or
incorrect, please open an issue so it can be corrected.

## Disclaimer

SWArmada is an unofficial, non-commercial fan project. It is not affiliated
with, authorized by, sponsored by, or endorsed by Lucasfilm Ltd., The Walt
Disney Company, Fantasy Flight Games, Atomic Mass Games, or any other rights
holder named here.

*Star Wars* and related names, characters, artwork, and designs are the
property of their respective owners. *Star Wars: Armada* was created and
published by Fantasy Flight Games, with stewardship later moving to Atomic
Mass Games. Third-party names are used only for identification and
acknowledgement; attribution does not imply endorsement or permission.
