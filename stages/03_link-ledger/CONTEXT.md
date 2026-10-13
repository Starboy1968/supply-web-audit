# 03_link-ledger: one row per link

One job: write every link between players as one row, from records.

## Inputs
- Working (this run): ../02_players-and-ai/output/roster.md
- Working (this run): client contracts, invoices, payment history
- Reference (every run): references/ledger-fields.md
- Reference (every run): ../../_templates/ledger-header.csv
- Reference (every run): ../../_shared/evidence-labels.md

Do NOT load: AI uses, behavior scoring, other stages' references.

## Process
1. For each pair that exchanges anything, add a row. Include unwritten links (favors, shared owners, shared staff).
2. Fill every field from records. Blank means Gap, never a guess.
3. Label each row's evidence.

## Outputs
- ledger.csv → output/

## Human check
Spot-check three rows against what you know. Edit in place.
