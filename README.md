# 🦥🦥🦥🦥 Celestia-lite-node 🦥🦥🦥🦥

#System Requirements

CPU | 2+ | 
--- | --- |
RAM | 4+ GB |
Storage | 20 GB SSD |
Operting System | Ubuntu 22	 |

## Node Setup

### 🦥 Update system

```
sudo apt update && sudo apt upgrade -y
```

 ## 🦥 Screen Installtion
```shell
sudo apt install screen
```

 ## 🦥 Docker Installation and verify
```shell
sudo apt-get install docker-ce docker-ce-cli http://containerd.io
sudo docker run hello-world
```

 ## 🦥 Create Celestia screen
```shell
screen -S celestia
```

 ## 🦥 Light Node Setup Commnads (run one after another)
```shell
export NETWORK=celestia
export NODE_TYPE=light
export RPC_URL=http://public-celestia-consensus.numia.xyz
docker run -e NODE_TYPE=$NODE_TYPE -e P2P_NETWORK=$NETWORK \
    ghcr.io/celestiaorg/celestia-node:v0.13.7 \
    celestia $NODE_TYPE start --core.ip $RPC_URL --p2p.network $NETWORK
 ```
