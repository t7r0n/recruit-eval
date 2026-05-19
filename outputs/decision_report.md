# Decision Report: Recruit Eval

An open core evaluation + replay harness for recruiting agents: deterministic regression on your firm's own historical placements, with shortlist taste and outreach tone scoring before the agent ever goes live in a customer's tenant.

## Evidence-Grounded Findings

CLAIM: agentic policy boundary should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=1.708. [EVID: ev_0099]
CLAIM: committed failure replay should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=3.333. [EVID: ev_0044]
CLAIM: publicly gap should `block release until replay is understood` because blocks=3 reviews=2 mean_severity=3.333. [EVID: ev_0143]
CLAIM: publicly reviewer handoff should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=2.583. [EVID: ev_0055]
CLAIM: spott drift should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=2.5. [EVID: ev_0022]
CLAIM: spott evidence recall should `block release until replay is understood` because blocks=3 reviews=3 mean_severity=1.875. [EVID: ev_0000]
