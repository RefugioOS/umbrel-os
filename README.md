# RefugioOS for UmbrelOS

Community App Store de RefugioOS para UmbrelOS.

RefugioOS Community App Store for UmbrelOS.

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

## Estructura Del Repo / Repository Structure

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

## Notas / Notes

Este repositorio solo contiene las recetas de instalación para UmbrelOS:
manifiestos, `docker-compose.yml`, iconos y documentación mínima.

El código fuente de las apps no se publica aquí. Las apps usan imágenes Docker
públicas y versionadas bajo `ghcr.io/refugioos/...`.

Cada app usa el prefijo `refugioos-`, que coincide con el `id` del store en
`umbrel-app-store.yml`.

This repository contains only UmbrelOS installation recipes: manifests,
`docker-compose.yml`, icons, and minimal documentation. App source code is not
published here; apps use public, versioned Docker images under
`ghcr.io/refugioos/...`.
