## Cara Monitoring Block

```shell
#Install Screen
sudo apt-get update && sudo apt-get upgrade -y
sudo apt install screen
```

```shell
screen -S logs.sh
```
```
sudo nano logs.sh
```
>Paste ini
```
#!/bin/bash

while true
do
    local_height=$(initiad status | jq -r .sync_info.latest_block_height)
    network_height=$(curl -s https://rpc-initia-testnet.trusted-point.com/status | jq -r .result.sync_info.latest_block_height)
    blocks_left=$((network_height - local_height))
    current_date=$(date "+%Y-%m-%d %H:%M:%S")
    n_peers=$(curl -s localhost:26657/net_info | jq .result.n_peers)
    
    echo "======================================================="
    echo "Current date and time: $current_date"
    echo "======================================================="
    echo "Node Running Right Now : $local_height"
    echo "Block from Initia Network Latest : $network_height"
    echo "Block Need to be Catch Up : $blocks_left"
    echo "Peers Active : $n_peers"
    echo "======================================================="
    sleep 10
done
```

```
chmod +x logs.sh
```

>Jalankan program
```
./logs.sh
```
>Close screen `CTRL + A D`

Untuk Cek Lagi
```
screen -R logs
```

