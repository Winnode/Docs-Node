# Cheat Sheet

## to create a new wallet, use the following command. don’t forget to save the mnemonic

```
wardend keys add $WALLET
```

## to restore exexuting wallet, use the following command

```
wardend keys add $WALLET --recover
```

## save wallet and validator address

```
WALLET_ADDRESS=$(wardend keys show $WALLET -a)
VALOPER_ADDRESS=$(wardend keys show $WALLET --bech val -a)
echo "export WALLET_ADDRESS="$WALLET_ADDRESS >> $HOME/.bash_profile
echo "export VALOPER_ADDRESS="$VALOPER_ADDRESS >> $HOME/.bash_profile
source $HOME/.bash_profile
```

## check sync status, once your node is fully synced, the output from above will print "false"

```
wardend status 2>&1 | jq 
```

## Create validator.json file

```
echo "{\"pubkey\":{\"@type\":\"/cosmos.crypto.ed25519.PubKey\",\"key\":\"$(wardend comet show-validator | grep -Po '\"key\":\s*\"\K[^"]*')\"},
    \"amount\": \"1000000uward\",
    \"moniker\": \"test\",
    \"identity\": \"\",
    \"website\": \"\",
    \"security\": \"\",
    \"details\": \"I love blockchain ❤️\",
    \"commission-rate\": \"0.1\",
    \"commission-max-rate\": \"0.2\",
    \"commission-max-change-rate\": \"0.01\",
    \"min-self-delegation\": \"1\"
}" > validator.json
# Create a validator using the JSON configuration
wardend tx staking create-validator validator.json \
    --from $WALLET \
    --chain-id buenavista-1 \
	--gas auto --gas-adjustment 1.5 --fees 600uward \
```

## Delete node

```
sudo systemctl stop wardend
sudo systemctl disable wardend
sudo rm -rf /etc/systemd/system/wardend.service
sudo rm $(which wardend)
sudo rm -rf $HOME/.warden
sed -i "/WARDEN_/d" $HOME/.bash_profile
```
