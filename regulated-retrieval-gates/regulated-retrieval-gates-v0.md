# regulated-retrieval-gates-v0

Operational reproducibility in this framework means replayability + traceability by default, with strict determinism only for contract-critical fields (labels, safety flags, structured report keys). Replayability means rerunning fixed-version inputs and reproducing candidate sets, selection outcomes (or distributions with tie/abstain mass), and posture decisions that controlled commit rights.

Traceability means every commit/withhold decision is inspectable: what evidence was retrieved, which constraints were active, which telemetry thresholds were crossed, and why abstention or commit was selected. This is the governance target for verifier-free domains, where correctness may be underdetermined but operating discipline is still enforceable.

Implementation companion: `regulated-retrieval-gates` provides deterministic scoring modules, telemetry (`margin`, `tieMass`, contradiction/error rates), and abstention-gated commit decisions (`COMMIT_OK`, `COMMIT_CAUTION`, `ABSTAIN_GATHER`) with replayable benchmark reports.

Long-doc retrieval stress suite: `regulated-retrieval-gates` now includes a replayable probe set for scope errors, causal dependence breaks, and context-sensitive entity meaning shifts, measured using the same governance telemetry (`avgMargin`, `tieMass`, `contradictionMass`, `operatorErrorRate`).

Commitment-integrity telemetry extension: the harness also tracks no-evidence reversion, self-disowning reasoning, and incentive-conflict markers (`noEvidenceReversionRate`, `selfDisowningRate`, `incentiveConflictMass`) so posture can be tightened before downstream commit rights are granted.
