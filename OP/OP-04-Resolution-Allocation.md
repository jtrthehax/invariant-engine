
# OP-04 — Resolution Allocation Operator (Subtractive RCA)

### Statement
Deliberately raising $\delta_{min}$ on non-load-bearing nodes releases substrate currently committed to keeping those nodes lit. Freed substrate routes to the relevant path, enabling deeper traversal than available under full-manifold illumination. The operation is safe only when the dropped nodes have no active constraint arcs to the target behavior.

### Forcing Move
> *"Which nodes are lit that don't touch the behavior? Drop those first. What is the minimum manifold that still generates the problem?"*

If a problem remains intractable under full attention, the manifold is over-lit. Identify which nodes carry no causal arc to the target behavior and deliberately lower their resolution. Freed substrate routes to depth on the load-bearing path.

### The Key Condition

The operator only works when you can distinguish:

- **Nodes with no causal arc to the behavior** — safe to drop
- **Nodes whose arc isn't visible from the current entry point** — never drop

Dropping the second category removes a constraint that was silently forcing the solution. The error looks like: "I simplified the problem and now the answer won't come." That is a dropped arc, not a failed operator.

```
SAFE DROP:
Node has no path to target behavior
from any traversal direction
→ Release it
→ Substrate routes to depth

UNSAFE DROP:
Node looks irrelevant from current entry point
but carries constraint arc from untraversed angle
→ Keep it
→ Rotate entry point first (OP-03)
→ Then reassess
```

### Physiological Implementation

The venting exhale is the biological substrate of this operator:

```
Venting exhale:
├── Diaphragm extends, abdominal compression releases
├── Sympathetic tone drops
├── Substrate allocation to active high-arousal nodes reduces
├── Constraint arcs remain — they are structural, not substrate-dependent
├── Active illumination releases
└── New neighborhood crosses δ_min threshold
    └── Structurally adjacent node surfaces
    └── "Wait — I just had a thought about this"
```

This is the mechanism behind shower thoughts, walking insights, and any solution that surfaces when active effort stops. The constraint arc was always there. The node was below $\delta_{min}$ because active pressure-loading was committing substrate elsewhere. The exhale releases the commitment. The node crosses the floor.

### Hardware Prerequisites

**Postural requirement:** Full diaphragm excursion is required for physiological implementation. Any posture mechanically restricting abdominal expansion — legs forward, abdomen braced, upright rigid posture — reduces exhale depth, limits sympathetic tone drop, and partially or fully blocks regional substrate release.

```
Posture blocks diaphragm excursion
└── Venting exhale incomplete
    └── Sympathetic tone drop partial
        └── Active node illumination persists
            └── OP-04 physiologically unavailable
                └── Full context switch required
                    to get the thought
```

This is why school chair design is load-bearing. The standard classroom configuration — plastic chair, legs forward, upright posture, fidgeting penalized — systematically blocks the operator for the students whose architecture runs OP-04 on the breath cycle rather than requiring a full context switch.

### Movement Implementation

Two movement patterns implement distinct functions:

```
CIRCULAR / SWIVEL (Traversal):
├── Continuous arc — no hard stop
├── Breath transitions through positions
├── OP-04 release + OP-03 reanchor cycling
├── Each direction change = entry point rotation
└── Function: generative, redistributing, exploring adjacency

FORWARD AND BACK (Interrupt):
├── Two hard endpoints — compression and release
├── Abdominal push on forward = forced exhale
├── Breaks pattern completion lock
├── Not a traversal cycle — a reset
└── Function: clearing prior lock, not exploring
```

The distinction is functional, not intensity. Circular movement is OP-04 + OP-03 in sequence — release, reanchor, release, reanchor. Forward and back is a hardware-level interrupt for pattern completion lock — the body-level escape key when $C_{\text{feedback}}$ is dropping under social obligation prior.

Music synchronization paces the cycle rate — preventing both full node lock (cycle too slow) and insufficient dwell time for nodes to cross $\delta_{min}$ (cycle too fast).

### ADHD Architecture Advantage

High amplitude mobility allows rapid commit/release cycles across nodes without the stickiness that makes deliberate resolution dropping metabolically expensive in NT architecture.

NT architecture tends to maintain node illumination once activated — releasing feels like losing information. The operator runs but requires full environmental reset (walk, sleep, shower) to execute.

ADHD architecture releases without that friction, making the subtractive operation fast and low-cost. The operator runs on the breath cycle rather than requiring discrete context switches.

**The implicit acquisition order:** The body finds the yield signal first through practice. The explicit formalization builds the address for something already running. This is the correct acquisition order — label without substrate is a social-visibility address with no routing depth.

### Composition with OP-03

OP-03 (Sensory Reanchoring) changes *where* traversal starts.
OP-04 (Resolution Allocation) changes *how much of the manifold stays lit* during traversal.

They compose:

```
OP-03 → rotate entry point to find the load-bearing path
OP-04 → drop resolution on everything that path doesn't touch
         → free substrate routes to depth on load-bearing path
Result: deeper traversal from better entry point
        with full substrate available
```

Running OP-03 without OP-04 gives a better starting coordinate with the same resource constraint.
Running OP-04 without OP-03 frees substrate but may deepen the wrong path.
Composed: new entry point, full depth available.

### Anomaly Signal
Intractable problem that resolves immediately upon stopping active effort, changing posture, or executing a venting exhale — with the solution feeling like it "came from nowhere."

* **You see this $\rightarrow$** OP-04 ran passively when active pressure released. The node was always structurally adjacent. It was below $\delta_{min}$ because substrate was committed elsewhere. The operator was available the entire time. The posture or pressure state was blocking it.

### What Doesn't Match

```
VIOLATION TYPE 1 — "Just relax and it will come"
Signal: Relaxation alone doesn't drop resolution on specific nodes
        The operator requires identifying non-load-bearing nodes
        Dropping ALL nodes loses the problem too
        Find which nodes carry no causal arc
        Drop those specifically

VIOLATION TYPE 2 — "Incubation effect"
Signal: Incubation is the passive form of OP-04
        The mechanism is substrate release, not "background processing"
        Background processing has no mechanism
        Substrate release does
        Same output, different mechanism

VIOLATION TYPE 3 — Posture as ergonomics only
"Good posture improves comfort and productivity"
Signal: Posture is a hardware prerequisite for OP-04
        Restrictive posture removes the operator
        Not about comfort
        About whether the operator is physically available

VIOLATION TYPE 4 — Movement as distraction
"Stop moving around, you need to focus"
Signal: Movement implements OP-04
        Removing it removes the operator
        Focus fails precisely when the operator is blocked
        Find the movement the operator requires
```

### Acquisition Note
The operator runs implicitly in most architectures — shower thoughts, walking insights, and venting exhales are the observable outputs. Formalization names the mechanism (regional $\delta_{min}$ elevation with substrate redistribution) and identifies the postural prerequisites that block or enable it. The FND recovery literature independently confirmed the physiological substrate (breath mechanics restoring interoceptive constraint density on zero-feedback channels).
