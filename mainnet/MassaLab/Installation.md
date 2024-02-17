### Install Dependencies
```
sudo apt update
sudo apt upgrade
```
### Install  Binary
```
wget https://github.com/massalabs/massa/releases/download/MAIN.2.1/massa_MAIN.2.1_release_linux.tar.gz
tar -xvf massa_MAIN.2.1_release_linux.tar.gz
cd massa-node
```
### Node Configuration
```
nano config/config.toml
```
### Open Port
```
sudo ufw allow 31244
sudo ufw allow 31245
```
### Start Massa Node
```
./massa-node start
```
### Check Node Status:
```
./massa-node status
```
### Configuring Massa Client
```
nano massa-client/config/config.toml
```
### Generate a Key Pair
```
./massa-client generate-keypair
```
### Buy Rolls
```
./massa-client buy-rolls --amount <amount> --payment <payment_address> --staking <staking_key_file>
```
### List Owned Rolls:
```
./massa-client list-rolls
```
### Sell Rolls
```
./massa-client sell-rolls --amount <amount> --payment <payment_address> --staking <staking_key_file>
```
