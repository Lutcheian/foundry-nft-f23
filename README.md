# Foundry NFT Project

A Solidity-based NFT project built using **Foundry**, **OpenZeppelin**, and Ethereum smart contracts. This project demonstrates NFT creation, deployment, testing, and on-chain metadata management.

## Overview

This repository contains two NFT implementations:

### 1. Basic NFT
- ERC-721 standard implementation.
- Mint NFTs with custom token URIs.
- Track token ownership.
- Built using OpenZeppelin.

### 2. Mood NFT
- Dynamic NFT that represents different moods.
- Supports HAPPY and SAD moods.
- NFT owners can flip their NFT's mood.
- Uses Base64-encoded SVG images.
- Generates on-chain JSON metadata.
- Updates the NFT image when its mood changes.

## Technologies Used

| Technology | Purpose |
|---|---|
| Solidity | Smart contract development |
| Foundry | Development, testing and deployment |
| Forge | Contract compilation and testing |
| Cast | Ethereum RPC interaction |
| Anvil | Local Ethereum blockchain |
| OpenZeppelin | ERC-721 implementation |
| Base64 | Encoding NFT metadata and SVG images |
| Ethereum Sepolia | Smart contract test network |

## Project Structure

```text
foundry-nft-f23/
├── .github/
├── img/
│   ├── happy.svg
│   └── sad.svg
├── lib/
│   ├── forge-std/
│   ├── foundry-devops/
│   └── openzeppelin-contracts/
├── script/
│   ├── DeployBasicNft.s.sol
│   ├── DeployMoodNft.s.sol
│   └── Interactions.s.sol
├── src/
│   ├── BasicNft.sol
│   └── MoodNft.sol
├── test/
│   ├── unit/
│   └── intergrations/
├── foundry.toml
├── foundry.lock
├── Makefile
└── README.md
```

## Getting Started

### Prerequisites

Install the following:

- Git
- Foundry
- An Ethereum wallet for testnet deployment

### Clone the Repository

```bash
git clone https://github.com/Lutcheian/foundry-nft-f23.git
cd foundry-nft-f23
```

### Initialize Dependencies

```bash
git submodule update --init --recursive
```

### Build the Project

```bash
forge build
```

### Run Tests

```bash
forge test
```

Run the test coverage report:

```bash
forge coverage
```

## Local Deployment

Start Anvil:

```bash
anvil
```

In another terminal, deploy the Mood NFT:

```bash
make deployMood
```

This deploys the contract to your local Anvil blockchain.

## Sepolia Deployment

Configure your environment variables in `.env`:

```env
SEPOLIA_RPC_URL=YOUR_SEPOLIA_RPC_URL
PRIVATE_KEY=YOUR_PRIVATE_KEY
```

**Security:** Never commit your `.env` file or expose your private key.

Deploy using:

```bash
make deployMood ARGS="--network sepolia"
```

## Learning Objectives

This project demonstrates:

- ERC-721 NFT development.
- Smart contract deployment with Foundry.
- Unit and integration testing.
- Dynamic NFT metadata.
- SVG image encoding using Base64.
- Local blockchain development with Anvil.
- Ethereum testnet deployment.

## Author

**Kren Muts**

---

*Built with Solidity and Foundry.*