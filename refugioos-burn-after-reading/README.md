# Burn After Reading for UmbrelOS

Port/Fork no oficial de
[Start9Labs/burn-after-reading](https://github.com/Start9Labs/burn-after-reading)
para el Community App Store de RefugioOS en UmbrelOS.

Unofficial RefugioOS port/fork of Start9Labs Burn After Reading for the UmbrelOS
Community App Store.

```text
Store ID: refugioos
App ID: refugioos-burn-after-reading
Target: UmbrelOS
Tipo: Port/Fork
Origen: Start9Labs/burn-after-reading
Licencia upstream: GPL-3.0
```

## Notas

- Usa `ghcr.io/refugioos/burn-after-reading:0.1.6-refugioos.1`.
- El proyecto original pertenece a Start9Labs; RefugioOS solo mantiene este
  empaquetado/port para UmbrelOS.
- No incluye la integración Tor/onion propia de StartOS.
- User / Usuario: `admin`.
- Password / Contraseña: `refugioos`.
- El password se guarda en `/data/start9/config.yaml` durante el primer inicio.
- El contenido se quema cuando el lector pulsa `View` en la interfaz web. Una
  petición directa `GET /api/data/<hash>` solo descarga el contenido; la
  interfaz llama después a `DELETE /api/data/<hash>`.
- El proxy de autenticación de Umbrel está desactivado para que los enlaces
  efímeros puedan abrirse desde fuera de la sesión de Umbrel.
- La licencia upstream se incluye en `LICENSE.upstream-GPL-3.0.txt`.

## Notes

- Uses `ghcr.io/refugioos/burn-after-reading:0.1.6-refugioos.1`.
- The original project belongs to Start9Labs; RefugioOS maintains only this
  UmbrelOS package/port.
- It does not include the native StartOS Tor/onion integration.
- User: `admin`.
- Password: `refugioos`.
- Content is burned when the reader presses `View` in the web interface. A raw
  `GET /api/data/<hash>` only downloads the content; the interface then calls
  `DELETE /api/data/<hash>`.
- Umbrel proxy authentication is disabled so ephemeral links can be opened
  outside the Umbrel session.
