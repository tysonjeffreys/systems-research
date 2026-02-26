# Cross-Project Sync - 2026-02-17

This note records paper-adjacent updates that live in companion repositories.

## Regulated Agent Replay Suite

- Repository: `/Users/tmoney/work/baseline_project/regulated-agent-replay-suite`
- HEAD: `ed5b01a`
- Recent relevant commits:
  - `ed5b01a` Bump release to v0.4.0
  - `db9d249` Add non-blocking paper proxy telemetry and ablation mode
  - `4674de5` Add optional cross-domain integration stress pack and retrieval-gate signal
  - `2b0c7f4` Add long-doc stress coverage and governance wiring

## Regulated Retrieval Gates

- Repository: `/Users/tmoney/work/baseline_project/regulated-retrieval-gates`
- HEAD: `d1b6f2d`
- Recent relevant commits:
  - `d1b6f2d` Bump project version to 0.2.0
  - `91783ec` Add basis-change risk telemetry and conservative gating
  - `09653dc` Wire long-doc stress gates into CI and report metadata
  - `af1a098` Add long-doc retrieval stress suite

## Paper Linkage Summary

- Upstream selection signals: `regulated-retrieval-gates`
- Downstream commit/output governance: `regulated-agent-replay-suite`
- Bridging statement in papers: “Replay suite governs downstream outputs; retrieval gates govern upstream selection signals.”
