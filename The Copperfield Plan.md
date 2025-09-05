# The Copperfield Plan
## Tondi as Bitcoin's Proving Ground for Unadopted BIPs


The Copperfield Plan is our initiative to transform Tondi, a Taproot-native high-performance blockchain, into a living laboratory for Bitcoin's unadopted or experimental proposals. Our goal is twofold:

**Validation for Bitcoin** – provide a proving ground for technical ideas discussed in the Bitcoin community but not yet adopted into consensus.

**Preparation for the Next Era** – explore how Bitcoin's "impossible trinity" of decentralization, security, and scalability may shift dynamically, rather than remain frozen under extreme conservatism.

We believe that inaction is not entropy reduction. Conservatism preserves Bitcoin's security today, but experimentation is necessary to prepare for tomorrow.

---

## Focus Areas of Experimentation

Within Copperfield, we are actively implementing the following classes of proposals as core differentiators of Tondi:

### 🔹 Channel & Scalability Layer

- ✅ **ANYPREVOUT (TSP-0007)** – enabling eltoo and simplified channel updates. *Status: Review*
- ✅ **Channel Factories (TSP-0012)** – multi-party channel construction to reduce on-chain footprint. *Status: Draft*
- 🔄 **CTV (CheckTemplateVerify) (TSP-0009)** – covenant-based transaction commitments. *Status: Draft*

### 🔹 Privacy & Signature Layer

- ✅ **PTLC (TSP-0010)** – privacy-enhanced conditional payments. *Status: Draft*
- ✅ **CISA (TSP-0008)** – transaction size reduction via aggregate Schnorr signatures. *Status: Draft*
- ✅ **Native MuSig2 (TSP-0011)** – efficient multisig aggregation built into consensus rules. *Status: Draft*

### 🔹 Performance & State Management

- 🔄 **UTreeXO** – stateless client with Merkleized UTXO set. *Planned for future TSP*
- 🔄 **AssumeUTXO** – faster node bootstrapping with snapshot validation. *Planned for future TSP*

### 🔹 Extension Models

- 🔄 **Ark** – off-chain payment pools with improved UX. *Planned for future TSP*
- 🔄 **Statechains** – transferable off-chain custody with cryptographic handovers. *Planned for future TSP*

### 🔹 Covenant & Smart Contract Layer

- 🔄 **OP_VAULT** – secure vault mechanisms with delegated spending policies. *Planned for future TSP*
- 🔄 **OP_CAT** – reintroducing concatenation for expressive covenant design. *Planned for future TSP*
- 🔄 **OP_CSFS** – checksum-based script validation for advanced contracts. *Planned for future TSP*

### 🔹 Applications & Standards

- ✅ **FUN20 (TSP-0006)** – inscription-style fungible token standard. *Status: Review*

---

## Process and Community Feedback

### Current Implementation Status (January 2025)

#### Stage 1 – **Tondi Frontier (Testnet)**
- ✅ **TSP-0001**: Kaspa-Compatible Payment Types with Extended Taproot - **Implemented**
- ✅ **TSP-0002**: BLAKE3 Hash Algorithm Adoption - **Implemented** 
- ✅ **TSP-0004**: TSP Numbering and Lifecycle Definition - **Implemented**
- 🔄 **TSP-0003**: ASIC-Resistant PoW with BLAKE3+MTR - **Review**
- 🔄 **TSP-0005**: Biannual Evolution and Frontier Network - **Accepted**
- 🔄 **TSP-0006**: FUN20 Fungible Token Standard - **Review**

#### Stage 2 – **Mainnet Preparation**
- 📋 **TSP-0007**: ANYPREVOUT for Eltoo Channels - **Review** (Target: v2026a)
- 📋 **TSP-0008**: CISA Signature Aggregation - **Draft** (Target: v2026a)
- 📋 **TSP-0009**: CTV Covenants - **Draft** (Target: v2026b)
- 📋 **TSP-0010**: PTLC Contracts - **Draft** (Target: v2026a)
- 📋 **TSP-0011**: Native MuSig2 - **Draft** (Target: v2026a)
- 📋 **TSP-0012**: Channel Factories - **Draft** (Target: v2026b)

#### Stage 3 – **Reporting Back**
We commit to publishing technical reports for each tested proposal, feeding back real-world data, attack surfaces, and UX implications to the Bitcoin development community.

---

## 📊 Implementation Progress Overview

| Status | Count | Percentage |
|--------|-------|------------|
| ✅ Implemented | 3 | 25% |
| 🔄 Review | 3 | 25% |
| ✅ Accepted | 1 | 8.3% |
| 📋 Draft | 5 | 41.7% |
| **Total** | **12** | **100%** |

---

## 📋 Detailed Implementation Progress Table

### 🏗️ Core Protocol Layer

| TSP | Title | Status | Completion | Target Version | Implementation Phase | Notes |
|-----|-------|--------|------------|----------------|---------------------|-------|
| **TSP-0001** | Kaspa-Compatible Payment Types + Extended Taproot | ✅ **Implemented** | 100% | v2025a | ✅ Production | Supports all Kaspa payment types, adds Taproot support |
| **TSP-0002** | BLAKE3 Hash Algorithm Adoption | ✅ **Implemented** | 100% | v2025b | ✅ Production | Unified BLAKE3 usage across entire protocol stack |
| **TSP-0003** | ASIC-Resistant PoW (BLAKE3+MTR) | 🔄 **Review** | 75% | v2026b | 🔄 Testnet Validation | Memory-touch randomness algorithm design completed |

### 🏛️ Governance & Meta Protocol

| TSP | Title | Status | Completion | Target Version | Implementation Phase | Notes |
|-----|-------|--------|------------|----------------|---------------------|-------|
| **TSP-0004** | TSP Numbering, Categories, and Lifecycle Definition | ✅ **Implemented** | 100% | v2025a | ✅ Production | Two-phase numbering system established |
| **TSP-0005** | Biannual Evolution and Tondi Frontier Network | ✅ **Accepted** | 90% | v2025b | 🔄 Ready for Deployment | Frontier testnet formalization |

### 🚀 Applications Layer

| TSP | Title | Status | Completion | Target Version | Implementation Phase | Notes |
|-----|-------|--------|------------|----------------|---------------------|-------|
| **TSP-0006** | FUN20 - Inscription-style Fungible Token Standard | 🔄 **Review** | 80% | v2025b | 🔄 Testnet Validation | Complete token protocol specification with zk-proof support |

### ⚡ Consensus Layer

| TSP | Title | Status | Completion | Target Version | Implementation Phase | Notes |
|-----|-------|--------|------------|----------------|---------------------|-------|
| **TSP-0007** | ANYPREVOUT Support (Eltoo Payment Channels) | 🔄 **Review** | 70% | v2026a | 📋 Development | Core functionality for Tondi Flash |
| **TSP-0008** | CISA (Cross-Input Signature Aggregation) | 📋 **Draft** | 60% | v2026a | 📋 Design Phase | Transaction size optimization |
| **TSP-0009** | CTV (CheckTemplateVerify) Covenants | 📋 **Draft** | 50% | v2026b | 📋 Design Phase | Covenant primitive support |
| **TSP-0011** | Native MuSig2 Multi-Signatures | 📋 **Draft** | 55% | v2026a | 📋 Design Phase | Efficient multi-signature aggregation |

### 📏 Standards Layer

| TSP | Title | Status | Completion | Target Version | Implementation Phase | Notes |
|-----|-------|--------|------------|----------------|---------------------|-------|
| **TSP-0010** | Tondi PTLC (Point Time-Locked Contract) | 📋 **Draft** | 65% | v2026a | 📋 Design Phase | Privacy-enhanced conditional payments |

### 🌐 Layer 2

| TSP | Title | Status | Completion | Target Version | Implementation Phase | Notes |
|-----|-------|--------|------------|----------------|---------------------|-------|
| **TSP-0012** | Channel Factories (Scalable Off-Chain Payment Networks) | 📋 **Draft** | 45% | v2026b | 📋 Design Phase | Multi-party channel construction |

---

## 🔧 Technical Implementation Status

### Completed Implementations
1. **TSP-0001**: Kaspa-Compatible Payment Types + Taproot Support
   - ✅ Support for all Kaspa native payment types
   - ✅ Added Taproot (P2TR) output support
   - ✅ BIP-340 Schnorr signature compatibility
   - ✅ Bech32m address format (`tondi` prefix)

2. **TSP-0002**: BLAKE3 Hash Algorithm
   - ✅ Block header hashing (consensus path)
   - ✅ Transaction ID generation
   - ✅ Merkle tree construction
   - ✅ Script and contract hash references
   - ✅ RGB anchoring consistency

3. **TSP-0004**: TSP Numbering and Lifecycle
   - ✅ Two-phase numbering system
   - ✅ Category system definition
   - ✅ Lifecycle process
   - ✅ Editorial responsibilities and community governance

### In Development
1. **TSP-0003**: ASIC-Resistant PoW
   - 🔄 BLAKE3-MTR algorithm design
   - 🔄 Memory-touch randomness implementation
   - 🔄 Adjustable parameter design
   - 📋 Testnet validation preparation

2. **TSP-0006**: FUN20 Token Standard
   - 🔄 Compact payload design (≤128 bytes)
   - 🔄 Deterministic replay specification (CRS)
   - 🔄 MEV-resistant shuffling
   - 🔄 Dual deployment model (Deploy-Mint/Deploy-Issue)

### Design Phase
1. **TSP-0007**: ANYPREVOUT
   - 📋 Tapscript opcode design
   - 📋 Dynamic UTXO binding
   - 📋 Eltoo channel support
   - 📋 Tondi Flash integration

2. **TSP-0008**: CISA Signature Aggregation
   - 📋 Cross-input signature aggregation
   - 📋 Transaction size optimization
   - 📋 Privacy enhancement
   - 📋 Verification efficiency improvement

---

## 📈 Performance Metrics & Impact

### Performance Improvements from Implemented Features
- **BLAKE3 Hashing**: 30-50% performance improvement over SHA-256
- **Taproot Support**: Enhanced privacy with script path hiding
- **Kaspa Compatibility**: 100% backward compatibility, seamless migration

### Expected Performance Improvements (2026)
- **ANYPREVOUT**: Payment channel update latency <1ms
- **CISA**: Transaction size reduction of 30-50%
- **PTLC**: Significant privacy enhancement, no hash leakage
- **Channel Factories**: 90% reduction in off-chain channel creation costs

---

## 🎯 Key Milestone Timeline

### Q1 2025
- ✅ **TSP-0001**: Kaspa Compatibility + Taproot Support (Completed)
- ✅ **TSP-0002**: BLAKE3 Hash Algorithm (Completed)
- ✅ **TSP-0004**: TSP Numbering System (Completed)
- 🔄 **TSP-0003**: ASIC-Resistant PoW (Testnet Validation)
- 🔄 **TSP-0005**: Frontier Network (Ready for Deployment)
- 🔄 **TSP-0006**: FUN20 Token Standard (Testnet Validation)

### Q2 2025
- 🎯 **TSP-0003**: ASIC-Resistant PoW (Mainnet Deployment)
- 🎯 **TSP-0005**: Frontier Network (Formal Activation)
- 🎯 **TSP-0006**: FUN20 Token Standard (Mainnet Deployment)

### Q1 2026
- 🎯 **TSP-0007**: ANYPREVOUT (Mainnet Deployment)
- 🎯 **TSP-0008**: CISA Signature Aggregation (Mainnet Deployment)
- 🎯 **TSP-0010**: PTLC Contracts (Mainnet Deployment)
- 🎯 **TSP-0011**: Native MuSig2 (Mainnet Deployment)

### Q2 2026
- 🎯 **TSP-0009**: CTV Covenants (Mainnet Deployment)
- 🎯 **TSP-0012**: Channel Factories (Mainnet Deployment)

---

## 🔗 Repository Information

**GitHub Repository**: [https://github.com/Tondi-Foundation/Tondi-Standard-Proposal](https://github.com/Tondi-Foundation/Tondi-Standard-Proposal)

---

## Philosophy

Bitcoin's durability is built on caution, but progress comes from active exploration. Tondi's Copperfield Plan embraces this role:

**Not to compete with Bitcoin**, but to act as its wind tunnel—testing how new mechanics behave in live environments.

**Not to dilute security**, but to generate empirical data that Bitcoin Core and BIP authors can evaluate.

**Not to break the trilemma**, but to probe how decentralization, scalability, and security trade-offs evolve dynamically.

By running these experiments on Tondi, we hope to both strengthen Bitcoin's future path and prepare the ecosystem for the next technological cycle.