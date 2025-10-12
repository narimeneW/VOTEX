# VoteX: Decentralized Voting Application

**VoteX** is a hybrid blockchain-based voting platform that merges the security and transparency of blockchain with the usability and efficiency of modern web applications. Its goal is to provide a secure, transparent, and accessible digital voting ecosystem for academic, organizational, or community elections.

---

## Overview

VoteX tackles key challenges in digital voting:

* **Security:** Voting logic runs on the Energy Web Volta blockchain.
* **Transparency:** All votes are permanently and publicly verifiable on-chain.
* **Accessibility:** User-friendly interface for non-technical participants.
* **Scalability:** Hybrid architecture capable of supporting elections of any size.

---

## Technology Stack

### Frontend

* **React.js & Next.js** – UI development
* **Ethers.js** – Blockchain wallet & smart contract interactions
* **Tailwind CSS** – Styling

### Backend

* **Node.js & Express.js** – RESTful API server
* **MongoDB** – Database for elections, voters, and candidates

### Blockchain

* **Solidity** – Smart contract development
* **Hardhat** – Ethereum development framework
* **IPFS** – Decentralized storage for assets
* **Energy Web Volta Testnet** – Deployment & testing

---

## Installation & Setup

### Prerequisites

* Node.js v14 or higher
* npm or yarn
* Git
* MongoDB (local or cloud instance)

---

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/VoteX.git
cd VoteX
```

### 2. Install Dependencies

```bash
npm install
```

---

## MetaMask Setup

1. **Install MetaMask**
   [Download MetaMask](https://metamask.io) and create a wallet. Keep your recovery phrase safe.

2. **Add Volta Testnet**

```
Network Name: Energy Web Volta
RPC URL: https://volta-rpc.energyweb.org
Chain ID: 73799
Currency Symbol: VT
Block Explorer: https://volta-explorer.energyweb.org/
```

3. **Get Test Tokens**
   Use the [Volta Faucet](https://voltafaucet.energyweb.org/) to request test tokens for your wallet.

---

## Smart Contract Deployment

### Configure Environment

Create a `.env` file in the project root:

```
NEXT_PUBLIC_CONTRACT_ADDRESS=your_deployed_contract_address
```

### Deploy Smart Contracts

```bash
npx hardhat compile
npx hardhat run scripts/deploy.js --network volta
```

After deployment, update `context/constants.js` in the frontend with the deployed contract address.

---

## Backend Setup

```bash
cd server
npm install
```

Create `.env` in `server/`:

```
MONGODB_URI=your_mongodb_connection_string
PORT=5000
```

Run the server:

```bash
npm start
```

---

## Frontend Setup

```bash
cd ..
npm run dev
```

Visit the app at [http://localhost:3000](http://localhost:3000)

---

## 🗳 Using VoteX

### For Admins (Election Organizers)

* Connect MetaMask wallet
* Create elections, add candidates, and set timings
* Publish and monitor election activity

### For Voters

* Connect MetaMask wallet
* Browse available elections
* Select a candidate and cast a vote
* Confirm the transaction in MetaMask
* Verify your vote on-chain

---

## Development & Contribution

**Local Smart Contract Testing**

```bash
npx hardhat node
npx hardhat run scripts/deploy.js --network localhost
```

**Deploying to Volta Testnet**

```bash
npx hardhat run scripts/deploy.js --network volta
```

After deployment, update the deployed contract address in `context/constants.js`.

---

## Notes

The project is under active development. Features like error handling and UI enhancements are in progress. Contributions are welcome via issues, forks, and pull requests.
