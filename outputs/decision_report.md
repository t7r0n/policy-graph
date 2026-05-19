# Decision Report: Policy Graph

A typed, auditable OEM warranty parser that turns any manufacturer policy PDF into a machine checkable coverage DAG - with every clause traceable to a span in the source.

## Evidence-Grounded Findings

CLAIM: lowest policy boundary should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=1.708. [EVID: ev_0033]
CLAIM: painful failure replay should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=3.333. [EVID: ev_0110]
CLAIM: spells gap should `block release until replay is understood` because blocks=3 reviews=2 mean_severity=3.333. [EVID: ev_0143]
CLAIM: spells reviewer handoff should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=2.583. [EVID: ev_0121]
CLAIM: surebright drift should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=2.5. [EVID: ev_0088]
CLAIM: surebright evidence recall should `block release until replay is understood` because blocks=3 reviews=3 mean_severity=1.875. [EVID: ev_0132]
