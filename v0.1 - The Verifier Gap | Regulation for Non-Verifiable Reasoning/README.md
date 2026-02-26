# The Verifier Gap (v0.1)

This Prism project contains the LaTeX source for:

**The Verifier Gap — Regulation for Non-Verifiable Reasoning in Agents and Research Systems**

This paper is a short bridge in the Baseline / regulation series. It names the "verifier gap" regime (selection without task-specific verifiers) and specifies a minimal **Verifier Gap Layer**:

- judge-as-sensor telemetry (do not treat learned critics/judges as authorities)
- abstain/tie mass and disagreement as first-class uncertainty signals
- band-limited candidate generation and bounded selection (tournaments / capped pairwise comparisons)
- commit gating for persistent writes (including representation/container updates)
- judge versioning, drift monitoring, and rollback/recovery semantics

## Build

From this directory:

```bash
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```
