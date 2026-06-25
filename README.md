# RefugioOS UmbrelOS Community App Store

Repositorio publicable para UmbrelOS.

URL futura:

```text
https://github.com/RefugioOS/umbrel-os
```

El usuario agregara esa URL en:

```text
UmbrelOS -> App Store -> Community App Stores
```

## Estructura

Umbrel espera el manifiesto del store en la raiz y una carpeta por app:

```text
umbrel-app-store.yml
refugioos-burn-after-reading/
  umbrel-app.yml
  docker-compose.yml
  icon.png
  README.md
```

## Reglas

- Cada app debe usar un `id` prefijado con `refugioos-`.
- Cada app debe tener `umbrel-app.yml`.
- Cada app debe tener `docker-compose.yml`.
- No usar `build:` en apps publicas.
- Usar imagenes Docker publicas y versionadas.
- No meter codigo fuente en este repo.
