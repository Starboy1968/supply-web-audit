# Supply Web Audit: the pipeline

The flow in one line: fix the boundary, list the players, write the links, trace the money, find the narrow points, read behavior, test moves, report and set triggers.

| Stage | Job | Input | Output | Human check |
|---|---|---|---|---|
| `01_scope` | fix the boundary | client brief, profile | `output/scope.md` | owner confirms boundary |
| `02_players-and-ai` | list players and AI uses | 01's output | `output/roster.md`, `output/ai-uses.md` | owner confirms roster |
| `03_link-ledger` | one row per link | 02's output, client records | `output/ledger.csv` | owner spot-checks 3 rows |
| `04_money-map` | trace credit and buffers | 03's output, bank records | `output/money-map.md` | owner confirms top lenders |
| `05_narrow-points` | find where the web is thin | 03 and 04 outputs | `output/narrow-points.md` | owner confirms top 3 |
| `06_behavior` | read behavior from records | 03's output, two periods of records | `output/behavior.md` | owner reviews alternative explanations |
| `07_test-moves` | test shocks and moves | 05 and 06 outputs | `output/tests.md` | owner picks scenarios |
| `08_report` | report and set triggers | all outputs | `output/report.md` | owner signs off |

Optional intake: an auditor can fill `tools/intake-form.html` first and save its exports to `intake/`. Stages 02 and 03 read those as Working drafts, verify them, and write `output/`. Nothing in `intake/` counts as a stage output.

Factory (stable, every run): `_shared/` and each stage's `references/`
Product (new each run): each stage's `output/`

Status is whatever exists: a stage is COMPLETE when its `output/` holds an artifact. An empty folder or placeholder does not count.
