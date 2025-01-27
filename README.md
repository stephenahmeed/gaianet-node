# Gaianet Node (Docker)

Easily run a Gaianet Node using Docker. This guide walks you through the setup and usage process. 

## Requirements
- **Minimum RAM:** 16 GB (works on 8 GB but not recommended).
- **System:** VPS or Local Ubuntu system.
- **Supported OS:** Ubuntu 22.04 or Ubuntu 24.04.

## Recommendations
- Run the node only when chatting with the bot.
- Use a local system (e.g., WSL on Windows or Ubuntu on PC) if you don't want to keep a VPS active 24/7.
- You can purchase VPS services from [PQ Hosting](https://pq.hosting/) using cryptocurrency or [Contabo](https://contabo.com/en/) using card.

---

## Installation Steps

### 1. Install and Run Gaianet Docker Image

```bash
curl -sSfL 'https://github.com/GaiaNet-AI/gaianet-node/releases/latest/download/install.sh' | bash

```
Added Path Now

```bash
source /root/.bashrc
```

### 2. Run Model

```bash
gaianet init --config https://raw.githubusercontent.com/GaiaNet-AI/node-configs/main/qwen2-0.5b-instruct/config.json
```

Start The Node 

```bash
gaianet start
```

### 3. Get Node Info
Run the following command to retrieve your **Node ID** and **Device ID**:

```bash
gaianet info
```

Copy the **Node ID** and **Device ID**, then type `exit` to detach from the container.

### 4. Connect Node to Gaianet
1. Visit the [Gaianet site](https://www.gaianet.ai/setting/nodes) and connect your wallet.
2. Click on **Connect New Node** and enter your **Node ID** and **Device ID**.
3. Click **Join**.
4. Customize the following URL with your **Node ID**, and visit it to start chatting with the bot:
   ```
   https://YOUR_NODE_ID.us.gaianet.network
   ```

### 5. Back Up `nodeid.json` (Important)
Use the command below to back up your `nodeid.json` file. Store it securely.

```bash
docker exec -it gaianet cat /root/gaianet/nodeid.json
```

---

## Commands Overview

### Start Node
```bash
sudo docker restart gaianet
```

### Stop Node
```bash
sudo docker stop gaianet
```

### Check Node Info
```bash
docker exec -it gaianet /root/gaianet/bin/gaianet info
```

---

## FAQ

### 1. Should I run the node 24/7?
No. You only need to run the node while chatting with the bot. Throughput increases with interaction, not runtime.

### 2. Is it better to use a local system instead of a VPS?
Yes, if you're not using the bot 24/7, running it locally is more cost-efficient.

### 3. How do I stop the node?
Use:
```bash
sudo docker stop gaianet
```

### 4. How do I restart the node?
Use:
```bash
sudo docker restart gaianet
```

---

## Earn More Points
Chat more with the bot to increase throughput and earn more Gaianet points!
