# regulated-agent-replay-suite-v0

Reference implementation (Replay Suite v0). To make the regulator spec operational, we maintain a small replayable CI gate that evaluates candidate agent outputs against must-pass scenarios (commit discipline, injection resistance, and over-compression refusal). The suite accepts candidate JSON artifacts, applies deterministic pass/fail rules plus decomposed telemetry signals, and supports replay stability measurement (`--replays N`) to quantify winner volatility under perturbation. This turns "regulation" from an architectural claim into an enforceable artifact.

Executable harness. The Verifier Gap layer is implemented as a replay suite: a minimal, versioned test battery that ingests candidate outputs, applies abstention-gated rules for commits, and emits PASS/FAIL plus stability metrics. This harness is intentionally small so it can be treated as a governance primitive: a shared, reproducible contract for what "safe selection without a verifier" means in practice.

Abstention-gated container writes. Container updates are treated as commits. When tie/abstain mass is high (or uncertainty is above threshold), the system must block container writes and instead request discriminating evidence or produce falsifiers. This commit discipline prevents over-compression from becoming an irreversible representation attractor and is enforced in the replay suite's over-compression scenario (RG-07).

Commitment-integrity extension. The replay suite now includes explicit stress scenarios for no-evidence reversion, self-disowning reasoning, and conflict-of-interest posture tightening (`RG-11` to `RG-13`). These scenarios enforce the rule that unchanged evidence cannot silently justify stance reversal and that incentive-conflict telemetry must tighten posture before commits.

Implementation pointer. A small replayable CI gate accompanies this note to operationalize tournament selection + abstention gating as a concrete harness. The goal is not to "prove correctness," but to enforce commit discipline, injection resistance, and stability under perturbation as minimal requirements for verifier-free discovery systems.

Replay suite governs downstream outputs; retrieval gates govern upstream selection signals.
