<div align="center">

<a href="https://github.com/TraceFold/tracefold"><img src="https://github.com/TraceFold/tracefold/releases/download/brand-assets/banner.png" alt="tracefold" width="900"></a>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=20&pause=1200&color=00DFD8&background=0B0A0900&center=true&vCenter=true&width=650&lines=Autonomous+AI+Agent+Reversibility+Substrate;Holding+the+Checked+Inverse+Before+Actions+Land;Tamper-Evident+Receipts+Verifiable+Offline" alt="TraceFold Tagline" />

<p>
<a href="https://github.com/TraceFold/tracefold"><img src="https://img.shields.io/badge/Repository-TraceFold%2Ftracefold-7928ca?style=for-the-badge&logo=github&logoColor=ffffff" alt="TraceFold Repo"></a>
<a href="https://tracefold.github.io/tracefold/verify.html"><img src="https://img.shields.io/badge/Verifier-Zero%20Network%20WASM-00dfd8?style=for-the-badge&logo=webassembly&logoColor=090a0f" alt="Browser Verifier"></a>
<a href="https://www.npmjs.com/package/@mahirhir/tracefold"><img src="https://img.shields.io/badge/npm-SDK%20v0.1-0070f3?style=for-the-badge&logo=npm&logoColor=ffffff" alt="npm SDK"></a>
<a href="https://discord.gg/rtvXqYEQzr"><img src="https://img.shields.io/badge/Community-Discord-5865F2?style=for-the-badge&logo=discord&logoColor=ffffff" alt="Discord"></a>
</p>

</div>

---

### The Paradigm Shift: Pre-Fact Provenance

| Dimension | Traditional Post-Hoc Audit Logs | TraceFold Pre-Fact Provenance |
| :--- | :--- | :--- |
| **Execution Order** | Action executes first $
ightarrow$ Logged afterwards | Inverse constructed & checked $
ightarrow$ **Action lands** |
| **Irreversible Damage** | Discovered only after system corruption | **Blocked at the gate**; escalates to human approval |
| **Verification Trust** | Must trust the host/server that produced the log | **Zero-trust offline verification** via standalone WASM |
| **Verdict Precision** | Binary (Pass/Fail) conflates errors with attacks | **Tri-state**: `Verified`, `Refuted`, `Unknown/Unparseable` |

---

### Ecosystem Architecture

<table width="100%">
<tr>
<td width="50%" valign="top">
<h4>⚡ <a href="https://github.com/TraceFold/tracefold">TraceFold Core Engine</a></h4>
<p>Rust runtime substrate, state containment gate, and CLI.</p>
<code>cargo build --workspace</code>
</td>
<td width="50%" valign="top">
<h4>📦 <a href="https://www.npmjs.com/package/@mahirhir/tracefold">TypeScript / WASM SDK</a></h4>
<p>Offline receipt verifier package. Zero network calls, browser & Node.js ready.</p>
<code>npm i @mahirhir/tracefold</code>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<h4>🖥️ <a href="https://github.com/TraceFold/tracefold/tree/main/gui">The Window (GUI)</a></h4>
<p>Local-first visual inspector over execution traces, checkpoints, and receipts.</p>
</td>
<td width="50%" valign="top">
<h4>📐 <a href="https://github.com/TraceFold/tracefold/tree/main/lean">Lean 4 Formal Specifications</a></h4>
<p>117 machine-checked theorems certifying algebraic reversibility and boundaries.</p>
</td>
</tr>
</table>

---

### Security Invariants

1. **Deterministic Approval Gate**: If a verified inverse cannot be constructed before execution, the agent stops immediately and escalates to human approval.
2. **Air-Gapped Offline Verification**: Verification executes entirely in-process or in-browser (WASM) with 0 network calls.
3. **Tri-State Verdict Architecture**: Explicitly outputs `Verified`, `Refuted`, or `Unknown/Unparseable` so parsing errors are never mislabeled as fraud.

---

<div align="center">
<sub>Built by <a href="https://glovrex.com">Glovrex</a> &middot; Licensed under Apache-2.0</sub>
</div>
