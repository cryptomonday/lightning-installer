# Google Cloud MEAN stack (Bitnami) LND instalation

This script is tested on Ubuntu 16.04 LTS

## Getting Started

This is a full installer! It will install full bitcoin node, a lightning node and lightning-charge which is a lightning API.

### Prerequisites

Freshly deployed Ubuntu 16.04 LTS, with port 9735 open.

## Instalation

Simply follow these steps

First step

```
Edit the values in config file (This is for your Lightning Node)
DO NOT USE TILDA (~) FOR YOUR HOME PATH, BUT THE WHOLE PATH!
```

Second step

```
Install by running ./install.sh
```

#### Now wait for about 12+ hours for bitcoin node to fully sync.

To check bitcoin node syncing progress use

```
tail -f ~/.bitcoin/debug.log
```

After bitcoin node is fully synced use this command to start your lightning node and lightning charge

```
immortal lightningd
immortal charged --api-token mySecretToken --db-path ~/chargedb/charge.db
```
