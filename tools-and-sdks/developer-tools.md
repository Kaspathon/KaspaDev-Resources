# Developer Tools & SDKs

Comprehensive list of tools, libraries, and resources for building on Kaspa.

## Development SDKs

### Kaspa-JS
**Node.js/TypeScript SDK and starter kit**

- **Repository**: [github.com/K-Kluster/kaspa-js](https://github.com/K-Kluster/kaspa-js)
- **Language**: JavaScript/TypeScript
- **Best For**: Web applications, Node.js backends, quick prototyping
- **Features**:
  - Wallet management
  - Transaction creation and signing
  - Network interaction
  - UTXO handling
  - TypeScript support

**Installation:**
```bash
git clone https://github.com/K-Kluster/kaspa-js.git
cd kaspa-js
npm install
```

**Quick Example:**
```javascript
const { Wallet, Client } = require('kaspa-js');

const wallet = new Wallet();
const client = new Client({ network: 'mainnet' });
// Start building!
```

### Rusty Kaspa Libraries
**Core Rust implementation and libraries**

- **Repository**: [github.com/kaspanet/rusty-kaspa](https://github.com/kaspanet/rusty-kaspa)
- **Language**: Rust
- **Best For**: High-performance applications, infrastructure, native tools
- **Features**:
  - Full node implementation
  - Consensus engine
  - RPC client
  - CLI wallet
  - WASM bindings

**Key Crates:**
- `kaspa-cli` - Command-line wallet and RPC interface
- `kaspa-rpc-core` - RPC client implementation
- `kaspa-wallet-core` - Wallet functionality
- `kaspa-consensus-core` - Consensus and BlockDAG

**Installation:**
```bash
git clone https://github.com/kaspanet/rusty-kaspa.git
cd rusty-kaspa
cargo build --release
```

**Rust Tutorial:**
- **[KDApp](https://github.com/michaelsutton/kdapp)** - Comprehensive tutorial for building Kaspa applications in Rust (check also https://x.com/michaelsuttonil/status/1940238214817612014?s=20 )
- Covers wallet operations, transactions, network communication, and UTXO handling

### WASM SDK
**Direct integration of Rust code in JavaScript/TypeScript**

- **Documentation**: [kaspa.aspectron.org/docs](https://kaspa.aspectron.org/docs/)
- **Language**: JavaScript/TypeScript with Rust performance
- **Best For**: Browser applications, TypeScript projects requiring high performance
- **Features**:
  - Full Kaspa functionality in browser
  - Direct RPC integration
  - Wallet management
  - Transaction creation and signing
  - No backend required

**Installation:**
```bash
npm install @kaspa/core-wasm
```

**Quick Example:**
```typescript
import * as kaspa from '@kaspa/core-wasm';

await kaspa.init();
const wallet = kaspa.Wallet.create();
const rpc = new kaspa.RpcClient({ url: 'testnet.kaspathon.com' });
```

## Wallets

### Browser Extension Wallets

**Kasware**
- **Website**: [kasware.xyz](https://www.kasware.xyz/)
- Browser extension wallet

**Kastle**
- **Website**: [kastle.cc](https://kastle.cc)
- **Repository**: [github.com/forbole/kastle](https://github.com/forbole/kastle)
- Browser extension wallet
- Reference implementation for developers

### Desktop & Mobile Wallets

**Kaspium**
- **Website**: [kaspium.io](https://kaspium.io)
- Mobile-first wallet application
- User-friendly interface

**Kurncy**
- **Website**: [kurncy.com](https://www.kurncy.com/)
- Feature-rich wallet
- Desktop and mobile support

**Kaspa NG**
- **Website**: [kaspa-ng.org](https://kaspa-ng.org/)
- **Repository**: [github.com/aspectron/kaspa-ng](https://github.com/aspectron/kaspa-ng)
- Full-featured desktop wallet with built-in node
- Comprehensive development and user tools

**Full Wallet List**: [kaspa.org](https://kaspa.org)

## Blockchain Infrastructure

### Kaspa Full Node

Run your own Kaspa node for development and testing.

**Option 1: Rusty Kaspa (Command Line)**

Download pre-built binaries:
```bash
# Download from releases
wget https://github.com/kaspanet/rusty-kaspa/releases/latest/download/kaspad
chmod +x kaspad

# Run mainnet node
./kaspad

# Run testnet node
./kaspad --testnet
```

Or build from source:
```bash
git clone https://github.com/kaspanet/rusty-kaspa.git
cd rusty-kaspa
cargo build --release --bin kaspad
./target/release/kaspad --testnet
```

**Option 2: Kaspa NG (Desktop Application)**

Download the full desktop application with built-in node and wallet:
- **Releases**: [github.com/aspectron/kaspa-ng/releases](https://github.com/aspectron/kaspa-ng/releases)
- Includes GUI for node management
- Integrated wallet functionality
- Visual monitoring tools

**Benefits of Running Your Own Node:**
- ✅ Full control over your development environment
- ✅ No rate limits
- ✅ Better privacy
- ✅ Faster development iteration
- ✅ Can run testnet for safe testing
- ✅ Deeper understanding of network operations

**Hardware Requirements:**
- CPU: 2+ cores
- RAM: 4GB minimum, 8GB recommended
- Storage: 50GB+ SSD
- Network: Stable internet connection

### RPC Interfaces

**Kaspathon Public Nodes (Recommended for Hackathon):**
- **Testnet**: `testnet.kaspathon.com`
- **Mainnet**: `mainnet.kaspathon.com`

**Community Public Nodes:**
- Check documentation for additional public nodes
- Various community-provided endpoints available

**Testnet Faucet:**
- Get free testnet KAS: [https://faucet-tn10.kaspanet.io/](https://faucet-tn10.kaspanet.io/)

**Best Practice**: Run your own local node for development (see above)

**RPC Methods** (common operations):
```javascript
// Get block info
await client.rpc('getBlock', { blockHash });

// Get transaction
await client.rpc('getTransaction', { txId });

// Submit transaction
await client.rpc('submitTransaction', { transaction });

// Get balance
await client.rpc('getBalanceByAddress', { address });
```

## Token Development

### Kasplex Protocol
**KRC-20 token standard and tools**

- **Repository**: [github.com/argonmining/kasplex](https://github.com/argonmining/kasplex)
- **Purpose**: Standard for fungible tokens on Kaspa
- **Features**:
  - Token creation and minting
  - Open-source indexer
  - REST APIs for token data
  - Transfer and balance queries

**What You Can Build:**
- Fungible tokens
- Token-based applications
- Token indexing services
- Custom token standards

### KRC-20 Apps & Tools
**Token minting and management utilities**

- **Repository**: [github.com/coinchimp/kaspa-krc20-apps](https://github.com/coinchimp/kaspa-krc20-apps)
- **Features**:
  - Mnemonic phrase generation
  - Private key derivation
  - KRC-20 token minting
  - Wallet address generation

**Example Use Cases:**
- Mint your own tokens for the hackathon
- Build token distribution tools
- Create token-gated applications
- Develop token analytics

## Visualization & Monitoring

### Kaspa Graph Inspector
**Interactive BlockDAG visualization and analysis**

- **Repository**: [github.com/kaspa-live/kaspa-graph-inspector](https://github.com/kaspa-live/kaspa-graph-inspector)
- **Features**:
  - Real-time block creation visualization
  - Network dynamics display
  - BlockDAG structure representation
  - Graph inspection and analysis tools
  - Educational tool for understanding Kaspa

**Use Cases:**
- Learn how BlockDAG works
- Monitor network activity
- Analyze network topology
- Build custom visualizations
- Educational demonstrations

### Block Explorers

Use block explorers to view:
- Transaction details
- Block information
- Address balances
- Network statistics

**Community Explorers:**
- Check [kaspa.org](https://kaspa.org) for current explorer list


## Next Steps

- **[Build your first app](../getting-started/quickstart.md)** - Quick start guide
- **[Get support](../support/resources.md)** - Community help

---

**Have a favorite tool not listed here?** Contribute to this page!
