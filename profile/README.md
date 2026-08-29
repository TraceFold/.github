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

### Ecosystem Components

<table width="100%">
<tr>
<td width="50%" valign="top">
<h4>⚡ <a href="https://github.com/TraceFold/tracefold">TraceFold Core Engine</a></h4>
<p>Runtime substrate in Rust. Enforces deterministic approval gates, inverse construction, and CLI tools.</p>
<code>cargo build --workspace</code>
</td>
<td width="50%" valign="top">
<h4>📦 <a href="https://www.npmjs.com/package/@mahirhir/tracefold">@mahirhir/tracefold (npm SDK)</a></h4>
<p>Standalone TypeScript / WebAssembly offline receipt verifier. Published under Apache-2.0 on npm.</p>
<code>npm i @mahirhir/tracefold</code>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<h4>🖥️ <a href="https://github.com/TraceFold/tracefold/tree/main/gui">The Window (GUI)</a></h4>
<p>Local-first visual inspector over execution traces, state checkpoints, and inclusion receipts.</p>
</td>
<td width="50%" valign="top">
<h4>📐 <a href="https://github.com/TraceFold/tracefold/tree/main/lean">Lean 4 Formal Specifications</a></h4>
<p>117 machine-checked algebraic theorems proving effect containment with 0 <code>sorry</code> assertions.</p>
</td>
</tr>
</table>

---

### Security Invariants

1. **Deterministic Approval Gate**: If a verified inverse cannot be constructed before execution, the agent stops immediately and escalates to human approval.
2. **Air-Gapped Offline Verification**: Verification executes entirely in-process or in-browser (WASM) with 0 network calls.
3. **Tri-State Verdict Architecture**: Explicitly outputs `Verified`, `Refuted`, or `Unknown/Unparseable` so parsing errors are never mislabeled as fraud.

---

### Resources

- **Core Repository**: [`TraceFold/tracefold`](https://github.com/TraceFold/tracefold) &mdash; Source code, architecture, and issue tracker.
- **Interactive Browser Verifier**: [`tracefold.github.io/tracefold/verify.html`](https://tracefold.github.io/tracefold/verify.html) &mdash; Zero-network in-tab WASM receipt verification.
- **Formal Technical Report**: [`docs/TRACEFOLD_TR.md`](https://github.com/TraceFold/tracefold/blob/main/docs/TRACEFOLD_TR.md) &mdash; Complete mathematical derivations and error taxonomies.
- **Community Discord**: [`discord.gg/rtvXqYEQzr`](https://discord.gg/rtvXqYEQzr) &mdash; Discussion, agent security sparring, and releases.

---

<div align="center">
<sub>Built by <a href="https://glovrex.com">Glovrex</a> &middot; Licensed under Apache-2.0</sub>
</div>
