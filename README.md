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

---

## 🏷 Numbering

* TSPs are assigned sequential numbers (e.g. **TSP-0001**).
* The number does not indicate importance, only order of registration.
* Example:

  * **TSP-0001** – Support Kaspa-Compatible Payment Types with Extended Taproot
  * **TSP-0002** – BLAKE3 adoption across protocol
  * **TSP-0003** – ASIC-resistant PoW specification

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
