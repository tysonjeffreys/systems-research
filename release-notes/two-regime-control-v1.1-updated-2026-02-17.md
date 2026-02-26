# Two-Regime Control (`v1.1` updated) - 2026-02-17

## Delta Summary

- Added phase-discipline reproducibility hook paragraph in critics-as-sensors subsection.
- Added explicit commit-window paragraph: telemetry prerequisites + upstream posture controller behavior.

## Key Conceptual Upgrades

- Operationalized “write when stable” into transition-window discipline.
- Clarified selection gate role as upstream controller of commit rights under degraded telemetry.

## New Terms / Definitions

- Phase-discipline reproducibility hook.
- Phase-discipline commit windows.

## Implications

- Connects embodied control framing to verifier-free write governance in tool-using systems.
- Reduces irreproducible flailing by constraining irreversible actions to stable windows.

## Open Questions

- Which strain/uncertainty composite is best for opening commit windows?
- What timeout policy should force recovery vs continued evidence gathering?

## Related Repositories

- `regulated-agent-replay-suite` (downstream commit gating)
- `regulated-retrieval-gates` (upstream selection telemetry)
