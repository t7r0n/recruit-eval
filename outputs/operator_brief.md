# Operator Brief: Spott

Spott gets a local, deterministic pressure test around spott, publicly, and committed. The useful part is the repeatable evidence path from fixture to failure to operator action.

## Highest-leverage checks

- spott evidence replay -> block release until cited evidence is regenerated (spott_coverage, evidence ev_0088).
- agentic operator packet -> accept only if decision claims cite fixture evidence (publicly_risk, evidence ev_0143).
- committed regression harness -> open a regression issue with trace and benchmark delta (committed_precision, evidence ev_0110).
- publicly boundary probe -> route to reviewer with evidence packet (agentic_latency, evidence ev_0033).

## What makes this useful

The workflow is intentionally local and deterministic. A reviewer can run the same fixture set, inspect the evidence IDs, open the dashboard, and see exactly why a recommendation passed, went to review, or blocked.
