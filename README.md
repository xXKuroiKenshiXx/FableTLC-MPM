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

## Dirección del proyecto

La arquitectura objetivo es autoritativa desde el host:

1. El host simula combate, criaturas, NPCs y cambios del mundo.
2. Los clientes reciben snapshots validados y eventos discretos de juego.
3. Los jugadores remotos se representan como entidades proxy controladas por red.
4. Los cambios de región reconcilian entidades mediante IDs de red estables, no direcciones de memoria locales.

## Instalación

1. Instala una copia legítima para PC de *Fable: The Lost Chapters*.
2. Copia FableTLC-MPM la cual contiene `EgoMP.exe`, `EgoMP.dll` y `egomp.ini` junto a `Fable.exe` que seria la carpeta raíz del juego.
3. Configura la dirección del host y el puerto en `egomp.ini` (OPCIONAL).
4. Ejecuta `FableTLC-MPM-v.x.x.x.exe`, entra al mundo de juego y luego crea o conéctate a una sesión.

Consulta [INSTALL.md](INSTALL.md) para ver la instalación completa y la guía de solución de problemas.

## Controles predeterminados

| Acción | Tecla predeterminada |
| --- | --- |
| Crear sesión | `LEFT` |
| Conectar | `RIGHT` |
| Desconectar | `DOWN` |

Se recomienda usar `NUMPAD1`, `NUMPAD2` y `NUMPAD3` como alternativas para evitar conflictos con los controles normales del juego.

### 🐛 Reporte de problemas (Issues)
Si vas a reportar un problema o abrir un *Issue*, por favor asegúrate de incluir la siguiente información:
* **Versión/hash** del ejecutable de Fable.
* La **etiqueta de lanzamiento** (*release tag*) del mod.
* El **tipo de red** de ambos jugadores (LAN / VPN / Internet).
* Los valores del archivo `egomp.ini` *(⚠️ **Importante:** recuerda ocultar/censurar tus direcciones IP privadas por seguridad)*.
* El fragmento relevante del archivo de registro (*log*).

## 📝 Créditos y licencia
Puedes modificar y redistribuir el código libremente, siempre y cuando las obras derivadas sigan siendo de código abierto bajo la misma licencia.
Basado en el proyecto original [EgoMP](https://github.com/98thrxse/egomp) de 98thrxse. FableTLC-MPM se distribuye bajo la licencia [GPL-3.0](LICENSE).

Fable: The Lost Chapters y todos los recursos originales del juego pertenecen a sus respectivos propietarios incluyendo [Microsoft](https://en.wikipedia.org/wiki/Microsoft) y [Lionhead Studios](https://en.wikipedia.org/wiki/Lionhead_Studios). Este repositorio no contiene recursos originales del juego; se requiere una copia legítima para utilizar el mod.
