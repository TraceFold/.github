<div align="center">

<a href="https://github.com/TraceFold/tracefold"><img src="https://github.com/TraceFold/tracefold/releases/download/brand-assets/banner.png" alt="tracefold" width="900"></a>

# TraceFold

### Autonomous AI Agent Reversibility & Verifiable Provenance Substrate

**Undo is a feature. Reversibility is a property.**

The checked inverse is sealed **before actions land**. Anyone can verify the verdict afterwards, offline, without trusting whoever issued it.

[![Repository](https://img.shields.io/badge/Repository-TraceFold%2Ftracefold-181614?style=flat-square&logo=github&logoColor=ece7da)](https://github.com/TraceFold/tracefold)
[![Browser Verifier](https://img.shields.io/badge/Verifier-Offline%20WASM-26231f?style=flat-square)](https://tracefold.github.io/tracefold/verify.html)
[![npm SDK](https://img.shields.io/npm/v/@mahirhir/tracefold?style=flat-square&color=4a3e31&label=npm%20SDK)](https://www.npmjs.com/package/@mahirhir/tracefold)
[![Discord](https://img.shields.io/badge/Community-Discord-3a3128?style=flat-square&logo=discord&logoColor=ece7da)](https://discord.gg/rtvXqYEQzr)

</div>

---

### The Paradigm Shift

| Dimension | Traditional Post-Hoc Audit Logs | TraceFold Pre-Fact Provenance |
| :--- | :--- | :--- |
| **Execution Order** | Action executes first $
ightarrow$ Logged afterwards | Inverse constructed & checked $
ightarrow$ **Action lands** |
| **Irreversible Damage** | Discovered only after system corruption | **Blocked at the gate**; escalates to human approval |
| **Verification Trust** | Must trust the host/server that produced the log | **Zero-trust offline verification** via standalone WASM |
| **Verdict Precision** | Binary (Pass/Fail) conflates errors with attacks | **Tri-state**: `Verified`, `Refuted`, `Unknown/Unparseable` |

---

### Ecosystem Components

| Module | Role & Specification | Tech Stack | Status |
| :--- | :--- | :--- | :---: |
| **[`TraceFold Core`](https://github.com/TraceFold/tracefold)** | Runtime substrate, state containment gate, and CLI | Rust 1.97.1 | Core Engine |
| **[`@mahirhir/tracefold`](https://www.npmjs.com/package/@mahirhir/tracefold)** | Offline receipt verifier (0 network calls) | TypeScript / WASM | Published (Apache-2.0) |
| **[`gui/`](https://github.com/TraceFold/tracefold/tree/main/gui)** | Local-first visual trace inspector | Desktop UI | Operational |
| **[`lean/`](https://github.com/TraceFold/tracefold/tree/main/lean)** | 117 machine-checked algebraic theorems | Lean 4 (`sorry` 0) | Mathematically Proven |

---

### Security Invariants

1. **Deterministic Approval Gate**: If a verified inverse cannot be constructed before execution, the agent stops immediately and escalates to human approval.
2. **Air-Gapped Offline Verification**: Verification executes entirely in-process or in-browser (WASM) with 0 network calls.
3. **Tri-State Verdict Architecture**: Explicitly outputs `Verified`, `Refuted`, or `Unknown/Unparseable` so parsing errors are never mislabeled as fraud.

---

<div align="center">
<sub>Built by <a href="https://glovrex.com">Glovrex</a> &middot; Licensed under Apache-2.0</sub>
</div>
