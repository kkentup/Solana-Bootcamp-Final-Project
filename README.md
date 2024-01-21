# Web3 Restaurant Review - README

Welcome to the **Web3 Restaurant review** project repository! This decentralized application (DApp) leverages blockchain technology to implement an restaurant review platform on the Solana network. Customers can read and submit reviews of experiences in restaurants.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Frontend](#frontend)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Usage](#usage)
- [Smart Contract](#smart-contract)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Usage](#usage)
- [License](#license)

## Overview

The **Web3 Restaurant Review* provides a user-friendly interface to participate in Solana-based restaurant reviews. This project ensures transparency and trust in the review process through the use of smart contracts.

## Features

- Browse existing customer reviews.
- Submit a new review.
- Solana Wallet Integration: Connect your Solana wallet (e.g., Phantom) to participate directly.

## Frontend

### Prerequisites

1. Node.js: Ensure Node.js is installed. Download it from [nodejs.org](https://nodejs.org/).

### Installation

1. Clone the repository:

```bash
  git clone https://github.com/kkentup/Solana-Bootcamp-Final-Project.git
```

2. Navigate to the frontend directory:

```bash
  cd Solana-Bootcamp-Final-Project/review_frontend
```

3. Install required npm packages:

```bash
  npm install
```

### Usage
1. Create a production build of the app

```bash
  npm run build
```

2. Start the server:

```bash
  npm start
```

3. Open your web browser and navigate to `http://localhost:3000` to access the DApp.

4. Connect your Solana wallet (e.g., Phantom) to the DApp. Need switch your wallet to Solana devnet before connection.

5. Browse existing reviews and submit your own reviews.

## Smart Contract

### Prerequisites
1. Solana tool suite: https://docs.solana.com/cli/install-solana-cli-tools

### Installation
1. Check current Solana CLI configuration:

```bash
  solana config get
```
Configuration example: \
Config File: /xxx/.config/solana/cli/config.yml \
RPC URL: https://api.mainnet-beta.solana.com \
WebSocket URL: wss://api.mainnet-beta.solana.com/ (computed) \
Keypair Path: /xxx/.config/solana/id.json \
Commitment: confirmed

2. If current "WebSocket URL" configuration is not devnet, target it to the Devnet cluster:

```bash
  solana config set --url https://api.devnet.solana.com
```

3. Create a signer account if needed, use what "Keypair Path" is in your Solana configuration output:

```bash
  solana-keygen new -o /xxx/.config/solana/id.json
```

4. Airdrop yourself 1 sol to play on devnet:

```bash
  solana airdrop 1
```

### Usage
1. Navigate to the contract directory:

```bash
  cd Solana-Bootcamp-Final-Project/review_contract
```

2. Build the program:

```bash
  cargo build-bpf
```

3. Deploy the program:

```bash
  solana program deploy ./target/deploy/review_contract.so
```

## License

This project is licensed under the [MIT License](LICENSE).

---

Thank you for your interest in the Web3 Restaurant Review project!
