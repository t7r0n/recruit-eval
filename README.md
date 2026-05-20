# Recruit Eval

An open core evaluation + replay harness for recruiting agents: deterministic regression on your firm's own historical placements, with shortlist taste and outreach tone scoring before the agent ever goes live in a customer's tenant.

![Recruit Eval working dashboard](outputs/project_working.svg)

## Why it exists

Spott has publicly committed to "agentic workflows" but the visible product surface (and the Spott app announcement) is still ATS/CRM table stakes: pipelines, outreach, transcripts, scheduling.

Most internal demos stop at a pretty chart. This repository is built around the harder part: a repeatable path from fixture, to failure, to evidence, to the operator action a serious team would actually trust.

## What is inside

- A deterministic replay harness tuned around spott, publicly, and committed.
- Company-specific strategy code in `src/recruit_eval/strategy.py`, not just README-level customization.
- Citation-locked reports where every decision claim has to point back to a generated evidence ID.
- Two visual artifacts generated from the latest run: `outputs/project_working.svg` and `outputs/evidence_map.svg`.
- A portable demo pack with JSON, CSV, Markdown, HTML, SVG, and benchmark artifacts.

![Recruit Eval evidence map](outputs/evidence_map.svg)

## Signals it measures

- `spott coverage`
- `publicly risk`
- `committed precision`
- `agentic latency`

## Failure modes it plants

- spott drift
- publicly gap
- committed misroute
- agentic blindspot

## Run it locally

```bash
uv sync
uv run recruit-eval all
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

## Sources

- https://spott.io/careers
- https://spott.io/jobs/software-engineer
- https://www.ycombinator.com/companies/spott
- https://venturebeat.com/ai/spotts-ai-native-recruiting-platform-scores-3-2m-to-end-hiring-software-chaos
- https://getlatka.com/companies/spott.io
- https://www.linkedin.com/in/lander-degr%C3%A8ve/
- https://www.linkedin.com/in/manuvanderveeren/
- https://www.linkedin.com/posts/lander-degr%C3%A8ve_spott-app-is-now-live-it-starts-by-solving-activity-7406339909176807425-LdZD
- https://www.fortino.vc/news/spott-raises-32-million-bolster-its-ai-native-recruitment-platform

## Boundary

Everything runs locally against synthetic fixtures. There are no credentials, no customer records, no outreach files, and no hosted API dependency.
