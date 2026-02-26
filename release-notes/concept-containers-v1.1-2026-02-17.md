# Concept Containers (`v1.1`) - 2026-02-17

## Delta Summary

- Added abstention-gated container write paragraph in regulated writes section.
- Defined high tie/abstain mass as explicit block condition for container commits.
- Mapped enforcement to replay-suite over-compression scenario (`RG-07`).

## Key Conceptual Upgrades

- Container updates are treated as governed commits, not passive representation edits.
- Over-compression risk is operationalized as a testable gate condition.

## New Terms / Definitions

- Abstention-gated container writes.

## Implications

- Reduces irreversible representational drift under uncertainty.
- Connects representation-level regulation to CI-verifiable governance.

## Open Questions

- Should container write gating depend on both tie mass and disagreement entropy?
- What persistence horizon best captures harmful over-compression commits?

## Related Repositories

- `regulated-agent-replay-suite` (`RG-07` over-compression enforcement)
