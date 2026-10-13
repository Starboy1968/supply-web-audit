# Stage 4: Money map
Job: Trace credit, cash, and buffers.

## Inputs
Working (this run):
- `03-link-ledger/output/ledger.csv`
- Client records: bank, loans, credit lines, AR and AP aging
Reference (every run):
- `_shared/payoffs-and-drivers.md`
- `_shared/principles.md`

## Process
1. List every lender and credit source. Count heads (hydra rule).
2. Compute buffer days and payment-timing gaps.
3. Run the 30% cut test: months until options are gone.
4. Flag lenders that share a parent, bank, or fund.

## Outputs
- `04-money-map/output/money-map.md`

## Human check
Owner confirms the top lenders and the buffer numbers.
