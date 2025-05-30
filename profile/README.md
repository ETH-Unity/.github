# ETH-Unity

ETH-Unity develops tools that integrate Ethereum blockchain functionality into Unity-based multiplayer environments.

## Projects

-   **UnityNethereum**  
    A Unity project combining multiplayer interactions (via Unity's Netcode for GameObjects) with Ethereum integration. It enables in-game wallet connections, Ether transactions, and smart contract interactions.
    
-   **EthNetwork**  
    Provides the blockchain backend for UnityNethereum, including a local GoQuorum testnet and smart contracts for user-to-user and user-to-device interactions.
    

## Use Cases

-   In-game asset transfers using Ethereum.
    
-   Access control for digital or physical spaces via smart contracts.
    
-   Simulated IoT interactions (e.g., doors, sensors) within multiplayer environments.

## Data Flow

The following illustrates the core data flow between the components in a typical ETH-Unity WebGL environment integrated with blockchain and multiplayer support:

**Game Initialization**  
   - The user opens the WebGL game in their browser.
   - The Unity WebGL client makes an `HTTP GET` request to fetch assets (e.g., `/Build/Build.data`) from the client-side HTTP server.
   - The server responds with the required game files, and the Unity game loads in the browser.

**Multiplayer Connectivity**  
   - The WebGL client establishes a WebSocket connection to the Unity multiplayer server.
   - Real-time multiplayer synchronization is maintained over this WebSocket connection.

**Blockchain Integration**  
   - The Unity WebGL client may make JSON-RPC HTTP requests directly to an Ethereum node via the blockchain RPC endpoint (e.g., `eth_blockNumber`, `eth_getBalance`) to retrieve on-chain data.
   - Optionally, the Unity server can also perform JSON-RPC requests to the blockchain if server-side blockchain logic is needed.

**Responses and Sync**  
   - The Ethereum node returns JSON-RPC responses, which are processed either directly by the WebGL client or relayed via the Unity server.

This hybrid architecture enables seamless interaction between decentralized blockchain logic and real-time multiplayer gameplay in a browser-native Unity environment.


## 📄 License

All projects are under the MIT License.

## 🔗 Repositories

-   [UnityNethereum](https://github.com/ETH-Unity/UnityNethereum)
    
-   [EthNetwork](https://github.com/ETH-Unity/EthNetwork)
