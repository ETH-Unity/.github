# ETH-Unity

**ETH-Unity** is a project that bridges Ethereum blockchain functionality with Unity-based multiplayer experiences. It enables decentralized interactions between users and simulated IoT devices in real-time multiplayer environments.

## 🚀 Overview

ETH-Unity is composed of two main repositories:

- [**ETH-WEB**](https://github.com/ETH-Unity/ETH-WEB): A Unity WebGL project that demonstrates multiplayer interactions powered by Ethereum smart contracts. It supports wallet connections, Ether transactions, and blockchain-driven gameplay mechanics in a client-server architecture using Unity Netcode for GameObjects.

- [**EthNetwork**](https://github.com/ETH-Unity/EthNetwork): The blockchain infrastructure powering ETH-WEB. It includes a local GoQuorum Ethereum testnet, along with smart contracts designed for user-to-user and user-to-IoT device interactions.

Together, these repositories create a seamless environment where blockchain logic enhances real-time multiplayer gameplay.

---

## 🎮 Use Cases

- **In-Game Asset Transfers**  
  Enable secure, on-chain message, document, currency or NFT transfers between players.

- **Access Control via Smart Contracts**  
  Control in-game or physical space access (e.g., doors, rooms, sensors) based on wallet ownership or contract conditions.

- **IoT Device Simulation**  
  Demonstrate blockchain-controlled IoT devices (like smart doors or lights) within a multiplayer game world.

---

## 🔁 System Architecture

<img src="https://github.com/ETH-Unity/.github/blob/1fc4a72141f8124512eef9966340ba0f488401fd/dataflow.png" height="400" alt="Data Flow Diagram">

### 1. Game Initialization
- A user opens the WebGL game in their browser.
- The game assets (e.g., `.data`, `.wasm`, `.js`) are fetched from a static HTTP server.

### 2. Multiplayer Connectivity
- The WebGL client connects to a Unity-hosted multiplayer server via WebSockets.
- Unity Netcode synchronizes player actions and state across all connected clients.

### 3. Blockchain Integration
- The WebGL client (or Unity server) sends JSON-RPC requests to the Ethereum node via the provided RPC endpoint.
- Example calls: `eth_blockNumber`, `eth_getBalance`, or smart contract methods.

### 4. Response Handling
- Blockchain responses are processed directly by the WebGL client or routed through the Unity server for game logic synchronization.

---

## 📦 Repositories

| Repository | Description |
|------------|-------------|
| [**ETH-WEB**](https://github.com/ETH-Unity/ETH-WEB) | Unity WebGL project demonstrating Ethereum integration in a multiplayer environment. |
| [**EthNetwork**](https://github.com/ETH-Unity/EthNetwork) | Blockchain backend with GoQuorum testnet and custom smart contracts for user/device interactions. |

---

## 🛠️ Contributing

We welcome contributions from anyone! Whether you're a developer, designer, tester, or just interested in experimenting with Ethereum + Unity, you're encouraged to open issues, suggest features, or submit pull requests.

## 📄 License

All projects are under the MIT License.

