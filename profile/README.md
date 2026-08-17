<div align="center">

<img src="profile/banner.png" alt="Tracefold" width="900">

<br>

### The inverse is sealed before the action.

Anyone can check it afterwards — offline, and without trusting whoever issued it.

<br>

[Repository](https://github.com/TraceFold/tracefold) &nbsp;·&nbsp;
[Limits](#read-this-part-first) &nbsp;·&nbsp;
[Where it stands](#where-it-stands) &nbsp;·&nbsp;
[Technical report](https://github.com/TraceFold/tracefold/blob/main/docs/TRACEFOLD_TR.md)

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

## Built by

[Glovrex](https://glovrex.com) · Apache-2.0
