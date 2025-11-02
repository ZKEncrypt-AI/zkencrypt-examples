# ZKEncrypt Examplesd

Example applications and tutorials for building with ZKEncrypt Network. Learn how to integrate FHE privacy into your dApps.

## 📚 Examples

### 1. Basic FHE Operations
Location: `/basic-fhe`

Simple examples demonstrating encryption, decryption, and homomorphic operations.

```typescript
import { ZKEncryptSDK } from '@zkencrypt/sdk';

const sdk = new ZKEncryptSDK({ network: 'devnet' });
const encrypted = await sdk.encrypt({ data: 'Hello', publicKey });
const decrypted = await sdk.decrypt({ ciphertext: encrypted.ciphertext, privateKey });
```

[View Full Example →](./basic-fhe)

### 2. Confidential Token
Location: `/confidential-token`

ERC20 token with private balances using FHE. Users can transfer tokens without revealing amounts.

**Features:**
- Private balance storage
- Encrypted transfers
- Public total supply
- Access control for viewing balances

[View Full Example →](./confidential-token)

### 3. Private Auction DApp
Location: `/private-auction`

Sealed-bid auction where bids remain encrypted until the auction ends.

**Features:**
- Hidden bid amounts
- Automatic winner determination
- No front-running possible
- Fair bidding process

[View Full Example →](./private-auction)

### 4. Encrypted Voting System
Location: `/encrypted-voting`

DAO governance with secret ballot voting.

**Features:**
- Anonymous voting
- Encrypted vote tallying
- Results revealed after voting period
- Sybil resistance

[View Full Example →](./encrypted-voting)

### 5. Private DeFi Lending
Location: `/private-lending`

Privacy-preserving lending protocol where collateral amounts remain hidden.

**Features:**
- Private collateral amounts
- Encrypted interest rates
- Hidden loan positions
- Secure liquidations

[View Full Example →](./private-lending)

### 6. x402 Micropayments
Location: `/x402-payments`

Send privacy-preserving micropayments on Solana with sub-cent fees.

**Features:**
- Payments under $0.01
- Privacy by default
- Instant settlement
- ZK-proof verification

[View Full Example →](./x402-payments)

### 7. AI Oracle Integration
Location: `/ai-oracle`

Query AI models with encrypted prompts and receive encrypted responses.

**Features:**
- Private AI inference
- Multiple model support
- Encrypted prompt/response
- Pay-per-query

[View Full Example →](./ai-oracle)

### 8. Private NFT Marketplace
Location: `/private-nft`

NFT marketplace with hidden bids and private sales.

**Features:**
- Private offer amounts
- Sealed-bid auctions
- Hidden collection floor prices
- Confidential royalties

[View Full Example →](./private-nft)

### 9. Shielded DEX Swap
Location: `/private-swap`

Decentralized exchange with private swap amounts.

**Features:**
- Hidden swap amounts
- Private liquidity pools
- MEV protection
- Multi-token support

[View Full Example →](./private-swap)

### 10. Full-Stack dApp Template
Location: `/fullstack-template`

Complete dApp template with React frontend, Solana backend, and FHE integration.

**Stack:**
- React + TypeScript
- @zkencrypt/sdk
- Solana wallet integration
- Tailwind CSS

[View Full Example →](./fullstack-template)

## 🚀 Quick Start

### Prerequisites

- Node.js >= 16
- npm or yarn
- Solana wallet (Phantom, Solflare, etc.)

### Installation

```bash
# Clone the repository
git clone https://github.com/ZKEncrypt-AI/zkencrypt-examples.git
cd zkencrypt-examples

# Install dependencies
npm install

# Copy environment variables
cp .env.example .env
```

### Running Examples

```bash
# Navigate to an example
cd basic-fhe

# Install dependencies
npm install

# Run the example
npm start
```

## 🛠️ Development

### Using with Local SDK

```bash
# Link local SDK
cd /path/to/zkencrypt-sdk
npm link

cd /path/to/zkencrypt-examples/basic-fhe
npm link @zkencrypt/sdk
```

### Environment Variables

Each example includes an `.env.example` file. Copy it to `.env` and fill in your values:

```env
VITE_NETWORK=devnet
VITE_RPC_URL=https://api.devnet.solana.com
VITE_FHE_ENDPOINT=https://fhe.zk-labs.network
VITE_ORACLE_ENDPOINT=https://oracle.zk-labs.network
```

## 📖 Tutorials

### Tutorial 1: Building Your First FHE dApp

Learn the basics of FHE integration:
1. Setup ZKEncrypt SDK
2. Encrypt/decrypt data
3. Perform homomorphic operations
4. Build a simple UI

[Read Tutorial →](./tutorials/01-first-fhe-dapp.md)

### Tutorial 2: Private Token Transfers

Build a confidential ERC20 token:
1. Deploy ConfidentialERC20
2. Implement private transfers
3. Add access control
4. Build token UI

[Read Tutorial →](./tutorials/02-private-token.md)

### Tutorial 3: Sealed-Bid Auction

Create a privacy-preserving auction:
1. Design auction contract
2. Implement encrypted bidding
3. Winner determination
4. Refund logic

[Read Tutorial →](./tutorials/03-sealed-auction.md)

## 🎯 Use Cases

### DeFi
- Private lending/borrowing
- Confidential trading
- Hidden liquidity pools
- Encrypted collateral

### Gaming
- Hidden game state
- Private loot boxes
- Confidential player stats
- Sealed-bid tournaments

### Governance
- Anonymous voting
- Private proposals
- Hidden vote counts
- Sybil-resistant polls

### Enterprise
- Confidential supply chain
- Private B2B transactions
- Encrypted employee data
- GDPR-compliant storage

## 🔗 Resources

- [ZKEncrypt SDK](https://github.com/ZKEncrypt-AI/zkencrypt-sdk)
- [Solidity Contracts](https://github.com/ZKEncrypt-AI/zkencrypt-solidity)
- [CLI Tool](https://github.com/ZKEncrypt-AI/zkencrypt-cli)
- [Documentation](https://zkencrypt-ai.gitbook.io/zkencrypt-ai)

## 🤝 Contributing

We welcome new examples! Please:
1. Fork the repository
2. Create an example in a new folder
3. Add README with clear instructions
4. Submit a pull request

## 📄 License

MIT License - see [LICENSE](LICENSE) for details.

---

Built with ❤️ by the ZKEncrypt AI team
