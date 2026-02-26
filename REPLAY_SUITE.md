# Replay Suite (Reference Harness)

This is a companion artifact to the papers: a runnable, deterministic CI gate that evaluates “regulated agent” candidate outputs.

## What it is
- A small scenario suite (v0) with must-pass gates (RG-01 / RG-04 / RG-07)
- Deterministic fixtures + evaluator + runner
- Produces PASS/FAIL plus a JSON report

## Where it lives
Copy the `requested-agent-replay-suite/` repo from the provided bundle into its own Git repo and run:

```bash
npm install
npm run ci
```

## Why this exists
The papers argue for regulation (bands, budgets, checkpoint/rollback, abstention gating).  
This harness makes those claims *testable*.

Replay suite governs downstream outputs; retrieval gates govern upstream selection signals.

## Next intended expansions
- Candidate mode: run the gate on real outputs from an external agent run
- Replay stability (`--replays N`) to quantify tie/abstain + winner volatility
- Expand beyond v0 to the full suite
