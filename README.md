# FableTLC-MPM

> Mod multijugador experimental para **Fable: The Lost Chapters**.

[![Release](https://img.shields.io/github/v/release/xXKuroiKenshiXx/FableTLC-MPM?include_prereleases&style=flat-square)](https://github.com/xXKuroiKenshiXx/FableTLC-MPM/releases)
[![Licencia](https://img.shields.io/github/license/xXKuroiKenshiXx/FableTLC-MPM?style=flat-square)](LICENSE)
[![Estado](https://img.shields.io/badge/estado-experimental-e67e22?style=flat-square)](https://github.com/xXKuroiKenshiXx/FableTLC-MPM)

FableTLC-MPM es una continuación de código abierto de la base multijugador creada por [EgoMP](https://github.com/98thrxse/egomp). Su objetivo es transformar la sincronización básica de jugadores remotos en una infraestructura cooperativa estable y autoritativa para Fable TLC.

> [!WARNING]
> Este software se encuentra en una etapa experimental temprana. Son esperables cierres inesperados, desincronización, incompatibilidades con versiones del juego y sistemas de juego incompletos. Haz una copia de seguridad de tus partidas antes de probarlo.

## Estado actual

| Disponible actualmente | Aún no sincronizado |
| --- | --- |
| Crear, conectar y desconectar sesiones | Daño, vida y combate |
| Proxy del jugador remoto | Enemigos y NPCs |
| Movimiento y rotación básicos | Misiones, inventario y botín |
| Configuración de red y teclas mediante INI | Hechizos, transiciones de mapa y estado del mundo |

La versión original **`v0.1.0-alpha`** se conserva como la compilación base. Demuestra la conexión y el proxy remoto, pero no es todavía un mod multijugador de mundo compartido completo.

## Dirección del proyecto

La arquitectura objetivo es autoritativa desde el host:

1. El host simula combate, criaturas, NPCs y cambios del mundo.
2. Los clientes reciben snapshots validados y eventos discretos de juego.
3. Los jugadores remotos se representan como entidades proxy controladas por red.
4. Los cambios de región reconcilian entidades mediante IDs de red estables, no direcciones de memoria locales.

## Instalación

1. Instala una copia legítima para PC de *Fable: The Lost Chapters*.
2. Copia `EgoMP.exe`, `EgoMP.dll` y `egomp.ini` junto a `Fable.exe`.
3. Configura la dirección del host y el puerto en `egomp.ini`.
4. Ejecuta `EgoMP.exe`, entra al mundo de juego y luego crea o conéctate a una sesión.

Consulta [INSTALL.md](INSTALL.md) para ver la instalación completa y la guía de solución de problemas.

## Controles predeterminados

| Acción | Tecla predeterminada |
| --- | --- |
| Crear sesión | `LEFT` |
| Conectar | `RIGHT` |
| Desconectar | `DOWN` |

Se recomienda usar `NUMPAD1`, `NUMPAD2` y `NUMPAD3` como alternativas para evitar conflictos con los controles normales del juego.

## Compatibilidad

FableTLC-MPM está dirigido a la versión para PC de *Fable: The Lost Chapters*. El mod depende de componentes obtenidos mediante ingeniería inversa; por ese motivo, todos los jugadores deben usar la misma compilación compatible de `Fable.exe` y la misma versión del mod.

## Releases

- [`v0.1.0-alpha`](docs/releases/v0.1.0-alpha.md) — versión base original: conexión, proxy remoto y actualizaciones básicas de posición/rotación.
- Las futuras versiones documentarán exactamente sus garantías de sincronización, sin prometer características multijugador que aún no estén implementadas.

## Créditos y licencia
Puedes modificar y redistribuir el código libremente, siempre y cuando las obras derivadas sigan siendo de código abierto bajo la misma licencia.
Basado en el proyecto original [EgoMP](https://github.com/98thrxse/egomp) de 98thrxse. FableTLC-MPM se distribuye bajo la licencia [GPL-3.0](LICENSE).

Fable: The Lost Chapters y todos los recursos originales del juego pertenecen a sus respectivos propietarios incluyendo [Microsoft](https://en.wikipedia.org/wiki/Microsoft) y [Lionhead Studios](https://en.wikipedia.org/wiki/Lionhead_Studios). Este repositorio no contiene recursos originales del juego; se requiere una copia legítima para utilizar el mod.
