# Policy Graph

A typed, auditable OEM warranty parser that turns any manufacturer policy PDF into a machine checkable coverage DAG - with every clause traceable to a span in the source.

![Policy Graph working dashboard](outputs/project_working.svg)

## Why it exists

SureBright's own JD spells out the most painful, lowest leverage line item on their roadmap: OEM warranty parsing - "converting manufacturer policies into machine readable coverage logic." Today every new merchant onboarding requires a human (or a one shot LLM call) to read each OEM's policy PDF (Whirlpool, Bosch, DJI, Peloton, Therabody...), decide what's c

Most internal demos stop at a pretty chart. This repository is built around the harder part: a repeatable path from fixture, to failure, to evidence, to the operator action a serious team would actually trust.

## What is inside

- A deterministic replay harness tuned around surebright, spells, and painful.
- Company-specific strategy code in `src/policy_graph/strategy.py`, not just README-level customization.
- Citation-locked reports where every decision claim has to point back to a generated evidence ID.
- Two visual artifacts generated from the latest run: `outputs/project_working.svg` and `outputs/evidence_map.svg`.
- A portable demo pack with JSON, CSV, Markdown, HTML, SVG, and benchmark artifacts.

![Policy Graph evidence map](outputs/evidence_map.svg)

## Signals it measures

- `surebright coverage`
- `spells risk`
- `painful precision`
- `lowest latency`

## Failure modes it plants

- surebright drift
- spells gap
- painful misroute
- lowest blindspot

## Run it locally

```bash
uv sync
uv run policy-graph all
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

- https://www.ycombinator.com/companies/surebright
- https://www.ycombinator.com/companies/surebright/jobs/HLJI44H-staff-ai-engineer-agentic-systems
- https://betakit.com/surebright-raises-3-2-million-cad-to-reinvent-retail-insurance/
- https://www.insurancebusinessmag.com/ca/news/technology/insurtech-surebright-secures-3-2-million-preseed-round-418620.aspx
- https://getlatka.com/companies/surebright.com
- https://theorg.com/org/surebright/org-chart/manish-chauhan
- https://nocap.blog/experience/surebright/
- https://www.surebright.com/faq/surebright-integration-process

## Boundary

Everything runs locally against synthetic fixtures. There are no credentials, no customer records, no outreach files, and no hosted API dependency.
