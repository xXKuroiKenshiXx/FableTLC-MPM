# FableTLC-MPM

Multiplayer mod experimental para **Fable: The Lost Chapters**, basado en EgoMP.

Este paquete apunta a transformar la sincronizacion basica de jugadores en una base real para multiplayer: clones remotos, movimiento en red, configuracion simple por archivo y una ruta tecnica hacia mundo autoritativo con NPCs, enemigos, vida y combate sincronizados.

## Estado actual

- Conexion basica entre dos instancias.
- Creacion de jugador remoto/proxy dentro de cada partida.
- Sincronizacion inicial de movimiento/rotacion.
- Configuracion por `egomp.ini`.
- Todavia no sincroniza combate, dano, inventario, quests, enemigos ni estado completo del mundo.

## Objetivo tecnico

La direccion del proyecto es usar una arquitectura host-authoritative:

- El host calcula enemigos, dano, vida y estado del mundo.
- Los clientes reciben snapshots/eventos desde el host.
- Los personajes remotos se representan como proxies/NPCs controlados por red.
- Los enemigos del cliente deben convertirse progresivamente en replicas pasivas del estado del host.

## Instalacion rapida

1. Instala **Fable: The Lost Chapters** en Steam.
2. Copia `EgoMP.exe`, `EgoMP.dll` y `egomp.ini` dentro de la carpeta principal del juego, junto a `Fable.exe`.
3. Edita `egomp.ini`.
4. El host debe abrir/permitir el puerto configurado.
5. Ejecuta `EgoMP.exe` para iniciar el mod.

Lee `INSTALL.md` para la instalacion completa.

## Controles por defecto

- Host: `LEFT`
- Connect: `RIGHT`
- Disconnect: `DOWN`

Se recomienda cambiar estas teclas por `NUMPAD1`, `NUMPAD2`, `NUMPAD3` para evitar conflictos durante el juego.

## Compatibilidad

Este mod esta pensado para **Fable: The Lost Chapters PC**. La ingenieria inversa actual depende de una version concreta de `Fable.exe`; si el ejecutable no coincide, algunas direcciones internas pueden fallar.

## Aviso importante

Este repositorio no incluye archivos propietarios de Fable, assets del juego, `game.bin`, texturas, mapas ni contenido distribuido por Lionhead/Microsoft. Solo contiene archivos del mod.

## Creditos

- Basado en EgoMP de 98thrxse.
- Usa ideas/tecnicas de modding e ingenieria inversa para Fable TLC.
- Fable: The Lost Chapters pertenece a Lionhead Studios / Microsoft.

## Licencia

GPL-3.0. Ver `LICENSE`.
