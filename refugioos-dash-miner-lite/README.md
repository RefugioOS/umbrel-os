# Dash Miner Lite (Beta) — RefugioOS

Gestiona tu granja de mineros ASIC desde tu LAN: escaner de red con bridge
integrado, gestion de equipos, calculadora de rentabilidad y directorio de
pools — sin nube, sin cuentas externas.

**BETA (0.1.0-beta.1)** — primera version publica, en pruebas.

- Bridge integrado: detecta y controla mineros Bitmain, MicroBT/WhatsMiner,
  Canaan/Avalon, Goldshell, IceRiver, Jasminer, Bitdeer y home-lab
  (Nerdminer/Nerdaxe) en tu red local.
- Stateless: los datos viven en el navegador; el contenedor no guarda estado.
- `network_mode: host` necesario para que el bridge descubra la LAN real.

Imagen: `ghcr.io/refugioos/dash-miner-lite:0.1.0-beta.1` (amd64 + arm64).
Codigo cerrado (ver NOTICE en la web oficial). Uso de la imagen libre y gratuito.