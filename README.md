# FableTLC-MPM

> Experimental multiplayer mod for **Fable: The Lost Chapters**.

[![Release](https://img.shields.io/github/v/release/xXKuroiKenshiXx/FableTLC-MPM?include_prereleases&style=flat-square)](https://github.com/xXKuroiKenshiXx/FableTLC-MPM/releases)
[![License](https://img.shields.io/github/license/xXKuroiKenshiXx/FableTLC-MPM?style=flat-square)](LICENSE)
[![Status](https://img.shields.io/badge/status-experimental-e67e22?style=flat-square)](https://github.com/xXKuroiKenshiXx/FableTLC-MPM)

FableTLC-MPM is an open-source continuation of the multiplayer foundation established by [EgoMP](https://github.com/98thrxse/egomp). Its objective is to evolve basic remote-player synchronization into a stable, host-authoritative cooperative framework for Fable TLC.

> [!WARNING]
> This is early experimental software. Crashes, desyncs, incompatible game builds and missing gameplay systems are expected. Back up your save files before testing.

## Current state

| Available now | Not synchronized yet |
| --- | --- |
| Session host/connect/disconnect | Damage, health and combat |
| Remote player proxy | Enemies and NPCs |
| Basic movement and rotation | Quests, inventory and loot |
| INI-based network/key settings | Spells, map transitions and world state |

The original **`v0.1.0-alpha`** release is preserved as the baseline build. It proves the connection and remote-proxy flow, but it is not a complete shared-world multiplayer mod.

## Direction of the project

The target architecture is host-authoritative:

1. The host simulates combat, creatures, NPCs and world changes.
2. Clients receive validated snapshots and discrete gameplay events.
3. Remote players are represented by network-controlled proxy entities.
4. Region changes reconcile entities by stable network IDs instead of local memory addresses.

## Installation

1. Install a legitimate PC copy of *Fable: The Lost Chapters*.
2. Copy `EgoMP.exe`, `EgoMP.dll` and `egomp.ini` next to `Fable.exe`.
3. Configure the host address and port in `egomp.ini`.
4. Launch `EgoMP.exe`, load into the game world, then host or connect.

Read [INSTALL.md](INSTALL.md) for the complete setup and troubleshooting guide.

## Default controls

| Action | Default key |
| --- | --- |
| Host session | `LEFT` |
| Connect | `RIGHT` |
| Disconnect | `DOWN` |

`NUMPAD1`, `NUMPAD2` and `NUMPAD3` are recommended alternatives to avoid conflicts with normal gameplay.

## Compatibility

FableTLC-MPM targets the PC version of *Fable: The Lost Chapters*. The mod depends on reverse-engineered game internals, therefore all testers should use the same supported `Fable.exe` build and the same mod release.

## Releases

- [`v0.1.0-alpha`](docs/releases/v0.1.0-alpha.md) — original baseline: connection, remote proxy and basic transform updates.
- Future releases will document their synchronization guarantees rather than claiming unimplemented multiplayer features.

## Credits and license

Based on the original [EgoMP](https://github.com/98thrxse/egomp) project by 98thrxse. FableTLC-MPM is licensed under [GPL-3.0](LICENSE).

Fable: The Lost Chapters and all original game assets belong to their respective owners. This repository contains no original game assets; a legitimate copy of the game is required.
