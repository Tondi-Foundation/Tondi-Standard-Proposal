# Tondi Standard Proposals (TSP)

The **Tondi Standard Proposal (TSP)** process defines the evolution of the **Tondi blockchain** and its ecosystem.
TSPs are the canonical way to propose, discuss, and standardize protocol-level changes, ecosystem conventions, and governance rules within the Tondi network.

---

## 📌 What is a TSP?

A **TSP (Tondi Standard Proposal)** is a design document that provides information to the Tondi community or describes a new feature for the Tondi chain, its consensus, or its ecosystem.
Each TSP should:

* Provide a **clear technical specification** of the change or feature.
* Explain the **motivation and rationale** behind it.
* Describe any **backward compatibility** and **security considerations**.
* Define the **implementation and activation plan**.

TSPs are the primary mechanism for standardizing the Tondi protocol and ensuring long-term coherence of the ecosystem.

---

## 📖 Proposal Workflow

A TSP moves through several stages in its lifecycle:

1. **Draft** – Initial version, open for feedback.
2. **Review / Last Call** – Under technical review and community discussion.
3. **Accepted** – Approved for inclusion in a future Tondi release.
4. **Implemented** – Implemented in reference clients and/or testnet.
5. **Final (Active)** – Successfully deployed and active on mainnet.
6. *(Optional)* **Replaced / Deprecated** – Superseded by another TSP.

---

## 📂 TSP Categories

TSPs are grouped into categories, depending on their scope:

* **Core** – Consensus rules, transaction validation, block structure, cryptography.
* **Networking** – P2P protocols, mempool, synchronization rules.
* **Applications** – Proposals for RGB anchoring, Lexum contracts, AMMs, DAOs, etc.
* **Layer 2 (L2)** – Payment channels, channel factories, off-chain scaling solutions.
* **Process / Governance** – Processes surrounding the TSP workflow and community rules.
* **Standards / Interface** – Wallet formats, RPC APIs, contract schemas, interoperability protocols.
* **Informational** – Research papers, best practices, educational content.

---

## 🏷 TSP Numbering System

The TSP numbering system follows a **two-phase approach** as defined in [TSP-0004](./TSP-0004.md):

### **Phase 1: Early TSPs (until October 2025)**
* **Sequential numbering**: `TSP-0001`, `TSP-0002`, `TSP-0003`, etc.
* Reserved for **Genesis Protocol specifications** and early ecosystem standards
* Current proposals (TSP-0001 through TSP-0012) follow this format

### **Phase 2: Categorized TSPs (from October 2025 onward)**
Proposals will use **category prefixes** + numeric sequence:

* **TSP-Cxxx** → Core/Consensus (transaction validation, PoW, cryptography)
* **TSP-Nxxx** → Networking (P2P protocols, mempool, synchronization)
* **TSP-Axxx** → Applications (RGB, Lexum contracts, AMMs, DAOs)
* **TSP-Lxxx** → Layer 2 (payment channels, scaling solutions)
* **TSP-Pxxx** → Process/Governance (workflow, voting mechanisms)
* **TSP-Sxxx** → Standards/Interface (wallet formats, APIs, schemas)
* **TSP-Ixxx** → Informational (research papers, best practices)

This ensures both **historical continuity** and **scalability** for long-term ecosystem growth.

---

## 📋 Current Proposals

| Number | Title | Status | Category |
|--------|-------|--------|----------|
| [TSP-0001](./TSP-0001.md) | Support Kaspa-Compatible Payment Types with Extended Taproot | Implemented | Core |
| [TSP-0002](./TSP-0002.md) | Adoption of BLAKE3 Hash Algorithm Across the Tondi Protocol | Implemented | Core |
| [TSP-0003](./TSP-0003.md) | ASIC-Resistant Proof-of-Work Hash Specification Based on BLAKE3 + Light Memory-Touching | Review | Core |
| [TSP-0004](./TSP-0004.md) | Definition of the TSP Numbering, Categories, and Lifecycle | Implemented | Governance/Meta |
| [TSP-0005](./TSP-0005.md) | Biannual Evolution and the Tondi Frontier Network | Accepted | Governance/Meta |
| [TSP-0006](./TSP-0006.md) | FUN20 — An Inscription-style Fungible Token Standard for Tondi | Review | Applications |
| [TSP-0007](./TSP-0007.md) | ANYPREVOUT Support for Eltoo-based Payment Channels (Tondi Flash) | Draft | Consensus |
| [TSP-0008](./TSP-0008.md) | CISA (Cross-Input Signature Aggregation) | Draft | Consensus |
| [TSP-0009](./TSP-0009.md) | Native MuSig2 Multi-Signatures | Draft | Consensus |
| [TSP-0010](./TSP-0010.md) | Tondi PTLC (Point Time-Locked Contract) Contract Specification | Draft | Standards Track |
| [TSP-0011](./TSP-0011.md) | Native MuSig2 Multi-Signatures | Draft | Consensus |
| [TSP-0012](./TSP-0012.md) | Channel Factories for Scalable Off-Chain Payment Networks | Draft | Layer 2 (L2) |

---

## ✍️ How to Propose a TSP

1. Fork this repository.
2. Create a new file under `/tsp` named `tsp-xxxx.md`, where `xxxx` is your draft number.
3. Write the TSP using the official [TSP Template](./TSP-TEMPLATE.md).
4. Submit a Pull Request.
5. The TSP editors and the community will review and assign an official number.

---

## 📜 License

All TSP documents are licensed under **CC0 1.0 Universal (Public Domain Dedication)**.