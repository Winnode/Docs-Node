# Installation

#### Preparation

```
sudo apt update && apt upgrade -y
sudo apt install tmux git curl -y
sudo apt install make clang pkg-config libssl-dev build-essential -y
```

#### Download Binary

```
cd $HOME && rm -rf node_pactus && wget https://github.com/pactus-project/pactus/releases/download/v1.0.1/pactus-cli_1.0.1_linux_amd64.tar.gz && tar -xzf pactus-cli_1.0.1_linux_amd64.tar.gz && rm -rf pactus-cli_1.0.1_linux_amd64.tar.gz && mv pactus-cli_1.0.1 node_pactus && cd node_pactus
```

#### Download Binary

```
sudo ./pactus-daemon init
```

#### Run

```
Screen -S pactus
```

```
sudo ./pactus-daemon start
```

#### Restore Wallet

```
./pactus-daemon init --restore "<your-mnemonic>"
```

#### Wallet Seed

```
./pactus-wallet seed
```

#### List of Addresses

```
./pactus-wallet address all
```

#### Get Address Balance

```
./pactus-wallet address balance <ADDRESS>
```

#### Sending Bond

```
./pactus-wallet tx bond <Reward address> <Validator address> <AMOUNT>
```

#### Sending Transfer

```
./pactus-wallet tx transfer <sender address> <receiver address> <AMOUNT>
```
