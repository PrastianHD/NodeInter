# Manual Installation
The CARV test verifier is currently operational on the opBNB testnet. We are offering a free, claimable NFT license key to anyone interested in joining the testnet to explore and test the verifier nodes before the mainnet launch. 

# Prerequisites
## Create a Wallet
- Create a Metamask Wallet
- Get Testnet Fund - BNB Testnet https://www.bnbchain.org/en/testnet-faucet
- Bridge from BNB Testnet to opBNB Testnet https://opbnb-testnet-bridge.bnbchain.org/deposit
## Get testnet node license
- To become eligible as a verifier on the testnet, you must first claim a testnet license. Please visit https://testnet-explorer.carv.io/verifiers, connect your wallet, and then click on "Claim Testnet License" located in the top right corner of the page. Follow the instructions provided to complete the claim process.
## Hardware Requirements
- Fast CPU with 2+ cores
- 4GB+ RAM
- 8+ MBit/sec download Internet service

# Running a Verifier Node

## Step 1: Install Go
Verifier requires Go (version 1.21 or later). You can install Go using your preferred package manager. For example, on Ubuntu, you can install Go by running:
```shell
sudo apt update && sudo apt upgrade -y
sudo rm -rf /usr/local/go
curl -Ls https://go.dev/dl/go1.21.1.linux-amd64.tar.gz | sudo tar -xzf - -C /usr/local
eval $(echo 'export PATH=$PATH:/usr/local/go/bin' | sudo tee /etc/profile.d/golang.sh)
eval $(echo 'export PATH=$PATH:$HOME/go/bin' | tee -a $HOME/.profile)
```
Verify the installation:
```
go version
```

## Step 2: Clone the Source Code
Open your terminal and run the following command to clone the verifier repository:
```
git clone https://github.com/carv-protocol/verifier
```
Navigate to the Cloned Directory:
```
cd verifier
```
Build the Verifier:
```
make build
```
This will download and compile dependencies to $GOPATH/bin. Ensure this path is added to your environment variable:
```
export PATH=$PATH:$GOPATH/bin
```

## Step 3: Configure Private Key
If this is your first time running the verifier, you need to specify a private key. The private key will sign the verification transaction, and the corresponding address will receive CARV rewards.

Configure the plain text private key: Set `wallet.mode` in the configuration file to 1, and write the plain text private key into `wallet.private_key`. 
```
nano verifier/configs/config.yaml
```
Edit

> 
>  mode: 1
> 
> private_key: "your private key" without 0x
>

## Step 4: Run Verifier Node
Install Screen:
```
sudo apt install screen
```
Create New Screen:
```
screen -S verifier
```
Navigate to the Bin Directory:
```
cd verifier/bin/
```
Then run:
```
./verifier -conf ../configs/config.yaml -private-key <Your Private Key>
```
Example:
> ./verifier -conf ../configs/config.yaml -private-key 0x1234243532525235

Close a screen `CTRL + A D`

## Monitoring
After running the node verifier, you can monitor or check the Testnet veCARV rewards you have received.
- Navigate to https://testnet-explorer.carv.io/verifiers
- Delegate Your Own License to Your Address according to the private key
- How to check screen logs
  ```
  screen -R verifier
  ```