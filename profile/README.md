<div align="center">

<img src="https://github.com/TraceFold/tracefold/releases/download/brand-assets/banner.png" alt="" width="900">

# tracefold

**Undo is a feature. Reversibility is a property.**

The inverse is sealed **before it lands**. Anyone can check it afterwards, offline, and
without trusting whoever issued it.

<p>
<a href="https://github.com/TraceFold/tracefold"><picture><source media="(prefers-color-scheme: dark)" srcset="https://img.shields.io/badge/repository-ece7da?style=for-the-badge&labelColor=ece7da&logo=github&logoColor=0b0a09"><img alt="repository" src="https://img.shields.io/badge/repository-0b0a09?style=for-the-badge&labelColor=0b0a09&logo=github&logoColor=ece7da"></picture></a>
<a href="https://github.com/TraceFold/tracefold/blob/main/docs/TRACEFOLD_TR.md"><picture><source media="(prefers-color-scheme: dark)" srcset="https://img.shields.io/badge/technical%20report-ece7da?style=for-the-badge&labelColor=ece7da"><img alt="technical report" src="https://img.shields.io/badge/technical%20report-0b0a09?style=for-the-badge&labelColor=0b0a09"></picture></a>
<a href="#read-this-part-first"><picture><source media="(prefers-color-scheme: dark)" srcset="https://img.shields.io/badge/the%20limits%20first-ece7da?style=for-the-badge&labelColor=ece7da"><img alt="the limits first" src="https://img.shields.io/badge/the%20limits%20first-0b0a09?style=for-the-badge&labelColor=0b0a09"></picture></a>
</p>

<p>
<a href="https://github.com/TraceFold/tracefold/blob/main/LICENSE"><img alt="license" src="https://img.shields.io/github/license/TraceFold/tracefold?style=flat-square&color=0b0a09&labelColor=0b0a09"></a>
<a href="https://github.com/TraceFold/tracefold/commits/main"><img alt="last commit" src="https://img.shields.io/github/last-commit/TraceFold/tracefold?style=flat-square&color=0b0a09&labelColor=0b0a09"></a>
<a href="https://github.com/TraceFold/tracefold"><img alt="language" src="https://img.shields.io/github/languages/top/TraceFold/tracefold?style=flat-square&color=0b0a09&labelColor=0b0a09"></a>
</p>

</div>

---

## Flip one byte, and the verifier says no

![Verify a receipt, flip one byte, verify again](https://github.com/TraceFold/tracefold/releases/download/demo-assets/tracefold-demo-10s.gif)

Three files on that terminal: a receipt, a signed checkpoint, a public key. No project
directory, no account, no network call. The receipt verifies and the command exits `0`. One
byte of its payload is flipped, `cmp -l` prints the single line proving exactly one byte
moved, and the same command exits `7`.

A real terminal captured against a fresh anonymous clone on 26 August 2026, nothing retyped.
The `cargo build --workspace` that precedes it, 64 seconds, is deliberately outside the
recording. [The repository](https://github.com/TraceFold/tracefold) has the commands to run
it yourself.

## Read this part first

Three classes of failure sit outside what this covers, **by declaration, not by oversight**.
Putting them here costs the first impression and saves you the afternoon you would otherwise
spend discovering them.

| out of scope | why it cannot be closed from inside |
|:--|:--|
| Root or kernel-privileged writes | They go around the tool entirely, and this build does not detect that |
| Writes into the tool's own state directory | A detector living in that directory cannot judge it. The defence is an artifact held elsewhere |
| A policy that encodes the wrong intent | It will be enforced faithfully. No amount of verification reaches the question of whether the rule was right |

Two more sit in the repository's own list, including the one that bounds the demonstration
above: exit `7` proves the receipt you hold is not the receipt that was signed, and says
nothing about whether the change it describes was wanted. The full list ships in the
repository, and a test fails if it drifts from the code that enforces it. The limits are not
prose someone remembered to update.

## Where it stands

| | measured | under what conditions |
|:--|--:|:--|
| Test floor | **2,602** | probes across 454 suites, plus the SDK's 36 passed, 0 failed, 7 skipped · fresh clone · one machine · single run · 25 August 2026. It has moved more than forty times in a month, because it moves with every repair round |
| Machine-checked | **117** | theorems in Lean, 12 of them counterexamples, `sorry` 0. One `axiom` carried rather than proved, and named in the report |
| Open holes | **0** | high severity, as of 25 August 2026, after forty-four adversarial rounds. It was 3, then 0, then 1, then 0 again inside one week, so read it as the state of an afternoon |
| Not measured | **3** | Windows native, OneDrive, SMB. Zero runs out of the three |

Numbers without the right-hand column are decoration. That column is why the table is wider
than it looks like it needs to be. Every figure here matches the repository README, and the
commands that produce them are printed there rather than described.

**Not released.** The names on crates.io and npm are reservations holding the name, and
installing either gets you nothing. What runs today is a build from source.

## What is deliberately absent

No build badge, because continuous integration is switched off and a green tick would be a
lie. No download counts and no star totals, because neither measures whether the thing works.
No package version badges, because the packages behind them are empty placeholders and a
version number would read as a release. Every figure above can be re-derived from the
repository by someone who does not trust us.

## Built by

[Glovrex](https://glovrex.com)
