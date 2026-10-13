# Stage 5: Narrow points
Job: Find where the web is thin.

## Inputs
Working (this run):
- `03-link-ledger/output/ledger.csv`
- `04-money-map/output/money-map.md`
Reference (every run):
- `_shared/principles.md`

## Process
1. Common-dependency check: second suppliers on the same bank, port, cloud, or owner are not redundancy.
2. Mark hubs, bridges, keystones, feedback loops, thresholds, delays.
3. Constraint search: what single thing limits the whole.
4. Rank by strength and speed. Cap at the top 10.

## Outputs
- `05-narrow-points/output/narrow-points.md`

## Human check
Owner confirms the top three are real and in the right order.
