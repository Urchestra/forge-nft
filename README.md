 # 🔥 THE FORGE COLLECTIVE - Genesis NFT Collection

Welcome to **The Forge Collective**, an NFT collection of 4,444 unique digital builders designed to appeal to retailers, developers, and creative entrepreneurs. Built with cutting-edge blockchain technology, Privy wallet integration, and deployed on Vercel.

 ## 📋 Project Overview

### What is The Forge?

The Forge is more than an NFT collection—it's a philosophy for builders. Genesis NFTs represent 4,444 inaugural members of a community celebrating makers, hustlers, architects, rebels, and anchors.

### Key Features

✅ **4,444 Genesis NFTs** with 5 distinct tribes and procedural trait generation  
✅ **Token-Gated Minting** - Requires 10,000 FORGE tokens per mint  
✅ **Privy Wallet Integration** - Seamless authentication and wallet management  
✅ **Vercel Deployment** - Production-ready dApp hosted at vercel.app  
✅ **ERC721 + ERC20** - Full blockchain integration  
✅ **Retail-Ready** - Appeal to businesses, builders, and creators  

 ## 🏗️ The Five Tribes

Each NFT belongs to one of five distinct tribes:

| Tribe | Color | Role | Vision |
|-------|-------|------|--------|
| **Architect** | 🔵 Blue | System Designers | They design the ecosystem |
| **Craftsperson** | 🟤 Brown | Master Builders | They execute with precision |
| **Hustler** | 🟡 Gold | Dealmakers | They amplify and connect |
| **Rebel** | 🔴 Red | Disruptors | They challenge the status quo |
| **Anchor** | 🟢 Green | Community Builders | They ensure sustainability |

Each tribe has unique visual characteristics, backgrounds, and status symbols.

## 🚀 Quick Start

### Option 1: Deploy in 10 Minutes

**Step 1: Clone & Install**
```bash
git clone <your-repo-url>
cd forge-nft
npm install
```

**Step 2: Set Environment Variables**
```bash
cp .env.example .env.local
# Edit .env.local with your values:
# - NEXT_PUBLIC_PRIVY_APP_ID (from privy.io)
# - Contract addresses (after deployment)
```

**Step 3: Deploy Smart Contracts**
```bash
# Deploy to Sepolia testnet
npm run deploy:token -- --network sepolia
npm run deploy:nft -- --network sepolia
```

**Step 4: Deploy to Vercel**
```bash
npm run build
npm install -g vercel
vercel --prod
```

**That's it!** Your dApp is live. 🎉

### Option 2: Local Development

```bash
npm run dev
# Opens http://localhost:3000
```

---

## 📦 Project Structure

```
forge-nft/
├── app/
│   ├── _app.tsx           # Privy provider setup
│   └── index.tsx          # Main minting interface
├── contracts/
│   ├── ForgeToken.sol     # ERC20 token (45M supply)
│   └── ForgeNFT.sol       # ERC721 NFT (4,444 max)
├── scripts/
│   ├── deployToken.js     # Token deployment
│   └── deployNFT.js       # NFT deployment
├── styles/
│   ├── globals.css        # Global styles
│   └── Home.module.css    # Page-specific styles
├── package.json           # Dependencies
├── next.config.js         # Next.js config
├── hardhat.config.js      # Hardhat config
└── DEPLOYMENT_GUIDE.md    # Full deployment instructions
```

---

## 🔐 Smart Contracts

### ForgeToken (ERC20)
- **Total Supply**: 45,000,000 FORGE tokens
- **Decimals**: 18
- **Purpose**: Gate NFT minting & future governance
- **Minting Cost**: 10,000 FORGE per NFT

### ForgeNFT (ERC721)
- **Collection**: The Forge Collective - Genesis
- **Max Supply**: 4,444 NFTs
- **Traits**: 
  - Tribe (5 options)
  - Background (5 options)
  - Status Symbol (6 options)
  - Rarity Score (1-100)
- **Mint Restriction**: One per address (during Genesis)
- **Metadata**: Stored on-chain with trait encoding

---

## 💼 For Retailers & Businesses

### Merchant Benefits

- **Brand Partnerships**: Exclusive merchandise access
- **Customer Loyalty**: Reward program integration
- **Marketing**: Community-driven promotion
- **Revenue Share**: Profit participation for early partners

### Integration Options

1. **NFT Verification**: Check holder status via smart contract
2. **Merchant API**: Custom endpoints for retailers
3. **White Label**: Customize checkout experience
4. **Multi-Chain**: Cross-chain compatibility coming

---

## 🛠️ For Developers & Builders

### Developer Tools

```typescript
// Connect Wallet
const { login, authenticated, user } = usePrivy();

// Get User's NFT Data
const nftContract = new ethers.Contract(NFT_ADDRESS, ABI, provider);
const hasGenesis = await nftContract.hasMintedGenesis(userAddress);

// Check Token Balance
const balance = await tokenContract.balanceOf(userAddress);
```

### SDK & Libraries

- **ethers.js v6** - Blockchain interaction
- **Privy SDK** - Wallet management
- **Next.js 14** - React framework
- **React Query** - State management

### API Documentation

See `DEPLOYMENT_GUIDE.md` for complete API reference and code examples.

---

## 🌐 Deployment Checklist

- [ ] Smart contracts deployed to testnet
- [ ] Privy application created
- [ ] Environment variables configured
- [ ] GitHub repository created
- [ ] Vercel project linked
- [ ] Environment variables added to Vercel
- [ ] Production contracts deployed
- [ ] Privy domain allowlist updated
- [ ] dApp tested end-to-end
- [ ] Announced to community

**See DEPLOYMENT_GUIDE.md for detailed step-by-step instructions**

---

## 🎮 Testing

### Testnet Flow

1. Get free Sepolia ETH: https://www.alchemy.com/faucets/ethereum-sepolia
2. Deploy contracts to Sepolia
3. Manually transfer FORGE tokens to test wallet
4. Mint test NFTs
5. Verify on Etherscan

### Unit Tests

```bash
npx hardhat test
```

---

## 📊 Gas Optimization

- ✅ Token transfer: ~65K gas
- ✅ NFT mint: ~120K gas
- ✅ Trait lookup: ~25K gas (view function)

**Total mint transaction: ~185K gas**

---

## 🔒 Security

- ✅ ERC standard implementations (OpenZeppelin)
- ✅ No admin/owner keys in frontend
- ✅ Privy handles wallet security
- ✅ Contract-level access control
- ✅ One-mint-per-address during Genesis

### Audit Recommendations

Before mainnet launch:
1. Code review by experienced Solidity developer
2. Formal security audit (Trail of Bits, OpenZeppelin)
3. Mainnet testing with limited supply
4. Bug bounty program

---

## 🌍 Environment Variables

```bash
# Required for all environments
NEXT_PUBLIC_PRIVY_APP_ID=your_privy_app_id

# After contract deployment
NEXT_PUBLIC_NFT_CONTRACT=0x...
NEXT_PUBLIC_TOKEN_CONTRACT=0x...

# Network configuration
NEXT_PUBLIC_CHAIN_ID=11155111 (Sepolia) or 1 (Mainnet)
NEXT_PUBLIC_RPC_URL=https://rpc.ankr.com/eth_sepolia
```

---

## 📱 Browser Support

- ✅ Chrome/Edge 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

---

## 🤝 Community & Support

- **Discord**: [Your Discord Link]
- **Twitter**: [@TheForgeCollective](https://twitter.com)
- **Website**: [Your Website]
- **Email**: support@theforge.collective

---

## 📝 License

MIT License - See LICENSE file for details

---

## 🎯 Roadmap

### Phase 1: Genesis (Current)
- ✅ 4,444 Genesis NFTs
- ✅ Privy integration
- ✅ Vercel deployment

### Phase 2: Utility (Q1 2025)
- Retail merchant integration
- Developer SDK release
- DAO governance token

### Phase 3: Evolution (Q2 2025)
- Legendary variants
- Cross-chain bridging
- Community-driven updates

### Phase 4: Ecosystem (Q3 2025)
- Native marketplace
- Staking rewards
- Partner launches

---

## 🔥 Made With

- **Smart Contracts**: Solidity + OpenZeppelin
- **Frontend**: Next.js 14 + React 18
- **Blockchain**: Ethereum
- **Wallet**: Privy
- **Hosting**: Vercel
- **Styling**: CSS Modules + Modern CSS

---

## 💜 Special Thanks

To all the builders, makers, hustlers, rebels, and anchors who inspired this project.

**In The Forge, there are no passengers—only protagonists.**

---

## 📄 License

MIT © 2024 The Forge Collective

---

**Ready to mint? Visit the dApp and join 4,444 builders reshaping the future.**

🔥 **LET'S BUILD TOGETHER**

