# RefugioOS for UmbrelOS

Community App Store de RefugioOS para UmbrelOS.

URL para agregar en UmbrelOS:

```text
https://github.com/RefugioOS/umbrel-os
```

En UmbrelOS, abre:

```text
UmbrelOS -> App Store -> Community App Stores
```

Y agrega la URL del repo.

## Apps

```text
refugioos-seedforge
refugioos-burn-after-reading
```

## Estructura Del Repo

```text
umbrel-app-store.yml
refugioos-seedforge/
  umbrel-app.yml
  docker-compose.yml
  icon.png
  README.md
refugioos-burn-after-reading/
  umbrel-app.yml
  docker-compose.yml
  icon.png
  README.md
```

## Notas

Este repositorio solo contiene las recetas de instalacion para UmbrelOS:
manifiestos, `docker-compose.yml`, iconos y documentacion minima.

El codigo fuente de las apps no se publica aqui. Las apps usan imagenes Docker
publicas y versionadas bajo `ghcr.io/refugioos/...`.

Cada app usa el prefijo `refugioos-`, que coincide con el `id` del store en
`umbrel-app-store.yml`.
