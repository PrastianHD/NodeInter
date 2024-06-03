# Madara Get Started ⚡

This repository is for pushing transactions in Avail Madara-Cli, Original Repo [here](https://github.com/karnotxyz/madara-get-started).

## How to use these scripts

### Setup 

> You will need Node.js to use these scripts. These scripts were tested on Node version v20.5.1
```
sudo apt update
sudo apt install curl
```

```
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
```

```
sudo apt update
sudo apt install -y nodejs
```

```
node -v
npm -v
```

### Clone Repo
```
git clone https://github.com/PrastianHD/madara-tx
```

```
screen -S madaratx
```

```
cd madara-tx
npm i
```

### Edit Config
> nodeUrl: "http://37.60.244.91:9944" == replace it with your IP
> edit amount and delay time (optional)

### Using the scripts

1. Declaring a contract:

   ```
   node scripts/declare.js <path_to_sierra> <path_to_casm>
   ```

   For example,

   ```
   node scripts/declare.js ./contracts/OpenZeppelinAccountCairoOne.sierra.json ./contracts/OpenZeppelinAccountCairoOne.casm.json
   ```

2. Deploying a contract
   ```
   node scripts/deploy.js <path_to_sierra> <iterations> 
   ```

   For example,
   ```
   node scripts/deploy.js ./contracts/OpenZeppelinAccountCairoOne.sierra.json 10
   ```

3. Claim a faucet
   '''
   node scripts/faucet.js <path_to_sierra>
   '''

   For example,
   '''
   node scripts/faucet.js ./contracts/ERC20.json 
   '''

4. Getting a transaction receipt
   ```
   node scripts/get_transaction.js <txn_hash>
   ```
