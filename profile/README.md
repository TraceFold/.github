<div align="center">

<a href="https://github.com/TraceFold/tracefold"><img src="https://github.com/TraceFold/tracefold/releases/download/brand-assets/banner.png" alt="tracefold" width="900"></a>

# TraceFold

### Autonomous AI Agent Reversibility & Verifiable Provenance Substrate

**Undo is a feature. Reversibility is a property.**

The checked inverse is sealed **before actions land**. Anyone can verify the verdict afterwards, offline, without trusting whoever issued it.

<p>
<a href="https://github.com/TraceFold/tracefold"><img src="https://img.shields.io/badge/Repository-TraceFold%2Ftracefold-7928ca?style=for-the-badge&logo=github&logoColor=ffffff" alt="TraceFold Repo"></a>
<a href="https://tracefold.github.io/tracefold/verify.html"><img src="https://img.shields.io/badge/Verifier-Zero%20Network%20WASM-00dfd8?style=for-the-badge&logo=webassembly&logoColor=090a0f" alt="Browser Verifier"></a>
<a href="https://www.npmjs.com/package/@mahirhir/tracefold"><img src="https://img.shields.io/badge/npm-SDK%20v0.1-0070f3?style=for-the-badge&logo=npm&logoColor=ffffff" alt="npm SDK"></a>
<a href="https://discord.gg/rtvXqYEQzr"><img src="https://img.shields.io/badge/Community-Discord-5865F2?style=for-the-badge&logo=discord&logoColor=ffffff" alt="Discord"></a>
</p>

</div>

---

### Target Architecture (System Context)

<div align="center">
<img src="https://raw.githubusercontent.com/TraceFold/tracefold/main/assets/glovrex_target_architecture_vision.png" alt="Glovrex Digital World - Target Architecture Vision" width="100%">
</div>

---

### Ecosystem Components

| Component | Responsibility | Tech Stack | Status |
| :--- | :--- | :--- | :---: |
| **[`TraceFold Core`](https://github.com/TraceFold/tracefold)** | Deterministic approval gate, runtime inverse engine, and CLI | Rust 1.97.1 | Core Engine |
| **[`@mahirhir/tracefold`](https://www.npmjs.com/package/@mahirhir/tracefold)** | Air-gapped offline receipt verifier (Zero network calls) | TypeScript / WASM | Published (Apache-2.0) |
| **[`gui/`](https://github.com/TraceFold/tracefold/tree/main/gui)** | Local-first visual inspector over execution traces and checkpoints | Desktop UI | Operational |
| **[`lean/`](https://github.com/TraceFold/tracefold/tree/main/lean)** | 117 machine-checked algebraic proofs with 0 `sorry` assertions | Lean 4 | Formally Verified |

---

### Resources & Access

- **Core Engine & CLI**: [`TraceFold/tracefold`](https://github.com/TraceFold/tracefold) &mdash; Source code, issue tracker, and discussions.
- **Instant WASM Verifier**: [`tracefold.github.io/tracefold/verify.html`](https://tracefold.github.io/tracefold/verify.html) &mdash; Standalone in-tab verification.
- **Formal Technical Report**: [`docs/TRACEFOLD_TR.md`](https://github.com/TraceFold/tracefold/blob/main/docs/TRACEFOLD_TR.md) &mdash; Mathematical foundation and error taxonomy.
- **Discord Community**: [`discord.gg/rtvXqYEQzr`](https://discord.gg/rtvXqYEQzr) &mdash; Research sparring and release notes.

---

<div align="center">
<sub>Built by <a href="https://glovrex.com">Glovrex</a> &middot; Licensed under Apache-2.0</sub>
</div>
