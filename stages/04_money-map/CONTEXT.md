# 04_money-map: trace credit and buffers

One job: show who the client owes, who owes the client, and how long the cash lasts.

## Inputs
- Working (this run): ../03_link-ledger/output/ledger.csv
- Working (this run): bank, loan, and credit-line records; AR and AP aging
- Reference (every run): references/money-rules.md
- Reference (every run): ../../_shared/payoffs-and-drivers.md

Do NOT load: behavior or narrow-point material.

## Process
1. List every lender and credit source. Count heads.
2. Compute buffer days and payment-timing gaps.
3. Run the 30% cut test and the shared-parent check (see references).

## Outputs
- money-map.md → output/

## Human check
Confirm the top lenders and the buffer numbers against the bank statements. Edit in place.
