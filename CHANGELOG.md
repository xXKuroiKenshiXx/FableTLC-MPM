# Changelog

All notable changes to FableTLC-MPM are documented here. Releases describe only functionality that has been tested or is present in the shipped package.

## [Unreleased]

### Planned

- Stable session protocol and compatibility checks.
- Host-authoritative combat, health and creature replication.
- Stable network IDs and region-transition reconciliation.

## [0.1.0-alpha] — Original baseline

This tag preserves the version that existed before the subsequent multiplayer-architecture work.

### Included

- Host, connect and disconnect flow.
- Remote player/proxy creation.
- Initial movement and rotation synchronization.
- `egomp.ini` configuration for keys, host IP and port.
- `EgoMP.exe` launcher and `EgoMP.dll` runtime.

### Known limitations

- No shared health, damage, attacks or combat resolution.
- No enemy/NPC, inventory, quest, spell, loot or world-state synchronization.
- Each installation simulates its own local world.
- Region changes and unsupported executable builds may desynchronize or fail.

[Unreleased]: https://github.com/xXKuroiKenshiXx/FableTLC-MPM/compare/v0.1.0-alpha...HEAD
[0.1.0-alpha]: https://github.com/xXKuroiKenshiXx/FableTLC-MPM/releases/tag/v0.1.0-alpha
