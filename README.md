# Node-Guild
```
sudo apt install curl tar wget clang pkg-config libssl-dev jq build-essential git make lz4 unzip ncdu -y
```

Step 1: Clone the Allora Chain Repository
```
git clone https://github.com/allora-network/allora-chain.git
```
Step 2: Run the Node with Docker Compose
```
cd allora-chain
docker compose pull
docker compose up -d
```

Monitoring Logs
```
docker compose logs -f
```
Executing RPC Calls
```
curl -s http://localhost:26657/status | jq .
```
Check Sync Node, Return false is complete
```
curl -so- http\://localhost:26657/status | jq .result.sync_info.catching_up
```

