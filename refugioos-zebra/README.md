# Zebra (Zcash Node) — RefugioOS para UmbrelOS

<!-- PORT-VERSION-BEGIN -->
Version: `6.3.0-refugioos.1` - upstream `v6.3.0` (commit `f5c5277fe41eba9c74f37098738f93f35dd70d60`)
<!-- PORT-VERSION-END -->

Port puro del nodo Zcash [Zebra (zebrad)](https://github.com/ZcashFoundation/zebra)
de la Zcash Foundation para UmbrelOS.

- Imagen versionada: `ghcr.io/refugioos/zebra:6.3.0-refugioos.1` (amd64 + arm64).
- Binarios oficiales verificados por SHA256 (sin forks ni parches).
- Puertos: **8233** P2P Mainnet, **8232** RPC JSON (cookie auth en
  `/data/.cookie`), **8080** health `/healthy` y `/ready`.
- Requisitos: ~300 GB de disco libre, 4 GB de RAM minimo (16 GB recomendado).

La app no tiene interfaz grafica: al abrirla desde Umbrel veras el estado del
nodo (`/healthy`). Conectate al RPC desde otra maquina con
`cat /data/.cookie` (usuario `__cookie__`).

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

- Versioned image: `ghcr.io/refugioos/zebra:6.3.0-refugioos.1` (amd64 + arm64).
- Official SHA256-verified binaries (no forks or patches).
- Ports: **8233** P2P Mainnet, **8232** JSON-RPC (cookie auth in
  `/data/.cookie`), **8080** health `/healthy` and `/ready`.
- Requirements: ~300 GB free disk, 4 GB RAM minimum (16 GB recommended).

No GUI: opening the app from Umbrel shows the node status (`/healthy`). Use
the RPC from another machine with `cat /data/.cookie` (user `__cookie__`).