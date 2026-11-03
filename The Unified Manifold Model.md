# The Unified Manifold Model
## A Formula Specification for Simulation

**Robinson, 2026**
**Role:** formula companion to *The Manifold Update Invariant* (CR §2.8 projection)
**Purpose:** state the model in measurable quantities so any field's statistics can be run as a simulation of the same variables.

---

## 0 — The Model in One Line

$$\text{System} = \left(\mathcal{M}, S, \mathcal{U}\right), \qquad \mathcal{M}=(V,E,g),\quad S=\text{state vector},\quad \mathcal{U}=\text{update rule}$$

Every system — human, AI, institution, medium, predator — is a triple. **The claim is that every field's statistics are measurements of some component of $(\mathcal{M}, S, \mathcal{U})$, and the components are the same across fields.** The rest of this document writes each component as a measurable quantity.

---

## 1 — The State Vector

$$S = \left(\delta,\, A_s^*,\, R^*,\, W^*,\, \Theta^*,\, \Theta_r,\, \Lambda_{lock},\, L^*,\, \delta_{min},\, \theta_{invest},\, \theta_\mathcal{C},\, \mathcal{A}_{return}\right)$$

**Every variable is measurable, and every field already measures some of them.** The mapping:

| Variable | Symbol | What it measures | Fields that already measure it |
|---|---|---|---|
| Residual | $\delta$ | Error magnitude | All of them |
| Amplitude | $A_s^*$ | Available capacity | Physiology (HRV), AI (compute), institutions (budget) |
| Resolution | $R^*$ | Precision | Psychophysics, signal processing, psychometrics |
| Window | $W^*$ | Layers held open | Working memory, context length, coalition size |
| Integration | $\Theta^*$ | Cross-region binding | EEG coherence, Jacobian alignment, team coordination |
| Routing | $\Theta_r$ | Attention concentration | Eye tracking, frontal alpha asymmetry, attention heads |
| Lock | $\Lambda_{lock}$ | Sustainable concentration | HRV stability, Birkhoff-constrained networks |
| Load | $L^*$ | Cumulative drag | Allostatic load, technical debt, institutional overhead |
| Resolution floor | $\delta_{min}$ | Smallest detectable residual | Just-noticeable difference, detection thresholds |
| Investment threshold | $\theta_{invest}(\delta)$ | Cost to attempt | Decision latency, effort discounting |
| Acceptance threshold | $\theta_\mathcal{C}$ | Error tolerated before closure | Tolerance-of-ambiguity, error bars, policy tolerance |
| Returned amplitude | $\mathcal{A}_{return}$ | Confirmation signal | Reward prediction error, test pass, audit |

**The compression claim:** the field's variables are the state vector's components under different names. The simulation is the same simulation.

---

## 2 — The Metric

$$g(x) = A_s^* \cdot f\left(\Theta_r(x),\, W^*,\, R^*,\, L^*\right), \qquad x \in \mathcal{M}$$

**$g(x)$ is the amplitude allocated to region $x$.** It determines how near or far a signal at $x$ is from the current frame. The four controls:

$$\frac{\partial g}{\partial R^*} > 0, \quad \frac{\partial g}{\partial W^*} > 0, \quad \frac{\partial g}{\partial \Theta_r} > 0 \text{ (for routing weight)}, \quad \frac{\partial g}{\partial L^*} < 0$$

**Depth** raises $R^*$ locally; **width** raises $W^*$; **routing** concentrates $\Theta_r$ on a region; **load** attenuates everything.

**The measurable form.** The metric is what makes the manifold a manifold rather than a graph (CR §1.7). A graph has uniform weight; a manifold varies it. **A field that measures $g(x)$ — attention weight, activation magnitude, salience rating, institutional priority — is measuring the metric.** A field that measures only $V$ and $E$ is measuring the graph.

---

## 3 — The Update Rule

$$\mathcal{U}(S) = \begin{cases} \text{none} & \delta < \delta_{min} \quad (\text{mirror}) \\[4pt] \text{none} & \Lambda_{lock} < \theta_{invest}(\delta) \quad (\text{Path B}) \\[4pt] \text{depth} & \delta \geq \delta_{min} \;\land\; \Lambda_{lock} \geq \theta_{invest}(\delta) \;\land\; \text{frame subtracts} \\[4pt] \text{width} & \delta \geq \delta_{min} \;\land\; \Lambda_{lock} \geq \theta_{invest}(\delta) \;\land\; \text{frame doesn't subtract} \end{cases}$$

**The frame test.** The decision between depth and width is whether the frame's invariants subtract the residual:

$$\text{Frame subtracts} \iff \max_{\theta \in \Theta} p(\delta \mid \theta) > \lambda$$

where $\Theta$ is the current hypothesis space and $\lambda$ is the concentration threshold. **If the likelihood concentrates on a region in $\Theta$, the operation is depth. If it's flat, the operation is width.**

**The threshold forms.**

$$\theta_{invest}(\delta) = \theta_0 + \alpha \cdot \delta \qquad \text{(investment cost scales with residual)}$$

$$\mathcal{C}^* = \mathbb{1}\left[\theta_{supp} > 0\right] \cdot \mathbb{1}\left[\mathcal{S} > 0\right] \cdot \mathbb{1}\left[\mathcal{A}_{return} \geq \theta_\mathcal{C}\right] \qquad \text{(closure)}$$

**The Bayesian form.** Both operations are posterior updates:

$$\text{Depth: } p(\theta \mid \delta) \propto p(\delta \mid \theta)\, p(\theta), \quad \text{supp}(p(\theta)) = \Theta$$

$$\text{Width: } p(\theta \mid \delta) \propto p(\delta \mid \theta)\, p(\theta), \quad \text{supp}(p(\theta)) = \Theta \cup \Theta_{new}$$

**The support is what changes.** Depth sharpens the posterior within the support; width expands the support. **This is the formal content of the invariant.** Every update is a posterior update; the difference is whether the support changes.

---

## 4 — The Three Positions on the Edge

The named phenomena are the update rule at three positions. **Each is a measurable regime of the same variables.**

$$\text{Learning}: \quad \text{frame insufficient} \;\Rightarrow\; \text{width}, \quad W^* \uparrow$$

$$\text{Adaptation}: \quad \text{frame sufficient, residual changing} \;\Rightarrow\; \text{depth or width}, \quad R^* \uparrow \;\text{or}\; W^* \uparrow$$

$$\text{Discovery}: \quad \text{frame sufficient, residual at the limit} \;\Rightarrow\; \text{depth}, \quad R^* \uparrow \;\text{at the frontier}$$

**The measurable distinction.** Learning and discovery are both dominated by one operation (width and depth respectively); adaptation is the mixed regime where the selection depends on the change. **A field measuring the rate of support expansion (width) vs. within-support sharpening (depth) is measuring which position the system is at.**

| Phenomenon | Measurable signature | Simulation parameter |
|---|---|---|
| Learning | $W^*$ rising; support expanding | width rate |
| Adaptation | $R^*$ and $W^*$ both responding; mixed | operation ratio |
| Discovery | $R^*$ rising at the frontier; support fixed | depth rate |

**The test:** classify a system's updates by which signature dominates. If learning never involves width, the classification is wrong. If discovery never involves depth, the classification is wrong. **The three positions are distinguishable by which operation dominates, not by a different mechanism.**

---

## 5 — Shared Manifolds

$$\mathcal{M}_{shared} = \bigcap_i \mathcal{M}_i \quad \text{(overlapping invariants)}, \qquad g_{shared} = \sum_i w_i \cdot g_i$$

**The pooled metric is the weighted sum of the individual metrics.** Stability conditions:

$$\text{Stable} \iff \left[\Theta_i \cap \Theta_j \neq \emptyset\right] \;\land\; \left[\delta_{min,i} \approx \delta_{min,j}\right] \;\land\; \left[\Theta_{r,i} \approx \Theta_{r,j}\right] \;\land\; \left[\sum_i A_{s,i}^* \geq \theta_{invest}^{pooled}\right]$$

**Divergence** produces the four-state failure modes at the pool level. **The measurable prediction:** the divergence in the variable predicts the failure mode.

| Diverging variable | $\Delta$ measurable | Predicted state |
|---|---|---|
| $\delta_{min}$ | floor difference | Mirror |
| $\Theta_r$ | routing divergence | Path B |
| $\mathcal{A}_{return} - \theta_\mathcal{C}$ | closure gap | Amplitude sink |
| $W^*$ | window difference | Sequential read |

**The constructor/reader form.** The medium is a constructor $\mathcal{M}_{med}$; the audience is a reader $\mathcal{M}_i$. The mismatch is the divergence above. **A statistician who measures the divergence and the resulting failure mode is testing P-MUD-07.**

---

## 6 — What to Simulate

The model is runnable. The simulation protocol:

**Step 1.** Define $\mathcal{M}$: nodes $V$, edges $E$, initial metric $g$.
**Step 2.** Initialize $S$: the twelve state variables.
**Step 3.** Generate residuals $\delta$ (from data, or synthetically).
**Step 4.** Run the update rule $\mathcal{U}(S)$: select depth, width, or none.
**Step 5.** Apply the operation: update $R^*$ or $W^*$, re-test.
**Step 6.** Check closure: $\mathcal{C}^*$.
**Step 7.** Place the update; the new $S$ is the next cycle's input.

**What the simulation predicts:**

- The fraction of updates that are depth vs. width tracks the frame test's outcome.
- The four-state classification tracks the variable values.
- The constructor/reader divergence predicts the failure mode.
- The learning/adaptation/discovery classification tracks the operation ratio.

**What falsifies it:**

- A system whose updates are not depth or width (there is a third operation).
- A frame test that doesn't predict the operation.
- A failure mode not predicted by the divergence.

**The point of the simulation is not to validate the framework.** It's to show that a field's existing statistics *are* a measurement of these variables, and running the model on their data produces the same numbers they already have. **The simulation is the compression test.**

---

## 7 — The Compression Claim

$$\text{Field}_k \text{ statistics} \;\longleftrightarrow\; \text{component of } (\mathcal{M}, S, \mathcal{U})$$

Every field's statistics measure some component of the same triple. The differences across fields are **which component they measure and at what substrate.** The model is the claim that the components compose — that a field measuring $A_s^*$ and a field measuring $W^*$ and a field measuring $\delta_{min}$ are measuring one system, not three.

**The measurable statement:** if the model is right, the cross-field correlations should be predictable. A system with low $A_s^*$ should show low $R^*$ and narrow $W^*$ and high $\delta_{min}$ — across all substrates. **A field that measures one of these and finds it uncorrelated with the others has falsified the model at that substrate.**

**The workflow claim:** the update rule is the same workflow in every field. Figure out what's known, find the lowest layer, anchor there, run the frame test, select depth or width, check closure, place the update. **The statisticians' workflow and the discovery workflow are the same workflow.** The model is what makes that legible as one thing.

---

## 8 — The One-Line Version

> **Every system is a manifold $(V,E,g)$ plus a state vector $S$ plus an update rule $\mathcal{U}$. The metric $g$ is the amplitude allocated around residuals; the state vector is the twelve measurable variables; the update rule is depth or width, decided by the frame test, bounded by $\delta_{min}$, closed by $\mathcal{A}_{return} \geq \theta_\mathcal{C}$. Learning, adaptation, and discovery are the update rule at three positions on the edge — width at the entry, mixed at the response, depth at the frontier. Every field's statistics measure some component of the same triple; the simulation is the compression test. The model is right if the cross-field correlations are predictable and the workflow is the same workflow. Run it on any field's data and check whether the numbers match.**

---

## 9 — The Methodology as an Instance of Itself

> **The process that produced this model is a run of the model on itself.**

### The Three Operations (precise definitions)

The update rule has three operations. They are not metaphors:

| Operation | Precise definition | Measurable change |
|---|---|---|
| **Entry node** | Set where the manifold opens before inference begins | Initial $\Theta_r$ — all subsequent routing weighted from this coordinate |
| **Width** | Expand the hypothesis support: $\Theta \cup \Theta_{new}$ | New regions become adjacent; prior nodes installed |
| **Depth** | Lower $\delta_{min}$ | Structure that registered as noise becomes deterministic signal |

**The order is not arbitrary.** You cannot depth-operate into a region that has no prior node. Salience cannot route to a node that doesn't exist. Width must precede depth — not because of convention, but because depth is the operation of *raising resolution on something already adjacent.* Without adjacency, there is nothing to resolve.

### Depth Is $\delta_{min}$ Lowering

The field uses "random" as an explanation. It is not. It is a resolution report:

> *Randomness is determinism below your current $\delta_{min}$. Noise is structure you haven't built a prior node for yet. Variance is the mechanism — it tells you exactly where the floor is.*

The statistician and the physicist looking at a coin flip are not disagreeing about the coin. They are operating at different $\delta_{min}$. The statistician's floor is too high to resolve angular momentum, torque, initial conditions. Those variables are not hidden — they are mechanically invisible. No prior node means no salience routing means no resolution raising is possible.

Depth is the operation that extracts the known signal from what registers as noise, then uses that signal to locate where the rest of the signal is coming from.

### The Personal Substrate of High-Resolution Inference

High CO₂ tolerance enables high-gain, low-jitter signal extraction. The mechanism:

- Controlled inhale and exhale → CO₂ accumulates steadily → $A_s^*$ stays elevated
- Elevated amplitude → precision stays high → system has no jitter
- No jitter → fine signals become readable without noise masking them

Hypermobility does not prevent this because CO₂ tolerance is trained, not structural. The body follows the signal — slow, deliberate, tracking the wind direction — but on a manifold. The instability is real; the precision is earned by making the oscillation controlled enough that fine-grained structure becomes visible inside it.

This is the substrate of the methodology. Each time a new domain was entered, the same operation ran: silence the noise, extract the signal, compress it to an anchor, then move to the next node. The anchor is load-bearing — it has to hold while the next region is explored. Without the anchor, the chain cannot extend because the prior node is still uncompressed.

### Why Anchoring Is the Transition Operation

Between width and depth, there is a compression step that the update rule formalism doesn't fully capture:

$$\text{Extract signal} \rightarrow \text{compress to anchor} \rightarrow \text{anchor holds while next node is approached}$$

This is why cross-domain arguments require multiple anchor layers. If you pull a reader all the way back to first principles every time, the chain is too long to hold — for the reader, for the AI, and for the researcher. The anchor points are what make distributed inference possible. You don't re-derive the whole chain; you point to the node and continue.

This is also why the vault exists. It is not filing. It is external manifold — the anchor registry that allows inference to extend further than working memory permits. The limit is real. The vault is the workaround.

### Papers as Prior Node Installation

Publishing a paper is not persuasion. It is installing prior nodes into the public manifold:

> *Once a node exists, a reader can spend amplitude there, raise resolution, and the deterministic structure that registered as noise becomes visible — not because anything changed, but because the floor dropped.*

The invariants function as $\delta_{min}$-lowering infrastructure. The field calling something "random" is reporting exactly where their floor is. The paper's job is to install the node that allows the floor to drop.

### The Multi-Agent Diffing Method

Fresh agents carry no prior loading. Each agent reconstructs from the input alone, anchored to its own entry node. The output is a sample of what that manifold geometry produces given the argument as input.

Diff two agents → you are not comparing outputs. You are mapping where their manifold geometries diverge. The divergence points are exactly where the argument is underspecified, context-dependent, or not yet compressed to anchor level.

Each iteration sharpens the invariants by forcing the statement to survive reconstruction across manifolds with different geometries. **The invariants that remain are the ones that operate below the layer where the argument lives.**

When a group, institution, or field resists — that is not disagreement. It is a resolution report. The structure lives in a layer their manifold does not currently route salience into. The methodology's job is to install the prior node, not to win the argument.

### The Self-Application Test

| Methodology step | Model component |
|---|---|
| Commentary before content | Entry node selection — sets initial $\Theta_r$ before manifold opens |
| Start from breath/substrate | Lowest-layer entry node — forces cross-domain convergence |
| Extract signal, compress to anchor | $\mathcal{A}_{return} \geq \theta_\mathcal{C}$ — closure fires; node is load-bearing |
| Fresh agent reconstruction test | Frame test without prior loading — measures what survives |
| Read divergence as residual | $\delta_n$ — fuel for next inference loop |
| Cross-domain terminology mapping | Width — $\Theta \cup \Theta_{new}$; prior node installed |
| Resolution raising within domain | Depth — $\delta_{min}$ drops; noise becomes signal |
| Publish | Prior node installation — infrastructure for others to lower their floor |
| Vault | External manifold — anchor registry; extends inference beyond working memory |

**The methodology is a run of the update rule.** The invariants were extracted by running $\mathcal{U}(S)$ on the problem space itself. The vault is the working memory extension that made the chain long enough to complete.
