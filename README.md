# Outbound Agent Eval

A local evaluation and replay harness for recruiting agents: deterministic regression on synthetic placement histories, with shortlist fit and outreach tone scoring before an agent is allowed into a live workflow.

![Outbound Agent Eval working dashboard](outputs/project_working.svg)

## Why it exists

Recruiting agents can generate shortlists, outreach, and handoff notes at high speed, but teams need proof that the agent preserves placement taste, tone, evidence grounding, and candidate relevance before it contacts real people.

The project is intentionally built as a local replay harness instead of a slide. It creates fixtures, plants realistic failure modes, produces citation-locked evidence, and turns the result into a dashboard a reviewer can inspect without credentials or hosted services.

## What is inside

- Deterministic fixture generation for the company-specific risk surface.
- Strategy code in `src/outbound_agent_eval/strategy.py` with project-specific scoring and visual evidence.
- Citation-locked reports where every decision claim points to a generated evidence ID.
- Two regenerated visual artifacts: `outputs/project_working.svg` and `outputs/evidence_map.svg`.
- A portable demo pack with JSON, CSV, Markdown, HTML, SVG, benchmark, and test artifacts.

![Outbound Agent Eval evidence map](outputs/evidence_map.svg)

## Signals it measures

- `Evidence coverage`
- `publicly risk`
- `committed precision`
- `agentic latency`

## Failure modes it plants

- evidence drift
- publicly gap
- committed misroute
- agentic blindspot

## Run it locally

```bash
uv sync
uv run outbound-agent-eval all
uv run pytest -q
uv run ruff check .
```

## Outputs worth opening

- `outputs/dashboard.html`
- `outputs/project_working.svg`
- `outputs/evidence_map.svg`
- `outputs/operator_brief.md`
- `outputs/decision_report.md`
- `outputs/strategy_model.json`
- `outputs/demo_pack.zip`

## Boundary

Everything runs locally against synthetic fixtures. There are no credentials, no customer records, no outreach files, and no hosted API dependency.
