# SeedForge para UmbrelOS / SeedForge for UmbrelOS

App propia de RefugioOS empaquetada para UmbrelOS Community App Store.

First-party RefugioOS app packaged for the UmbrelOS Community App Store.

## Publicación / Publishing

Antes de publicar este repo, la imagen debe existir:

```text
ghcr.io/refugioos/seedforge:0.1.1-refugioos.1
```

SeedForge usa `admin` como usuario inicial y `refugioos` como contraseña
inicial. Umbrel genera `APP_SEED`, que SeedForge usa como secreto de sesión y
clave de datos.

SeedForge uses `admin` as the initial user and `refugioos` as the initial
password. Umbrel generates `APP_SEED`, which SeedForge uses as the session
secret and data key.

## Credenciales / Credentials

```text
Usuario / User: admin
Contraseña / Password: refugioos
```

## Conectividad / Connectivity

SeedForge permite configurar:

- APIs externas: Blockstream para BTC y Etherscan para ETH.
- API keys externas por red BTC/ETH.
- Nodos o APIs propias: BTC Core RPC local, BTC API Esplora y ETH JSON-RPC.
- Prioridad por fuente para probar primero tu nodo local y después respaldos.

SeedForge can configure external APIs, BTC/ETH API keys, custom BTC/ETH nodes or
APIs, and source priority.

## Uso previsto / Intended Use

SeedForge es una herramienta sensible para recuperación de wallets propias. No
la expongas públicamente y revisa credenciales antes de introducir datos reales.

SeedForge is a sensitive tool for recovering your own wallets. Do not expose it
publicly, and review credentials before entering real data.
