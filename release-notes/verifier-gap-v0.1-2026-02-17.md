# The Verifier Gap (`v0.1`) - 2026-02-17

## Delta Summary

- Added “Candidate generation is not selection” framing near introduction.
- Added “Regulated Retrieval Gates (artifact)” as upstream operational instantiation of bounded selection + abstention/tie telemetry.
- Added reproducibility-without-verifiers paragraph emphasizing bounded variation + deterministic submodules.

## Key Conceptual Upgrades

- Explicitly separated retriever quality improvements from selection-governance necessity.
- Strengthened claim that verifier-free stability comes from gated selection/commit policy, not retrieval quality alone.

## New Terms / Definitions

- Candidate generation is not selection.
- Reproducibility without verifiers (operational).

## Implications

- Preserves paper scope: governance layer ownership remains in Verifier Gap.
- Makes external retrieval advances “upstream inputs” rather than narrative competitors.

## Open Questions

- Which retrieval perturbations should be mandatory in verifier-gap replay suites?
- How should “stable enough selection telemetry” be thresholded across domains?

## Related Repositories

- `regulated-retrieval-gates` (upstream retrieval stress + telemetry)
- `regulated-agent-replay-suite` (downstream commit discipline gate)
