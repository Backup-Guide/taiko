# Taiko
[DISCORD](https://discord.gg/taikoxyz)

[![dev chat](https://discordapp.com/api/guilds/984015101017346058/widget.png?style=banner2)]([https://discord.gg/taikoxyz])


## Create Dapp Sepolia
[DISINI](https://dashboard.alchemy.com/)
- Copas WSS & HTTPS

<p align="left"><img height="auto" width="auto" src="https://user-images.githubusercontent.com/98658943/227556609-c0fe2742-cc1c-4322-9a83-3de0def97a2d.png"</p>


## Install Alat dan Bahan ( Jika belum )

Docker
```
sudo apt update; sudo apt upgrade
```

```
sudo apt-get update && sudo apt install jq git && sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin && sudo apt-get install docker-compose-plugin
```

## Open Port

```
ufw allow ssh; ufw allow 30303; ufw allow 8545; ufw allow 6060; ufw allow 9000; ufw allow 9090; ufw enable
```

## Clone Repo

```
git clone https://github.com/taikoxyz/simple-taiko-node.git
cd simple-taiko-node
```

## Edit .env

```
cp .env.sample .env
```

Lalu edit
```
nano .env
```

Paste https dan wss dari Alchemy tadi kesini
<p align="left"><img height="auto" width="auto" src="https://user-images.githubusercontent.com/98658943/227559350-8362428d-3fc6-4e14-8c2d-fea6b484f2bb.png"</p>

### Optional

Bisa aktifkan `Prover` kalo spek nya mencukupi [ 8/16 core CPU dan 32GB  RAM ]. Jika spek mencukupi, silahkan aktifkan `Prover`
Ubah `false` menjadi `true` lalu paste Private Key wallet baru kalian

<p align="left"><img height="auto" width="auto" src="https://user-images.githubusercontent.com/98658943/227561715-fa7307c4-2783-4475-a5e8-3ecce9756b47.png"</p>

# RUN!

```
docker compose up -d
```

## Command lain-lain

Cek logs

```
cd ~/simple-taiko-node
docker compose logs -f
```

Cek logs `Prover` kalo di aktifin

```
cd ~/simple-taiko-node
docker compose logs -f l2_execution_engine

Cek stats

buka link ini di browser kalian, ganti `IPVPS` ke IP VPS mu
```
http://IPVPS:3000/d/L2ExecutionEngine/l2-execution-engine-overview?orgId=1&refresh=10s
```

Contoh:
http://192.168.1.1:3000/d/L2ExecutionEngine/l2-execution-engine-overview?orgId=1&refresh=10s
