# SeedForge para UmbrelOS

App propia de RefuigoOS empaquetada para UmbrelOS Community App Store.

## Publicacion

Antes de publicar este repo, la imagen debe existir:

```text
ghcr.io/refuigoos/seedforge:0.1.1-refuigo.1
```

Umbrel genera `APP_PASSWORD` y `APP_SEED`. SeedForge los usa como contrasena inicial, secreto de sesion y clave de datos.

## Conectividad

SeedForge permite configurar:

- APIs externas: Blockstream para BTC y Etherscan para ETH.
- API keys externas por red BTC/ETH.
- Nodos o APIs propias: BTC Core RPC local, BTC API Esplora y ETH JSON-RPC.
- Prioridad por fuente para probar primero tu nodo local y despues respaldos.

## Uso previsto

SeedForge es una herramienta sensible para recuperacion de wallets propias. No la expongas publicamente y revisa credenciales antes de introducir datos reales.
