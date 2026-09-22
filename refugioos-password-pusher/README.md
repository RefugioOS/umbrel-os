# Password Pusher — tienda UmbrelOS (RefugioOS)

App del Community App Store de RefugioOS para umbrelOS.

- Imagen: `ghcr.io/refugioos/password-pusher:2.14.0-refugioos.1`
- Web: puerto 3481 (proxy interno 5100)
- Datos: `${APP_DATA_DIR}/data` -> `/opt/PasswordPusher/storage`

Ficha y port: `password-pusher-umbrel/` en el workspace. Update:
`update-pusher.py`. Publicacion: `deploy-port.py` + `publicar-app.py --app password-pusher`.