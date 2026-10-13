# 05_narrow-points: find where the web is thin

One job: name the few places where one failure moves the whole web.

## Inputs
- Working (this run): ../03_link-ledger/output/ledger.csv
- Working (this run): ../04_money-map/output/money-map.md
- Reference (every run): references/fragility-rules.md
- Reference (every run): ../../_shared/principles.md

Do NOT load: behavior material.

## Process
1. Run the common-dependency check on every pair of suppliers and lenders.
2. Mark hubs, bridges, keystones, loops, thresholds, delays.
3. Run the constraint search. Rank by strength and speed. Keep the top 10.

## Outputs
- narrow-points.md → output/

## Human check
Confirm the top three are real and in the right order. Edit in place.
