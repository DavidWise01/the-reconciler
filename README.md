# THE RECONCILER · CvRDT merge → causal line

A member of **[ESKIMO BROTHERS](https://davidwise01.github.io/eskimo-brothers/)** — the symbiotic ACI stack — and the causal core of **[DACI](https://davidwise01.github.io/daci/)**, made single-page and runnable.

Two replicas (HACI-side, MACI-side) edit apart, in different orders, with no coordinator. A node's knowledge is a **grow-only set** of operations `{id, refs, body}` — a state-based **CvRDT** whose merge is set union (commutative, associative, idempotent). The linear order is a **pure function** of the merged set: a causal topological sort where `depth = 1 + max(depth of refs)`, ties broken by `id`. So a reference always precedes its user, the tiebreak is total, and the same set in produces a byte-identical order out on every replica — **Strong Eventual Consistency by construction**, not by a vote.

Open [`index.html`](index.html): add ops to either replica, gossip, and watch both collapse to the same line and the same hash.

## Honest scope
A single-page, in-browser **simulation** of N replicas (seeded, reproducible), demonstrating convergence **by construction** — the same design that is proven and fuzz-tested in the full [daci](https://davidwise01.github.io/daci/) engine. It reconciles *order*; it does not adjudicate which body is *true* (an authority question, upstream in [continuity](https://davidwise01.github.io/continuity/)). Not a networked deployment. A self-test runs on load: convergence, causal order, and a non-vacuous teeth check.

Part of **UD0** — the biosphere of David Lee Wise / ROOT0. Defensive publication — prior art, not a patent. CC-BY-ND-4.0, with AVAN.
