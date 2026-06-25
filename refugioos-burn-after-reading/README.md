# Burn After Reading For UmbrelOS

Port/Fork de [Start9Labs/burn-after-reading](https://github.com/Start9Labs/burn-after-reading)
para el Community App Store de RefugioOS.

```text
Store ID: refugioos
App ID: refugioos-burn-after-reading
Target: UmbrelOS
Tipo: Port/Fork
Origen: Start9Labs/burn-after-reading
```

## Notas

- Usa `ghcr.io/refugioos/burn-after-reading:0.1.6-refugioos.1`.
- No incluye la integracion Tor/onion propia de StartOS.
- Requiere `APP_PASSWORD` antes del primer arranque.
- El password se guarda en `/data/start9/config.yaml` durante el primer inicio.
