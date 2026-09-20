# Refugio Sync para UmbrelOS / Refugio Sync for UmbrelOS

App de la RefugioOS Community App Store que empaqueta Syncthing con acceso
a discos externos y USB conectados al Umbrel.

RefugioOS Community App Store app that packages Syncthing with access to
external drives and USB devices connected to Umbrel.

## Qué lo diferencia de la app oficial / What makes it different

La app oficial de Syncthing en Umbrel solo accede a su propia carpeta de datos
interna. Refugio Sync también monta `/media` del host (donde UmbrelOS pone los
discos externos) dentro del contenedor como `/external`, por lo que puedes
añadir cualquier disco directamente desde la UI de Syncthing sin SSH.

The official Syncthing app on Umbrel only accesses its own internal data folder.
Refugio Sync also mounts the host's `/media` (where UmbrelOS places external
drives) inside the container as `/external`, so you can add any drive directly
from the Syncthing UI without SSH.

## Primera configuración / First-time setup

```
1. Instala la app desde la RefugioOS Community Store.
   Install the app from the RefugioOS Community Store.

2. Abre Refugio Sync — verás la UI de Syncthing.
   Open Refugio Sync — you will reach the Syncthing web UI.

3. En el primer arranque Syncthing pedirá usuario y contraseña para la GUI.
   Ponlos ahora. La app es accesible en tu red local.
   On first launch Syncthing will ask for a GUI username and password.
   Set them now. The app is accessible on your local network.

4. Conecta un disco externo o USB al equipo donde corre Umbrel.
   Connect an external drive or USB to the machine running Umbrel.

5. En Syncthing: Add Folder → ruta /external/<nombre-disco>
   In Syncthing: Add Folder → path /external/<drive-name>

6. Añade el dispositivo remoto (portátil, móvil, router…) con su Device ID.
   Add the remote device (laptop, phone, router…) using its Device ID.

7. Recomendado para exportar datos: tipo de carpeta "Send Only".
   Recommended for outbound-only folders: folder type "Send Only".
```

## Integración con router 4G + tarjeta SD / 4G router + SD card pairing

El router es otro nodo Syncthing estándar:

The router is just another standard Syncthing node:

```
1. Instala Syncthing en el router (OpenWRT, GL.iNet) o en un dispositivo
   conectado a él (Raspberry Pi, etc.).
   Install Syncthing on the router (OpenWRT, GL.iNet) or a device attached
   to it (Raspberry Pi, etc.).

2. Obtén el Device ID de esa instancia de Syncthing.
   Get the Device ID from that Syncthing instance.

3. En Refugio Sync → Add Remote Device → pega el Device ID.
   In Refugio Sync → Add Remote Device → paste the Device ID.

4. Comparte la carpeta /external/<disco> con ese dispositivo.
   Share the /external/<drive> folder with that device.

5. Acepta la sincronización en el lado del router.
   Accept the sync on the router side.
```

Syncthing gestiona el NAT traversal y relay automáticamente. Funciona sobre 4G
sin configuración extra de red.

Syncthing handles NAT traversal and relay automatically. Works over 4G with no
extra network configuration.

## Puertos P2P / P2P ports

Opcionalmente, abre estos puertos en tu router para sync directo más rápido
sin depender de los servidores relay de Syncthing:

Optionally forward these ports on your router for faster direct sync without
relying on Syncthing relay servers:

| Puerto / Port | Protocolo / Protocol | Uso / Purpose              |
|---------------|----------------------|----------------------------|
| 22000         | TCP                  | Protocolo de sync          |
| 22000         | UDP                  | QUIC transport             |
| 21027         | UDP                  | Descubrimiento local / LAN |

## Notas de seguridad / Safety notes

- Usa **Send Only** en carpetas donde el disco externo es la fuente de verdad.
  Evita que otro dispositivo borre o sobreescriba archivos del disco.
  Use **Send Only** on folders where the external drive is the source of truth.
  Prevents remote devices from deleting or overwriting files on the drive.

- Expulsa siempre el disco desde la app Files de UmbrelOS antes de
  desconectarlo para evitar corrupción de datos.
  Always eject the drive from UmbrelOS Files before unplugging to prevent
  data corruption.

- Syncthing cifra todo el tráfico en tránsito. Los datos en reposo no están
  cifrados por Syncthing — usa un volumen cifrado aparte si lo necesitas.
  Syncthing encrypts all traffic in transit. Data at rest on the drive is not
  encrypted by Syncthing — use a separately encrypted volume if needed.

## Imagen Docker / Docker image

Refugio Sync usa la imagen oficial sin modificaciones:

Refugio Sync uses the official image without modifications:

```
syncthing/syncthing:latest
```
