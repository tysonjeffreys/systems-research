# Reconstructed Cross-Project Change Log (Backfill)

Generated: 2026-02-18 (PT)

## Scope

This file reconstructs paper-change history across:

- `baseline-papers` (paper sources, zips, release notes)
- `regulated-agent-replay-suite` (downstream commit/output governance harness)
- `regulated-retrieval-gates` (upstream retrieval/selection governance harness)

## Evidence Used

- `baseline-papers/release-notes/*.md`
- `baseline-papers/CHANGELOG.md`
- `baseline-papers` file modification times for `main.tex`, zip bundles, and companion notes
- Zip-vs-source diffs for paper `main.tex` files
- `git log` + commit metadata in:
  - `regulated-agent-replay-suite`
  - `regulated-retrieval-gates`

## Reconstruction Limits

- `baseline-papers` currently has no commit history (`master` has no commits), so micro-commits inside that repo cannot be recovered.
- Timing/motivation links to code-repo commits are marked as inference when they rely on timestamp + semantic alignment.

## Chronological Reconstruction (PT)

| Timestamp | Location | Change |
| --- | --- | --- |
| 2026-02-11 21:51 | `baseline-papers` | `v1.0 - Two-Regime Control ... .zip` created (baseline snapshot). |
| 2026-02-12 08:17 | `regulated-agent-replay-suite` | `b5e396f` adds scenario-paper map + versioning note. |
| 2026-02-12 09:19 | `regulated-agent-replay-suite` | `b28b95a` adds `RG-05`/`RG-06` governance scenarios. |
| 2026-02-13 23:59 | `regulated-agent-replay-suite` | `f7dd4fc` adds reproducibility contract docs/manifest. |
| 2026-02-14 07:58-08:49 | `baseline-papers` | Paper bundles created/updated: Regulatory Ground v1.4.1, Critics-as-Sensors v0.1, Two-Regime v1.1 updated, Verifier Gap v0.1. |
| 2026-02-14 08:52 | both code repos | `2b0c7f4` (replay long-doc stress wiring) and `af1a098` (retrieval long-doc suite). |
| 2026-02-14 09:00 | `regulated-retrieval-gates` | `09653dc` wires long-doc stress into CI and report metadata. |
| 2026-02-16 07:24-07:25 | `baseline-papers` | `prism_verifier_gap/main.tex` updated; companion notes `regulated-agent-replay-suite-v0.md` and `regulated-retrieval-gates-v0.md` written. |
| 2026-02-16 08:14 | `regulated-agent-replay-suite` | `4674de5` adds commit-integrity and cross-domain stress packs + retrieval-gate signal wiring. |
| 2026-02-16 19:34 | `regulated-agent-replay-suite` | `db9d249` adds non-blocking paper proxy telemetry and ablation mode. |
| 2026-02-16 20:05-20:10 | `regulated-retrieval-gates` | `91783ec` adds basis-change risk + conservative gating; `d1b6f2d` bumps project to `0.2.0`. |
| 2026-02-16 20:20 | `regulated-agent-replay-suite` | `ed5b01a` bumps release to `v0.4.0`. |
| 2026-02-16 21:22-21:35 | `baseline-papers` | Post-bundle `main.tex` edits land in Concept Containers, Regulatory Ground, and Two-Regime Control. |
| 2026-02-17 03:53-03:54 | `baseline-papers` | Backfill docs added: `CHANGELOG.md`, `PUBLISHING.md`, per-paper release notes, and cross-project sync note. |

## Release-Grade Summaries By Paper

## Regulatory Ground for Agentic AI

- Version bump:
  - Recorded: `v1.2 -> v1.4.1` (per `prism_regulatory_ground_v1_4_1/README.md` and zip name).
  - Additional unversioned text patch after bundle: 2026-02-16 (`+3 insertions` vs zipped `main.tex`).
- What changed:
  - Added operational reproducibility framing (replayability + traceability, strict determinism only for contract-critical fields).
  - Added explicit replay-suite reference implementation language.
  - Post-bundle patch added coherence-support framing and commitment-integrity/incentive telemetry bullets.
- Why it changed:
  - Align paper claims with executable governance artifacts in replay/retrieval harnesses and newer integrity telemetry.
  - [Inference] Timing strongly aligns with replay `v0.4.0`/commit-integrity additions and retrieval basis-risk gating updates on 2026-02-16.
- User-visible effect:
  - Readers now get a concrete operational definition of reproducibility and clearer criteria for when commit rights should be withheld.
- Evidence:
  - `release-notes/regulatory-ground-v1.4.1-2026-02-17.md`
  - `prism_regulatory_ground_v1_4_1/main.tex`
  - Replay commits: `f7dd4fc`, `4674de5`, `db9d249`, `ed5b01a`
  - Retrieval commits: `91783ec`, `d1b6f2d`

## The Verifier Gap

- Version bump:
  - Recorded: `v0.1` bundle on 2026-02-14.
  - Additional unversioned text patch on 2026-02-16 (`+9 insertions` vs zipped `main.tex`).
- What changed:
  - Added explicit “candidate generation is not selection” framing and retrieval-gate artifact linkage.
  - Added reproducibility-without-verifiers framing (bounded variation + deterministic submodules).
  - Post-bundle patch adds self-disowning/no-evidence-reversion failure mode and commitment-integrity metrics.
- Why it changed:
  - Move from conceptual verifier-gap framing to enforceable governance checks that match harness telemetry and CI gates.
  - [Inference] Post-bundle integrity additions align with replay commit-integrity scenarios (`RG-11..RG-13`) and retrieval integrity metrics.
- User-visible effect:
  - Readers can now distinguish retrieval quality from selection governance and see concrete integrity failure classes.
- Evidence:
  - `release-notes/verifier-gap-v0.1-2026-02-17.md`
  - `prism_verifier_gap/main.tex`
  - Replay commit: `4674de5`
  - Retrieval commit: `91783ec`

## Concept Containers

- Version bump:
  - Recorded: `v1.0 -> v1.1` (zip naming + folder README).
  - Additional unversioned text patch on 2026-02-16 (`+4 insertions` vs zipped `main.tex`).
- What changed:
  - Added abstention-gated container write discipline, mapped to replay-suite over-compression scenario `RG-07`.
  - Post-bundle patch adds “coherence requires support” framing at representation layer and closing synthesis.
- Why it changed:
  - Tie representation updates to governed commit semantics and make over-compression risk testable.
  - [Inference] Alignment with replay-suite governance expansion and cross-project “coherence requires support” language.
- User-visible effect:
  - Readers now get explicit commit-gating logic for container updates, not just conceptual warnings about compression.
- Evidence:
  - `release-notes/concept-containers-v1.1-2026-02-17.md`
  - `prism_concept_containers/main.tex`
  - Replay scenario map and release notes: `docs/scenario-paper-map.md`, `RELEASE_NOTES.md`

## Critics-as-Sensors

- Version bump:
  - Recorded: `v0.1` (bundle + paper README).
  - No post-bundle source drift detected (`main.tex` matches zip).
- What changed:
  - Added implementation pointer to replayable CI gate and retrieval-gate analogue.
  - Clarified bounded-variation target as stable commit/withhold behavior, not identical prose.
- Why it changed:
  - Bridge theory to executable governance artifacts and align with verifier-gap/retrieval layers.
- User-visible effect:
  - Readers can map critics-as-sensors concepts directly to deployable harness behavior.
- Evidence:
  - `release-notes/critics-as-sensors-v0.1-2026-02-17.md`
  - `prism_critics_as_sensors/main.tex`

## Two-Regime Control

- Version bump:
  - Recorded: `v1.0 -> v1.1` (updated bundle created 2026-02-14; diff shows `31 insertions, 2 deletions` vs v1.0).
  - Additional unversioned text patch on 2026-02-16 (`+5 insertions` vs updated `v1.1` zip).
- What changed:
  - `v1.1` update added critic-as-sensor and abstention/tie-mass governance framing plus phase-discipline reproducibility hooks.
  - Post-bundle patch adds support-deficit framing, commitment-integrity hook (no silent reversion), and cross-cutting support principle.
- Why it changed:
  - Connect embodied two-regime control to the same selection-governance stack used in verifier-free language/retrieval systems.
  - [Inference] 2026-02-16 patch aligns with retrieval basis-change risk and replay integrity telemetry work.
- User-visible effect:
  - Readers now see explicit conditions for safe commit windows and how uncertainty/integrity telemetry controls irreversible actions.
- Evidence:
  - `release-notes/two-regime-control-v1.1-updated-2026-02-17.md`
  - `prism_two_regime_control/main.tex`
  - `v1.0 - Two-Regime Control_ Latent Coordination vs Compensation in Intelligent Systems.zip`
  - `v1.1 - Two-Regime Control_ Latent Coordination vs Compensation in Intelligent Systems_UPDATED.zip`

## Time-to-Analysis Layer

- Version bump:
  - Recorded bundle present: `v1.2` (2026-02-12).
- What changed:
  - No additional source-history evidence found in this repo snapshot (no source folder and no paper-specific release note in backfill set).
- Why it changed:
  - Not enough local evidence to reconstruct beyond bundle timestamp.
- User-visible effect:
  - No reconstructable post-`v1.2` deltas from available artifacts.
- Evidence:
  - `v1.2 -  The Time-to-Analysis Layer Pressure Points in AI-Assisted Research Systems.zip`

## Cross-Project Semantic Linkage

- Replay suite governs downstream commit/output behavior; retrieval gates govern upstream selection behavior.
- Explicit sync snapshot recorded on 2026-02-17:
  - replay head: `ed5b01a`
  - retrieval head: `d1b6f2d`
- Source:
  - `release-notes/cross-project-sync-2026-02-17.md`

## Open Gaps To Resolve

- Four papers have post-bundle `main.tex` edits not reflected in new zip artifacts:
  - `prism_regulatory_ground_v1_4_1/main.tex`
  - `prism_verifier_gap/main.tex`
  - `prism_two_regime_control/main.tex`
  - `prism_concept_containers/main.tex`
- If you want strict release traceability, publish a patch-bump batch (for example: `v1.4.2`, `v0.1.1`, `v1.1.1`) with matching release-note entries.
