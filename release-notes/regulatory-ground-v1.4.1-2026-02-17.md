# Regulatory Ground For Agentic AI (`v1.4.1`) - 2026-02-17

## Delta Summary

- Added explicit operational reproducibility definition: replayability + traceability by default, strict determinism where contract-critical.
- Added replay-suite reference implementation paragraph in evaluation harness section.
- Linked abstract regulatory claims to enforceable CI-gate artifacts and replay stability metrics.

## Key Conceptual Upgrades

- Reframed reproducibility as governed operations, not universal deterministic prose output.
- Clarified that posture trajectory (`g(t)`) and commit/withhold decisions are part of reproducibility evidence.

## New Terms / Definitions

- Operational reproducibility profile.

## Implications

- Strengthens auditability claim for verifier-free discovery systems.
- Grounds evaluation language in executable harness behavior.

## Open Questions

- What minimal replay metric set should be mandatory for external publication claims?
- Should tie/abstain drift thresholds be standardized across domains?

## Related Repositories

- `regulated-agent-replay-suite` (replayable downstream output governance)
- `regulated-retrieval-gates` (upstream selection-signal governance)
