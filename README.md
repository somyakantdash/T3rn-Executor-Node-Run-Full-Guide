# T3rn-Executor-Node-Run-Full-Guide

## Need Some Requirements for PC Users

1. For Windows Install WSL - https://learn.microsoft.com/en-us/windows/wsl/install#install-wsl-command

2. For Windows Install Ubuntu after Installing WSL - https://apps.microsoft.com/detail/9PDXGNCFSCZV?hl=en-us&gl=IN&ocid=pdpshare

3. For macOS If you have Installed Homebrew (https://brew.sh/) to manage packages on OS X,
run this command to install Git.
```
brew install git
```

## Participate as an Executor

Faucet: https://faucet.brn.t3rn.io/

Bridge: https://bridge.t1rn.io

1️⃣ Dependencies for WINDOWS & LINUX & VPS
```
sudo apt update
sudo apt upgrade -y
```

For VPS Only
```
apt install screen -y
```

2️⃣ Download Some Files & Extract
```
LATEST_VERSION=$(curl -s https://api.github.com/repos/t3rn/executor-release/releases/latest | grep 'tag_name' | cut -d\" -f4)
EXECUTOR_URL="https://github.com/t3rn/executor-release/releases/download/${LATEST_VERSION}/executor-linux-${LATEST_VERSION}.tar.gz"
curl -L -o executor-linux-${LATEST_VERSION}.tar.gz $EXECUTOR_URL
```
```
tar -xzvf executor-linux-${LATEST_VERSION}.tar.gz
rm -rf executor-linux-${LATEST_VERSION}.tar.gz
```
```
cd executor/executor/bin
```

For VPS Only
```
screen -S t3rn
```

3️⃣ Set Your Node Environment
```
export NODE_ENV=testnet
```

4️⃣ Set Your Log Settings
```
export LOG_LEVEL=debug
export LOG_PRETTY=false
export EXECUTOR_PROCESS_ORDERS=true
export EXECUTOR_PROCESS_CLAIMS=true
export EXECUTOR_MAX_L3_GAS_PRICE=50
export EXECUTOR_PROCESS_PENDING_ORDERS_FROM_API=false
```

5️⃣ Set Your Private Key [Replace ur (replace-your-privatekey) with ur actual Metamask Wallet Private Key]
```
export PRIVATE_KEY_LOCAL=replace-your-privatekey
```

6️⃣ Set Your Networks
```
export ENABLED_NETWORKS='arbitrum-sepolia,base-sepolia,optimism-sepolia,l1rn'
```

7️⃣ Start Node
```
./executor
```

For VPS Only
```
PRESS CTRL+A+D (to run ur miner continuously)
```

Take a screenshot of ur running node and post it on discord to get a Executor Role

Discord: https://discord.com/invite/9AeZdDuS

For VPS Only (to check ur node again)
```
screen -r t3rn
```
PRESS CTRL+A+D

## 🔶For Next Day Run This Command (Windows)

#1 Open WSL and Put this Command 
```
cd executor/executor/bin
```
```
export NODE_ENV=testnet
```
```
export LOG_LEVEL=debug
export LOG_PRETTY=false
export EXECUTOR_PROCESS_ORDERS=true
export EXECUTOR_PROCESS_CLAIMS=true
export EXECUTOR_MAX_L3_GAS_PRICE=50
export EXECUTOR_PROCESS_PENDING_ORDERS_FROM_API=false
```
```
export PRIVATE_KEY_LOCAL=replace-your-privatekey
```

Replace ur (replace-your-privatekey) with ur actual Metamask Wallet Private Key

```
export ENABLED_NETWORKS='arbitrum-sepolia,base-sepolia,optimism-sepolia,l1rn'
```
```
./executor
```




