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
* **Standards / Interface** – Wallet formats, RPC APIs, contract schemas.
* **Governance / Meta** – Processes surrounding the TSP workflow and community rules.
* **Applications** – Proposals for RGB anchoring, Lexum contracts, AMMs, DAOs, etc.
* **Layer 2 (L2)** – Payment channels, channel factories, off-chain scaling solutions.

---

## 🏷 Numbering

* TSPs are assigned sequential numbers (e.g. **TSP-0001**).
* The number does not indicate importance, only order of registration.
* Example:

  * **TSP-0001** – Support Kaspa-Compatible Payment Types with Extended Taproot
  * **TSP-0002** – Adoption of BLAKE3 Hash Algorithm Across the Tondi Protocol
  * **TSP-0003** – ASIC-Resistant Proof-of-Work Hash Specification Based on BLAKE3 + Light Memory-Touching
  * **TSP-0004** – Definition of the TSP Numbering, Categories, and Lifecycle
  * **TSP-0005** – Biannual Evolution and the Tondi Frontier Network
  * **TSP-0006** – FUN20 — An Inscription-style Fungible Token Standard for Tondi
  * **TSP-0007** – ANYPREVOUT Support for Eltoo-based Payment Channels (Tondi Flash)
  * **TSP-0008** – CISA (Cross-Input Signature Aggregation)
  * **TSP-0012** – Channel Factories for Scalable Off-Chain Payment Networks

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
| [TSP-0007](./TSP-0007.md) | ANYPREVOUT Support for Eltoo-based Payment Channels (Tondi Flash) | Review | Consensus |
| [TSP-0008](./TSP-0008.md) | CISA (Cross-Input Signature Aggregation) | Draft | Consensus |
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
