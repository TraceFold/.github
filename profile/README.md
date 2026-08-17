<div align="center">

<img src="https://github.com/TraceFold/tracefold/releases/download/brand-assets/banner.png" alt="" width="900">

# tracefold

**Undo is a feature. Reversibility is a property.**

The inverse is sealed **before it lands**. Anyone can check it afterwards — offline,
and without trusting whoever issued it.

<p>
<a href="https://github.com/TraceFold/tracefold"><picture><source media="(prefers-color-scheme: dark)" srcset="https://img.shields.io/badge/repository-ece7da?style=for-the-badge&labelColor=ece7da&logo=github&logoColor=0b0a09"><img alt="repository" src="https://img.shields.io/badge/repository-0b0a09?style=for-the-badge&labelColor=0b0a09&logo=github&logoColor=ece7da"></picture></a>
<a href="https://github.com/TraceFold/tracefold/blob/main/docs/TRACEFOLD_TR.md"><picture><source media="(prefers-color-scheme: dark)" srcset="https://img.shields.io/badge/technical%20report-ece7da?style=for-the-badge&labelColor=ece7da"><img alt="technical report" src="https://img.shields.io/badge/technical%20report-0b0a09?style=for-the-badge&labelColor=0b0a09"></picture></a>
<a href="#read-this-part-first"><picture><source media="(prefers-color-scheme: dark)" srcset="https://img.shields.io/badge/the%20limits%20first-ece7da?style=for-the-badge&labelColor=ece7da"><img alt="the limits first" src="https://img.shields.io/badge/the%20limits%20first-0b0a09?style=for-the-badge&labelColor=0b0a09"></picture></a>
</p>

<p>
<img alt="license" src="https://img.shields.io/github/license/TraceFold/tracefold?style=flat-square&color=0b0a09&labelColor=0b0a09">
<img alt="last commit" src="https://img.shields.io/github/last-commit/TraceFold/tracefold?style=flat-square&color=0b0a09&labelColor=0b0a09">
<img alt="crates.io" src="https://img.shields.io/crates/v/tracefold?style=flat-square&color=0b0a09&labelColor=0b0a09&logo=rust&logoColor=ece7da">
<img alt="npm" src="https://img.shields.io/npm/v/tracefold?style=flat-square&color=0b0a09&labelColor=0b0a09&logo=npm&logoColor=ece7da">
</p>

</div>

---

## Read this part first

Three classes of failure sit outside what this covers — **by declaration, not by
oversight**. Putting them here costs the first impression and saves you the afternoon you
would otherwise spend discovering them.

| out of scope | why it cannot be closed from inside |
|:--|:--|
| Root or kernel-privileged writes | They go around the tool entirely, and this build does not detect that |
| Writes into the tool's own state directory | A detector living in that directory cannot judge it. The defence is an artifact held elsewhere |
| A policy that encodes the wrong intent | It will be enforced faithfully. No amount of verification reaches the question of whether the rule was right |

The full list ships in the repository, and a test fails if it drifts from the code that
enforces it. The limits are not prose someone remembered to update.

## Where it stands

| | measured | under what conditions |
|:--|--:|:--|
| Test floor | **1,770** | probes across 318 suites · fresh clone · one machine · single run |
| Machine-checked | **90** | theorems, 0 `sorry` · three axioms carried, not proved |
| Open holes | **3** | high severity · adversarial round 13 · repair in progress |
| Not measured | **3** | Windows native, OneDrive, SMB — zero runs |

Numbers without the right-hand column are decoration. That column is why the table is
wider than it looks like it needs to be.

## What is deliberately absent

No build badge — continuous integration is switched off, and a green tick would be a lie.
No download counts and no star totals, because neither measures whether the thing works.
Every figure above can be re-derived from the repository by someone who does not trust us.

## Built by

[Glovrex](https://glovrex.com) · Apache-2.0
