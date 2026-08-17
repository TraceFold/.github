<div align="center">

# tracefold

**The inverse is sealed before the action.**

Anyone can check it afterwards — offline, and without trusting whoever issued it.

[![repository](https://img.shields.io/badge/repository-0b0a09?style=for-the-badge&labelColor=0b0a09&logo=github&logoColor=ece7da)](https://github.com/TraceFold/tracefold)
[![rust](https://img.shields.io/badge/rust-0b0a09?style=for-the-badge&labelColor=0b0a09&logo=rust&logoColor=ece7da)](https://github.com/TraceFold/tracefold)
[![technical report](https://img.shields.io/badge/technical%20report-0b0a09?style=for-the-badge&labelColor=0b0a09)](https://github.com/TraceFold/tracefold/blob/main/docs/TRACEFOLD_TR.md)
[![the limits first](https://img.shields.io/badge/the%20limits%20first-0b0a09?style=for-the-badge&labelColor=0b0a09)](#read-this-part-first)

![github/license/TraceFold/tracefold](https://img.shields.io/github/license/TraceFold/tracefold?style=flat-square&color=0b0a09&labelColor=0b0a09)
![github/last-commit/TraceFold/tracefold](https://img.shields.io/github/last-commit/TraceFold/tracefold?style=flat-square&color=0b0a09&labelColor=0b0a09)
![crates/v/tracefold](https://img.shields.io/crates/v/tracefold?style=flat-square&color=0b0a09&labelColor=0b0a09&logo=rust&logoColor=ece7da)
![npm/v/tracefold](https://img.shields.io/npm/v/tracefold?style=flat-square&color=0b0a09&labelColor=0b0a09&logo=npm&logoColor=ece7da)

</div>

---

## Read this part first

Several classes of failure are outside what this covers **by declaration, not by
oversight**. Saying so here costs us the first impression and saves you the afternoon you
would otherwise spend finding out.

- An actor with root or kernel privilege can write around it, and this build does not
  detect that.
- An actor holding write access to the tool's own state directory cannot be caught by a
  detector living in that same directory. The defence there is an artifact held elsewhere.
- A policy that faithfully enforces the wrong intent will be faithfully enforced. That is
  structural, and no amount of verification reaches it.

The full list ships in the repository, and a test fails if it drifts from the code that
enforces it — the limits are not prose someone remembered to update.

## Where it stands

| | measured | under what conditions |
|:--|--:|:--|
| Test floor | **1,770** | probes across 318 suites, from a fresh clone, one machine, single run |
| Machine-checked | **90** | theorems, 0 `sorry`. Three axioms are carried, not proved |
| Open holes | **3** | high severity, adversarial round 13 — repair in progress |
| Not measured | **3** | Windows native, OneDrive, SMB — zero runs |

Numbers without the right-hand column are decoration. That column is why this table is
wider than it looks like it needs to be.

## What is deliberately not shown

No build badge: continuous integration is switched off, and a green tick would be a lie.
No download counts and no star totals, because neither measures whether the thing works.
Every figure above can be re-derived from the repository.

## Built by

[Glovrex](https://glovrex.com) · Apache-2.0
