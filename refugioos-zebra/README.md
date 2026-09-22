# Zebra (Zcash Node) — RefugioOS para UmbrelOS

<!-- PORT-VERSION-BEGIN -->
Version: `6.3.0-refugioos.2` - upstream `v6.3.0` (commit `f5c5277fe41eba9c74f37098738f93f35dd70d60`)
<!-- PORT-VERSION-END -->

Port puro del nodo Zcash [Zebra (zebrad)](https://github.com/ZcashFoundation/zebra)
de la Zcash Foundation para UmbrelOS.

- Imagen versionada: `ghcr.io/refugioos/zebra:6.3.0-refugioos.2` (amd64 + arm64).
- Binarios oficiales verificados por SHA256 (sin forks ni parches).
- Puertos: **8233** P2P Mainnet, **8232** RPC JSON (cookie auth en
  `/data/.cookie`), **8080** pagina de estado local (estado, /healthy, /ready
  y log del sync).
- Requisitos: ~300 GB de disco libre, 4 GB de RAM minimo (16 GB recomendado).
- Recursos: el contenedor limita su RAM a **4 GB** por defecto (minimo
  oficial, suficiente para un nodo de baja demanda: solo sync) y rota los
  logs (20 MB x 3), para dejar RAM libre al resto de apps. Si la pagina
  muestra reinicios por RAM, sube el tope con `ZEBRA_MEM_LIMIT=8g`. La cadena
  no se puede podar: la pagina avisa cuando quedan < 25 GB libres.

Al abrir la app desde Umbrel veras la pagina de estado del nodo: si zebrad
cae se relanza solo y el error aparece en pantalla, y durante el sync inicial
(dias) el log muestra el progreso. Conectate al RPC desde otra maquina con
`docker exec <contenedor> cat /data/.cookie` (usuario `__cookie__`).

## Actualizaciones / Updates

Ejecuta desde el repo de trabajo:

```bash
python RefugioOS-AppStore/scripts/update-port.py check
python RefugioOS-AppStore/scripts/update-port.py update --build --push
```

Regenera la imagen y este manifiesto con la release nueva de Zebra.

---

Pure port of the Zcash Foundation's [Zebra (zebrad)](https://github.com/ZcashFoundation/zebra)
Zcash node for UmbrelOS.

- Versioned image: `ghcr.io/refugioos/zebra:6.3.0-refugioos.2` (amd64 + arm64).
- Official SHA256-verified binaries (no forks or patches).
- Ports: **8233** P2P Mainnet, **8232** JSON-RPC (cookie auth in
  `/data/.cookie`), **8080** local status page (state, /healthy, /ready and
  the sync log).
- Requirements: ~300 GB free disk, 4 GB RAM minimum (16 GB recommended).

Opening the app shows the local status page; if zebrad crashes it is
restarted automatically and the error is shown on the page, and the initial
sync (days) progress is visible in the log. Use the RPC from another machine
with `docker exec <container> cat /data/.cookie` (user `__cookie__`).