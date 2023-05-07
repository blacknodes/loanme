# Demo


## Step 1: Install the Celestia Lite node

First, run the `celestia lite node` go to the offical docs:

```
https://docs.celestia.org/nodes/light-node/
```

Command to Run Celestia Lite Node:
```
cd $HOME 
rm -rf celestia-node 
git clone https://github.com/celestiaorg/celestia-node.git 
cd celestia-node/ 
git checkout tags/v0.9.2 
make build 
make install 
make cel-key 
```

Initialize the light node:
```
celestia light init --p2p.network blockspacerace
```

Create your key for your node:
```
./cel-key add  my_key    --keyring-backend test --node.type light --p2p.network blockspacerace
```

Start your light node with the key created:
```
celestia light start --core.ip https://rpc-blockspacerace.pops.one:9090 --keyring.accname my_key --gateway --gateway.addr 127.0.0.1 --gateway.port 26659 --p2p.network blockspacerace
```

## Step 2: Clone and Start
Clone the repo: 
```
git clone https://github.com/subhamgurjar/loanme.git
```

Start the LoanMe Rollup:
```
cd loanme
bash init-chain.sh
```



