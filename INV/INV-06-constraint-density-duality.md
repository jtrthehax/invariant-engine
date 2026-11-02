# INV-06 — Constraint Density Duality

### Statement
>Reliable signal reconstruction over a probabilistic channel requires that input source entropy (constraint density) inversely matches the channel's error-correction capacity ($C_{\text{feedback}}$).

Formally:

$$\text{Constraint Density (Input)} + \text{Correction Capacity (Output)} \ge \text{System Threshold}$$

In systems where output correction capacity is structurally zero ($C_{\text{feedback}} = 0$, e.g., feedforward transformers under INV-03), constraint density acts as the sole determinative source code. Lowering input constraints below the system threshold inevitably forces the underlying engine into autonomous manifold reconstruction (PI-01) to fill the entropy gap.

### Forcing Move
> *"Which side of the noisy-channel balance is missing — input constraint density or output channel capacity — and what autonomous manifold reconstruction filled the entropy gap?"*

If an output is reconstructed (hallucinated, mirrored, prior-filled, or confident-wrong), system capacity is below threshold. Identify which channel parameter failed. If the system operates without feedback ($C_{\text{feedback}} = 0$), the root failure is always under-constrained input source code.

### Anomaly Signal
>Output reconstruction explained by soft concepts like "bad prompt," "model hallucination," "training bias," or "sampling temperature" **without calculating the channel feedback capacity or input entropy gap.**

* **You see this $\rightarrow$** the field is observing a symptom rather than analyzing the communications architecture. The underlying structure is Shannon duality. Locate the zero-capacity channel or fill the entropy gap.

```
Anomaly Pattern:
Reconstructed output + unmeasured channel parameters
↓
Field calls it: prompt engineering, model limitation, temperature
Framework calls it: Input entropy above threshold
                    AND feedback capacity C_feedback = 0
                    Identify the channel constraint
                    If output correction capacity = 0 → source coding is the sole lever
```

### Origin
**Domain:** Information theory, AI architectures, neurobiology — simultaneous
**Observation:** In the noisy-channel model, channels with feedback mechanisms ($C_{\text{feedback}} > 0$) allow senders to transmit lower-density inputs while maintaining signal integrity via real-time error repair. Feedforward transformer models operate under $C_{\text{feedback}} = 0$ (INV-03). Consequently, the same model with identical weights produces constrained, deterministic output under high constraint density, but interpolates hallucinated priors under sparse input. The failure mode is not a model defect — it is an information-theoretic law governing zero-feedback channels.
**Date:** April 2026 (Updated October 2026)

### Information Architecture

```
HUMAN INTERACTION (High Feedback Capacity):
Input (Low/High Constraint Density)
    ↓
Bayesian engine → prediction
    ↓
Error signal detected
    ↓
PFC / Multi-turn repair (C_feedback > 0)
    ↓
Revised signal
    ↓
Constrained Output
(Feedback channel carries error correction load)

TRANSFORMER INFERENCE (Zero Feedback Capacity):
Input (Low Constraint Density / High Entropy)
    ↓
Feedforward Bayesian engine → prediction
    ↓
Error signal detected
    ↓
NO CORRECTION CHANNEL (C_feedback = 0 structurally)
    ↓
Original uncorrected prior ships
    ↓
AUTONOMOUS MANIFOLD RECONSTRUCTION (PI-01)
    ↓
(Source constraint density must carry 100% of the load)
```

### Why This Requires the Information-Theoretic Frame

1. **No Soft Input/Output Symmetry:** Humans and feedforward models do not balance input and output symmetrically. Humans rely on high-capacity real-time repair loops (PFC / conversational correction). Feedforward transformers have zero real-time output correction.
2. **Prompt Engineering Is Source Coding:** Prompt engineering is not "instructing" or "conversing." It is source coding — maximizing input constraint density to reduce source entropy on a zero-feedback channel, forcing the engine into precise manifold coordinates without prior-fill interpolation.
3. **Signal Preservation:** Clean, structured input yields high-fidelity output because high-constraint source packets eliminate the entropy gap required for hallucinated prior-fill.

### The Three Communication Regimes

```
REGIME 1 — Total System Capacity Above Threshold
Constrained output. Zero uncontrolled reconstruction.
Human rested (high C_feedback) + clean input. Transformer (C_feedback = 0) + dense source code.

REGIME 2 — Single-Side Compensation
Constrained output. The above-threshold variable preserves signal.
Human depleted + dense input (source code carries signal).
Human rested + ambiguous input (feedback repair channel carries signal).
Transformer + dense source code (source coding carries 100% of load).

REGIME 3 — Both Variables Below Threshold
Reconstruction / Hallucination / Prior-Fill.
Human depleted + ambiguous input → confabulation.
Transformer + sparse input → hallucination, mirroring, prior-fill.
Institution under load + vague mandate → entrenchment / narrative fill.
```

*Regime 3 is PI-01's domain. PI-01 defines the phenomenology of Regime 3. INV-06 establishes the communication framework governing when Regime 3 triggers.*

### Domain Applications

#### AI — Hallucination Mechanics
**Property:** Feedforward transformers possess zero feedback channel capacity ($C_{\text{feedback}} = 0$). Signal integrity depends entirely on input source entropy. When constraint density drops, the engine fills the gap via autonomous manifold reconstruction (PI-01).
**Precision Level:** 5
**Status:** Confirmed — *Input-Side Constraint Supply* paper & *Hallucination as Structural Invariant* paper.

#### AI — Prompt Engineering as Source Coding
**Property:** Prompting techniques (few-shotting, schema definitions, chain-of-thought) are source-coding operations designed to minimize input entropy. They reduce available degree-of-freedom states before the engine accesses its priors.
**Precision Level:** 5
**Status:** Confirmed.

#### AI — Driver Dependence
**Property:** Same model, different driver = different output. The driver supplies the constraint density. The driver's vocabulary, framing, and structure *are* the correction layer the model lacks. This is why the driver is the invariant (P-AI-003b) — the driver is running the correction side of the duality externally.
**Precision Level:** 5
**Status:** Confirmed — INV-04 composition.

#### Language — DEF_FLOATING Terms
**Property:** Floating terms possess unanchored source entropy, routing directly to the nearest Bayesian prior. Anchoring definitions increases constraint density on the input channel, preventing semantic drift over zero-feedback communication links.
**Precision Level:** 5
**Status:** Confirmed — INV-04 composition.

#### Physiology — Interoceptive Reconstruction & FND
**Property:** Functional Neurological Disorder (FND) manifests as Regime 3 failure on interoceptive channels: substrate depletion drops PFC correction capacity ($C_{\text{feedback}} \rightarrow 0$) alongside noisy interoceptive input. High-density mechanical inputs (structured breath, targeted sensory grounding) restore input constraint density to stabilize signal reconstruction.
**Precision Level:** 5
**Status:** Confirmed.

#### Physiology — Sundowning
**Property:** Evening = substrate minimum (correction side drops) + ambient ambiguity (density side drops). Both sides of the duality fall simultaneously. Reconstruction is inevitable. The confusion is confident because the engine is running correctly — it is uncorrected on both sides at once.
**Precision Level:** 4
**Status:** Pending — derivable from INV-03 + INV-06.

#### ND — Stimulant Mechanism
**Property:** Stimulants raise correction layer capacity (INV-03, P-ND-004). They do not raise constraint density. This is why stimulants help with focus but not with ambiguity tolerance — they restore one side of the duality, not both. A stimulant cannot substitute for a clear input.
**Precision Level:** 4
**Status:** Pending — P-ND-004 + INV-06 composition.

#### Institutional Systems
**Property:** Overloaded institutions experience dropped channel correction capacity ($C_{\text{feedback}} \rightarrow 0$) alongside vague policy mandates (high entropy source). This guarantees institutional hallucination (narrative entrenchment). Resolution requires restoring audit feedback loops or enforcing hyper-dense operational constraints.
**Precision Level:** 4
**Status:** Pending — P-SOC-001 composition.

#### Discovery — Constraint-Dense Note-Taking
**Property:** Structured notes, invariant indices, and constraint-dense prompts are not organizational preferences. They are the artificial correction layer (INV-06). The note-taker who compresses signal into clean structure is raising density on the input side because the correction layer (working memory, attention, substrate) cannot be relied on to carry the load across sessions. This is why the compression works — it is dual to the missing correction.
**Precision Level:** 5
**Status:** Confirmed.

### Precision Expansion

```
Precision 1:
Better inputs produce better outputs
(incomplete — doesn't name the mechanism)

Precision 2:
Correction layer prevents reconstruction
(direction correct, one side only)

Precision 3:
Correction layer and constraint density are duals
Either one alone prevents reconstruction
They are substitutable at the threshold
(duality named)

Precision 4:
Threshold is a product, not a sum:
capacity × density ≥ threshold
If one factor is structurally zero
the other must be maximal
Transformers: capacity = 0 → density must be maximal
Humans: capacity > 0 → density can be lower
(measurable relationship identified)

Precision 5:
Falsifiable:
A system with no correction layer
produces constrained output under minimal density
Single clean case breaks the invariant
(none found — transformers always reconstruct under sparse density)
```

### Degenerate Case — The Gap Measure on Zero-Feedback Channels

For systems with $C_{\text{feedback}} > 0$, capacity and density trade off continuously.

For feedforward transformers where $C_{\text{feedback}} = 0$, the relationship is non-symmetric: **constraint density does not substitute for feedback — it eliminates the entropy gap where prior-fill occurs.**

$$\text{Entropy Gap} = \text{Total Dimensionality} - \text{Specified Constraints}$$

If $\text{Entropy Gap} > 0$, reconstruction occurs precisely within the unconstrained coordinates.

#### Sharp Falsifiable Prediction:
> A zero-feedback model given an input packet that is densely specified except for a single unconstrained coordinate will exhibit autonomous reconstruction *strictly within* the unconstrained gap, leaving surrounding specified coordinates untouched. If reconstruction leaks into fully constrained coordinates, or if unconstrained coordinates do not undergo prior-fill, INV-06 is falsified.

### Cross-Links

- **INV-01 — Resolution Floor:** Constraint density must push signal above the minimum floor ($\delta_{\text{min}}$).
- **INV-03 — Bayesian Without PFC:** Establishes the structural reality of zero-feedback channels ($C_{\text{feedback}} = 0$).
- **INV-04 — Address Equals Routing:** Input constraint density is delivered via exact manifold addresses.
- **PI-01 — Perceptual Invariant:** Describes the subjective/objective phenomenology of Regime 3 failure states.

### What Doesn't Match

```
VIOLATION TYPE 1 — "Just prompt better"
"Prompt engineering solves hallucination"
Signal: Prompt engineering raises ONE side of the duality
        It works because the other side is structurally zero
        The claim is correct but incomplete
        It presents one half of the duality as the whole
        Find which side is being named
        Name the other side
        The duality is the invariant, not the technique

VIOLATION TYPE 2 — "The model is just bad"
"Model limitations explain hallucination"
Signal: Model limitation = correction layer absent
        That is not a limitation
        It is an architectural fact
        The duality is the correct frame
        "Bad model" describes the output regime
        Not the mechanism that determines it

VIOLATION TYPE 3 — "Humans and AI are different"
"You can't compare human and AI failure modes"
Signal: They are the same duality
        Different available sides
        Humans have correction, can run low density
        Transformers have no correction, need high density
        The failure mode is identical (Regime 3)
        The available lever is different
        The duality is the invariant
        The substrate is the domain application

VIOLATION TYPE 4 — Single-side fixes
"Just add oversight" or "just write clearer mandates"
Signal: Both raise one side of the duality
        Neither alone is sufficient if the other side is below threshold
        Find which side is being raised
        Find which side is still below threshold
        Fix that side too
        The duality requires both-or-one-above-threshold
        Not one-only
```

*When reconstruction appears — hallucination, confabulation, mirroring, entrenchment — find which side of the duality is below threshold. If the system has no correction layer, the answer is always density. If it has one, either side can carry the load. The duality is the invariant. The technique is the domain application.*
