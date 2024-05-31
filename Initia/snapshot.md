## Sumber : https://wiki.f5nodes.com/initia/sync/snapshot

## Cara download snapshot lebih cepat



```shell
#Install Screen
sudo apt-get update && sudo apt-get upgrade -y
sudo apt install screen
```

```shell
screen -S snapshot.sh
```
```
sudo nano snapshot.sh
```

Paste Ini
```
#!/bin/bash

# Install aria2 if not already installed
sudo apt-get update
sudo apt-get install -y aria2

# Make a backup of the current priv_validator_state.json
cp $HOME/.initia/data/priv_validator_state.json $HOME/.initia/priv_validator_state.json.backup

# Define the snapshot URL
snapshot_url="https://initia-testnet-snapshots.f5nodes.com/initiation-1_529331.tar.lz4"

# Download the snapshot using aria2
aria2c -x 16 -s 16 -k 1M -d $HOME/ -o initiation-1_529331.tar.lz4 $snapshot_url

# Extract the snapshot
tar -Ilz4 -xf $HOME/initiation-1_529331.tar.lz4 -C $HOME/

# Stop the Initia service
sudo systemctl stop initiad

# reset your node and move a snapshot
rm -rf $HOME/.initia/data
mv home/node_initia_snapshots/.initia/data $HOME/.initia/

# replace the priv_validator_state.json you have backed up
mv $HOME/.initia/priv_validator_state.json.backup $HOME/.initia/data/priv_validator_state.json 

# Restart the Initia service and check the logs
sudo systemctl restart initiad
```

```
chmod +x snapshot.sh
```

```
./snapshot.sh
```

Tunggu sampai selesai atau boleh keluar screen `CTRL + A D`


