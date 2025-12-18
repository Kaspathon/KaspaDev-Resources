# Overview: Understanding Kaspa

Welcome to Kaspa development! This guide will help you understand what makes Kaspa unique and get you ready to start building.

## New to Kaspa?

### Start Here

If you're new to Kaspa, we recommend following this learning path:

1. **Read the introduction below** to understand what Kaspa is or head to **[kaspa.org](https://kaspa.org)** for a quick overview
2. **Explore the [Kaspa Wiki](https://wiki.kaspa.org/en/home)** for comprehensive community documentation
3. **Curious about how the magic DAG works?** Watch this detailed explanation: **[BlockDAG Introduction Video](https://www.youtube.com/watch?v=nhI2zo44dfc)** 
4. **Get a wallet** (see options below) to start interacting with the network
5. **Try the testnet** to build and experiment safely

### Get a Wallet

Before you start developing, you'll want a Kaspa wallet to interact with the network:

**Browser Extension Wallets:**
- **[Kasware](https://www.kasware.xyz/)** - Browser extension wallet
- **[Kastle](https://kastle.cc)** - Browser extension wallet

**Desktop/Mobile Wallets:**
- **[Kaspium](https://kaspium.io)** - Mobile-first wallet
- **[Kurncy](https://www.kurncy.com/)** - Feature-rich wallet
- **[Kaspa NG](https://kaspa-ng.org/)** - Full-featured desktop wallet

**Full wallet list**: [kaspa.org](https://kaspa.org)

## What is Kaspa?

Kaspa is the fastest and most scalable instant confirmation transaction layer ever built on a proof-of-work engine. Transactions sent to miners can be included immediately in the ledger, which is structured as a revolutionary blockDAG. Kaspa is based on the GhostDAG/PHANTOM protocol, a scalable generalization of the Nakamoto Consensus (Bitcoin consensus). Its design is faithful to the principles Satoshi embedded into Bitcoin — proof-of-work mining, UTXO-formed isolated state, deflationary monetary policy, no premine, and no central governance. Kaspa is unique in its ability to support high block rates while maintaining the level of security offered by the most secure proof-of-work environments.

**Current Performance:**
- **10 blocks per second (10 BPS)** on mainnet
- **Battle-tested at scale**: 158 million transactions processed during mainnet stress tests (October 2025)
- **Fast finality**: Near-instant transaction confirmation
- **Low transaction costs**: Minimal fees for all transactions 

## Why Build on Kaspa?

### 1. **High Throughput & Scalability**
- **10 blocks per second** on mainnet (10 BPS)
- **Proven at scale**: Processed 158M+ transactions in stress tests
- **Near-instant confirmations**: Fast finality for transactions
- **Low fees**: Minimal transaction costs

### 2. **Unique Architecture**
- BlockDAG instead of linear blockchain
- Parallel block creation and validation
- Novel approach to consensus and ordering

### 3. **UTXO Model**
- Similar to Bitcoin's proven transaction model
- Straightforward programming model
- Well-understood security properties

### 4. **Growing Ecosystem**
- Active development community
- Emerging DeFi and token standards (KRC-20)
- Opportunities for innovation

## Kaspa vs Traditional Blockchains

| Feature | Traditional Blockchain | Kaspa BlockDAG |
|---------|----------------------|----------------|
| **Structure** | Single chain | Directed Acyclic Graph |
| **Block Creation** | Sequential | Parallel (10 BPS) |
| **Throughput** | Limited by block time | 10 blocks/second (proven at 158M+ in 24h tx scale) |
| **Transaction Fees** | Variable, can be high | Low and consistent |
| **Finality** | Multiple confirmations | Fast (near-instant) |
| **Orphan Blocks** | Discarded | Included in consensus |

## Core Concepts

### BlockDAG

Instead of a single chain where blocks reference one parent, Kaspa's BlockDAG allows blocks to reference multiple parents. This enables:
- **Parallel mining**: Multiple miners can produce blocks simultaneously
- **Higher throughput**: Network isn't limited to sequential block production
- **No wasted work**: All valid blocks contribute to consensus

### UTXO (Unspent Transaction Output)

Kaspa uses Bitcoin's UTXO model:
- Transactions consume previous outputs and create new ones
- Clear ownership and state tracking
- Efficient validation and pruning

### KRC-20 Tokens

KRC-20 is an emerging token standard on Kaspa:
- Similar to Ethereum's ERC-20 concept
- Built using data insertion mechanisms
- Enabled by the Kasplex protocol
- Open-source indexer and APIs

## Development Networks

### Testnet (Recommended for Development)

Build and test your applications safely on Kaspa's testnet:

**Testnet Faucet:**
- Get free testnet KAS tokens: **[https://faucet-tn10.kaspanet.io/](https://faucet-tn10.kaspanet.io/)**

**Run Your Own Node**
- **Rusty Kaspa**: Download from [github.com/kaspanet/rusty-kaspa/releases](https://github.com/kaspanet/rusty-kaspa/releases)
- **Kaspa NG**: Download from [github.com/aspectron/kaspa-ng/releases](https://github.com/aspectron/kaspa-ng/releases)

Running your own node gives you:
- Full control and no rate limits
- Better privacy
- Faster development iteration
- Deeper understanding of the network

## Getting Started

Now that you understand Kaspa's fundamentals:

1. **[Follow the quickstart](./quickstart.md)** - Build your first Kaspa application

## Additional Learning

- **[Kaspa Wiki](https://wiki.kaspa.org/en/home)** - Comprehensive community documentation
- **[WASM SDK Documentation](https://kaspa.aspectron.org/docs/)** - Full specifications for direct integration of Rust code in JavaScript/TypeScript
- **[Kaspa.org Developments](https://kaspa.org/developments)** - Ecosystem projects
- **[Rusty Kaspa](https://github.com/kaspanet/rusty-kaspa)** - Core implementation source code

## Fun Resources

- **[TX Missile Command](https://tx-missile-command.com/)** - A game where you shoot Kaspa transactions!

---

**Next**: [Quick Start Guide](./quickstart.md) →
