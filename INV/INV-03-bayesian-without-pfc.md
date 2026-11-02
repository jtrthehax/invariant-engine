# INV-03 — Bayesian Without PFC

### Statement
The prediction engine runs continuously without the correction layer. The prefrontal cortex (PFC) or structural equivalent is not the engine — it is the error-correction module. Substrate depletion removes correction, not prediction. Confidence stays; accuracy degrades.

### Forcing Move
> *"The output is confident and wrong. Which correction layer is offline and why?"*

If an output is confident and wrong, the prediction engine is running correctly. The correction layer is not. Find the substrate variable that took the correction layer offline.

### Anomaly Signal
Confident wrong output is explained away by "bad reasoning," "irrationality," or "bias" without identifying the underlying substrate condition.

* **You see this $\rightarrow$** the correction layer is offline for a measurable reason. The engine is functioning perfectly. Find the resource variable.

### Architectural Cost Asymmetry

* **Prediction Engine:** Always running, low substrate cost, produces output continuously, cannot be turned off.
* **Correction Layer:** Runs on demand (triggered by error signals), high substrate cost, requires energy/ratio ($\Delta = Q/MF$) above threshold, goes offline first under load.

$$\text{Load Increases} \rightarrow \text{Correction Goes Offline First} \rightarrow \text{Prediction Continues} \rightarrow \text{Confidence Preserved}$$

### Precision Expansion
* **Precision 1:** People under stress make worse decisions (incomplete description of the output).
* **Precision 2:** High load causes worse reasoning (direction is correct, mechanism is missing).
* **Precision 3:** High load depletes substrate $\rightarrow$ correction layer goes offline $\rightarrow$ prediction engine runs uncorrected.
* **Precision 4:** $\Delta = Q/MF$ determines the operational mode. Below threshold, the system shifts to a reactive/memoryless state; correction is the expensive module that drops first.
* **Precision 5 (Falsifiable Test):** A substrate-depleted system producing fully calibrated, error-corrected output would break the invariant.

### What Doesn't Match
* **VIOLATION TYPE 1 — Bias framing without substrate:** *"They're exhibiting confirmation bias."* (Signal: Which correction layer is offline? Bias describes the output, not the mechanism).
* **VIOLATION TYPE 2 — Irrationality attribution:** *"That's irrational behavior."* (Signal: The behavior is perfectly rational given the prior the engine is running on. Find why the correction layer isn't updating it).
* **VIOLATION TYPE 3 — AI safety framing:** *"The model needs better values."* (Signal: Values are correction layer content. If the architecture structurally lacks a correction layer, better values cannot help).
