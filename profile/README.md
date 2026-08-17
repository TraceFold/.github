# TraceFold

Home of **[tracefold](https://github.com/TraceFold/tracefold)**.

The inverse is sealed before the action, and anyone can check it offline.

## Read the limits first

Several classes of failure are out of scope **by declaration, not by oversight**: an actor
with root or kernel privilege, an actor holding write access to the tool's own state
directory, and a policy that faithfully enforces the wrong intent. The full list ships in
the repository and a test fails if it drifts from the code that enforces it.

## Where it stands

| | measured | under what conditions |
|---|--:|---|
| Test floor | 1,770 | probes across 318 suites, from a fresh clone, one machine, single run |
| Machine-checked | 90 | theorems, 0 `sorry`. Three axioms are carried, not proved |
| Open holes | 3 | high severity, adversarial round 13. Repair in progress |
| Not measured | 3 | Windows native, OneDrive, SMB — zero runs |

## Built by

[Glovrex](https://glovrex.com). Apache-2.0.
