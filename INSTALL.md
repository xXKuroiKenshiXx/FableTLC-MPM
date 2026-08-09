# Installation

## Requirements

- A legitimate PC copy of Fable: The Lost Chapters.
- Windows.
- Dos PCs o dos instancias capaces de conectarse por red/VPN.
- Permitir el puerto UDP/TCP configurado en `egomp.ini` segun el entorno de prueba.

## Archivos incluidos

- `EgoMP.exe`
- `EgoMP.dll`
- `egomp.ini`
- `README.md`
- `LICENSE`
- `CHANGELOG.md`
- `INSTALL.md`
- `SHA256SUMS.txt`

## Setup

1. Back up your save files, then open the Fable TLC installation folder.

   En Steam suele ser:

   ```text
   C:\Program Files (x86)\Steam\steamapps\common\Fable The Lost Chapters
   ```

2. Copy these files next to `Fable.exe`:

   ```text
   EgoMP.exe
   EgoMP.dll
   egomp.ini
   ```

3. Edit `egomp.ini`.

   Para el host:

   ```ini
   [network]
   hostPort=60000
   ```

   Para el cliente:

   ```ini
   [network]
   hostIP=IP_DEL_HOST
   hostPort=60000
   ```

4. Allow the configured port in Windows Firewall/router when required, then start `EgoMP.exe`.

5. Load into the game world before using the multiplayer hotkeys:

   - Host: pulsa la tecla configurada como `host`.
   - Cliente: pulsa la tecla configurada como `connect`.
   - Desconectar: pulsa la tecla configurada como `disconnect`.

## Recommended controls

El archivo incluido usa:

```ini
[keys]
host=LEFT
connect=RIGHT
disconnect=DOWN
```

Si esas teclas molestan durante el juego, cambia a:

```ini
[keys]
host=NUMPAD1
connect=NUMPAD2
disconnect=NUMPAD3
```

## Alpha limitations

Esta version sirve para pruebas tecnicas. Todavia no es una experiencia cooperativa completa:

- No sincroniza dano/vida.
- No sincroniza enemigos.
- No sincroniza NPCs del mundo.
- No sincroniza quests ni estado persistente.
- Puede romperse al cambiar de region o al usar versiones distintas de `Fable.exe`.

## File verification

Puedes comparar los hashes SHA256 con `SHA256SUMS.txt`.
