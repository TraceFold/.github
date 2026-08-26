<div align="center">

<a href="https://github.com/TraceFold/tracefold"><img src="https://github.com/TraceFold/tracefold/releases/download/brand-assets/banner.png" alt="tracefold" width="900"></a>

# tracefold

**It asks before the changes it can't put back.**

An agent's change is held with a checked inverse before it lands. When the inverse is in hand the
change goes through and nobody is asked. When one cannot be built, the agent stops and the question
goes to a person. Every verdict also becomes a receipt that verifies offline, without trusting
whoever issued it.

<p>
<a href="https://github.com/TraceFold/tracefold"><picture><source media="(prefers-color-scheme: dark)" srcset="https://img.shields.io/badge/repository-ece7da?style=for-the-badge&labelColor=ece7da&logo=github&logoColor=0b0a09"><img alt="repository" src="https://img.shields.io/badge/repository-0b0a09?style=for-the-badge&labelColor=0b0a09&logo=github&logoColor=ece7da"></picture></a>
<a href="https://github.com/TraceFold/tracefold/blob/main/docs/LIMITS.md"><picture><source media="(prefers-color-scheme: dark)" srcset="https://img.shields.io/badge/the%20limits%20first-ece7da?style=for-the-badge&labelColor=ece7da"><img alt="the limits first" src="https://img.shields.io/badge/the%20limits%20first-0b0a09?style=for-the-badge&labelColor=0b0a09"></picture></a>
</p>

</div>

---

## Check one yourself, with nothing installed

**[tracefold.github.io/tracefold/verify.html](https://tracefold.github.io/tracefold/verify.html)**

The engine's own verifier, compiled to WebAssembly and run inside your tab. It answers *verified*,
*refuted*, or *did not conclude*, and it will not report a file it merely could not read as a
forgery. Sample receipts are built in. No install, no account, and no server of ours involved.

## Not released

The names held on crates.io and npm are reservations. What runs today is a build from source, which
needs a Rust toolchain, and on Windows the documented path is WSL. The page above removes that cost
for checking a receipt, though it cannot produce one.

Test counts, theorems and open holes stay in the
[repository](https://github.com/TraceFold/tracefold), beside the commands that produce them and the
date each was taken.

## Built by

[Glovrex](https://glovrex.com)
