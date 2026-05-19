# Policy Graph

A typed, auditable OEM warranty parser that turns any manufacturer policy PDF into a machine checkable coverage DAG - with every clause traceable to a span in the source.

## Why This Exists

SureBright's own JD spells out the most painful, lowest leverage line item on their roadmap: OEM warranty parsing - "converting manufacturer policies into machine readable coverage logic." Today every new merchant onboarding requires a human (or a one shot LLM call) to read each OEM's policy PDF (Whirlpool, Bosch, DJI, Peloton, Therabody...), decide what's covered vs.

## What It Builds

- Replays synthetic `surebright` and `spells` cases against the project's evidence rules.
- Scores `surebright_coverage`, `spells_risk`, and `painful_precision` so regressions are visible in CSV and JSON.
- Plants `surebright drift` and `spells gap` failures as negative controls.
- Writes citation-locked decision claims; unsupported claims fail verification.
- Exports a review dashboard and demo pack for `policy-graph` without hosted services.

## Local Run

```bash
uv sync
uv run policy-graph all
uv run pytest -q
uv run ruff check .
```

## Outputs

- `outputs/analysis.json`
- `outputs/scenario_report.csv`
- `outputs/decision_report.md`
- `outputs/evidence_packet.md`
- `outputs/dashboard.html`
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

This repository uses synthetic fixtures only. It has no credentials, no customer data, no outreach data, and no dependency on a hosted API.
