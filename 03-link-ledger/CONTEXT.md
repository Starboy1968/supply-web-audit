# Stage 3: Link ledger
Job: Write one row per link between players.

## Inputs
Working (this run):
- `02-players-and-ai/output/roster.md`
- Client records: contracts, invoices, payment history
Reference (every run):
- `_shared/ledger-fields.md`
- `_shared/evidence-labels.md`

## Process
1. For each pair that exchanges anything, add a row.
2. Fill every field from records. Blank means Gap, not a guess.
3. Label each row's evidence.
4. Include unwritten links (favors, shared owners, shared staff).

## Outputs
- `03-link-ledger/output/ledger.csv`

## Human check
Owner spot-checks three rows against what they know.
