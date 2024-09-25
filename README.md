# Sol Bundle Bot

## Project Overview

**Sol Bundle Bot** is a TypeScript-based project designed to interact with the Solana blockchain for advanced DeFi operations. The project includes a variety of scripts to manage liquidity pools, execute trading strategies, and provide utility functions for interacting with decentralized exchanges (DEXs) such as Raydium and Serum. The main focus is on automating liquidity management, executing buy and sell orders, and utilizing lookup tables for efficient blockchain interactions.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Project Structure](#project-structure)
- [Configuration](#configuration)
- [Dependencies](#dependencies)

## Features

- **Automated Trading**: Execute trades on Solana DEXs with efficiency.
- **Liquidity Management**: Add, remove, and manage liquidity pools automatically.
- **Bundled Transactions**: Group multiple operations in a single transaction to save on fees and improve execution speed.
- **Advanced Strategies**: Utilize custom strategies for optimal trading and liquidity provision.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/sergeychernyakov/sol_bundle_bot_2.git
   cd sol_bundle_bot_2
   ```
2. Install dependencies:
   ```bash
   npm install
   ```

3. Configure your environment variables by creating a `.env` file based on the `.env.example` file.

## Usage

To start the main script, use:

```bash
npm start
```

This will execute the `jitoPool.ts` script, which is the entry point of the project.

You can also run specific scripts depending on the desired functionality:

- **Buy Tokens**: 
  ```bash
  ts-node buyToken.ts
  ```
- **Sell Tokens**: 
  ```bash
  ts-node sellFunc.ts
  ```
- **Compute Liquidity Position**: 
  ```bash
  ts-node computeLPO.ts
  ```

## Features

- **Liquidity Pool Management**: Add or remove liquidity from Raydium pools using scripts like `removeLiq.ts` and `createLUT.ts`.
- **Automated Trading**: Execute buy and sell orders on Solana-based DEXs using `buyToken.ts` and `sellFunc.ts`.
- **Lookup Table Management**: Manage and utilize address lookup tables for optimized Solana transactions with `LookupTableProvider.ts`.
- **DeFi Integration**: Integration with various DeFi protocols such as Raydium and Serum for enhanced trading and liquidity operations.
- **Key Management**: Securely generate and manage cryptographic keys using `createKeys.ts`.
- **Data Structuring**: Structs and interfaces defined in `structs.ts` and `interfaces.ts` provide a robust structure for blockchain data handling.

## Project Structure

- **config.ts**: Configuration settings and environment variables.
- **constants.ts**: Constant values used throughout the project.
- **createKeys.ts**: Script for generating and managing cryptographic keys.
- **buyToken.ts**: Script for buying tokens on the Solana blockchain.
- **sellFunc.ts**: Script for selling tokens.
- **computeLPO.ts**: Script for computing liquidity positions.
- **raydiumUtil.ts**: Utility functions for interacting with Raydium.
- **jitoPool.ts**: Main script for interacting with Jito pools.
- **createMarket.ts**: Script for creating new markets on the Solana blockchain.
- **LookupTableProvider.ts**: Manages Solana address lookup tables for optimized transaction handling.
- **keyInfo.json**: Contains key information and wallet addresses for liquidity management.
- **tsconfig.json**: TypeScript configuration file.
- **package.json**: Project dependencies and scripts.

## Configuration

The project configuration is managed through the `config.ts` file and environment variables. Make sure to set the following environment variables in your `.env` file:

- `SOLANA_NETWORK`: The Solana network to connect to (e.g., `mainnet`, `testnet`).
- `PRIVATE_KEY`: Your private key for signing transactions.
- `RPC_ENDPOINT`: Solana RPC endpoint for network connections.
- Other variables as needed for your specific use case.

### Example `.env` file:
```
SOLANA_NETWORK=mainnet
PRIVATE_KEY=your_private_key_here
RPC_ENDPOINT=https://api.mainnet-beta.solana.com
```

## Dependencies

The project relies on several key libraries and frameworks:

- **@solana/web3.js**: For interacting with the Solana blockchain.
- **@coral-xyz/anchor**: Solana smart contract framework.
- **@project-serum/serum**: Decentralized exchange protocol on Solana.
- **@raydium-io/raydium-sdk**: Raydium SDK for interacting with Raydium pools.
- **jito-ts**: For interacting with Jito-specific features.
- And various other utility libraries like `axios`, `dotenv`, and `typescript`.

For a full list of dependencies, see the `package.json` file.
