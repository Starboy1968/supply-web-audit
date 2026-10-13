# Audit Example: Apex Digital Services (Cyber Risk)

This is a worked example of the supply web audit framework applied to cyber risk. Use it to understand how the pipeline works before running your own audit.

## The Client

**Apex Digital Services**
- Mid-market SaaS: financial reporting automation for accountants
- $8M ARR, 150 employees, AWS-hosted
- 40+ active API integrations (accounting platforms, banking APIs, identity providers)
- Pre-acquisition due diligence: board needs cyber risk visibility

**Decision:** Can we survive a breach or infrastructure failure? What are our concentration risks?

**Beneficiary:** CEO, board (investor perspective), M&A due diligence team

---

## Stage 01: Scope

**Output:** `stages/01_scope/output/scope.md`

### What was set
- **Layers:** Technology (primary), Rules, Behavior, Money
- **Excluded:** Narrative, Physical, Ecology (justified in output)
- **Boundary:** Apex + AWS + 40 integration vendors; excludes customers, regulators, competitors
- **Tiers:** Top (AWS, IdP), Middle (40 partners, security tools), Bottom (customers, contractors)

### What was not known (gaps)
1. AWS security posture detail — have logs, lack audit results and VPC config
2. Vendor risk matrix — no formal scoring for 40 partners yet
3. Incident RCA — we have incident log, lack post-mortems
4. Insurance fine print — policies exist, coverage gaps unknown
5. Revenue concentration — top customer exposure not measured
6. Key person redundancy — no functional backup map

### Key principle
**Boundary is tight and defensible for M&A.** Four layers map directly to acquirer concerns. Gaps are data-sourcing, not conceptual.

---

## How This Differs from Traditional Risk Audits

| Aspect | Traditional Risk Audit | Supply Web Audit |
|---|---|---|
| **Boundary** | Entire organization | Only the web that matters for this decision |
| **Layers** | Usually 1–2 (e.g., "cyber risk") | Seven connected layers; rank by relevance |
| **Players** | Assets/threats | Relationships where payoffs change |
| **Time horizon** | Snapshot | Infinite game (players recycle) |
| **Output** | Checklist of controls | Map of where web is thin, test scenarios, triggers |

---

## What Comes Next (Stages 02–08)

Once the boundary is approved:

**Stage 02:** Roster all 45+ players (Apex, AWS, each of 40 partners, 4 security vendors, insurers, etc.). Map who uses AI and who approves it.

**Stage 03:** Write the link ledger: 40–60 rows. Each row: [Source] → [Sink] | flow type | tier | contract terms | risk flag.
- Example: AWS → Apex | Data | Top | SLA 99.99% | No alternative region

**Stage 04:** Trace money. Insurance coverage? Who has cash reserves? If a top link breaks, what's recovery cost?

**Stage 05:** Find narrow points. Which 40 vendors are irreplaceable? Which have no SLA backup? Which regulations block alternatives?

**Stage 06:** Read behavior from records. 18 months of AWS logs + payment history. Incident frequency? Patch delays? Vendor access discipline?

**Stage 07:** Test scenarios. "If AWS region fails, how long until impact? If top vendor goes down, who absorbs the work?"

**Stage 08:** Write the signed report. State confidence on each claim (Established/Author/Gap). Set re-audit triggers.

---

## Key Concepts in This Audit

### Tiers (not all players equal)

- **Top:** AWS is strategic, hard to replace, absorbs shocks first
- **Middle:** 40 partners are operational, some redundancy, replaceable in months
- **Bottom:** Customers are replaceable (by contract), high velocity

### Narrow points (where web is thin)

Questions the audit will answer:
- Can we function without AWS? (Probably not — narrow point)
- Can we function without partner X? (Depends on tier and contract)
- What happens if top 3 customers default? (Stress test in Stage 07)

### Infinite game

Apex will hire new staff, partners will change, new regulations will arrive. The audit doesn't fix all risk; it prepares Apex for change. Re-audit triggers tell them when the web has shifted enough to need a fresh look.

---

## How to Use This Example

1. **Read Stage 01 output** (`stages/01_scope/output/scope.md`) to understand boundary-setting
2. **If you're running your own audit:** Copy this structure but fill in your client's details
3. **Expected timeline:** 2–4 weeks per client (depends on data availability)
4. **Evidence standard:** Label every claim (Established/Author/Gap) so readers know what to trust

---

## Differences if You Audit a Different Risk Domain

### Supply Chain (Physical + Money focus)
- Layers: Physical, Money, Rules, Ecology (drop Narrative, de-emphasize Behavior)
- Gaps: Supplier geopolitics, material substitutes, logistics costs
- Narrow points: Single-source materials, choke geography, tariff sensitivity

### Operational Resilience (Behavior + Technology focus)
- Layers: Behavior, Technology, Money, Rules (drop Physical, Ecology)
- Gaps: Incident response playbook effectiveness, key person cross-training
- Narrow points: Undocumented processes, single-person skills, aging infrastructure

### Regulatory/Compliance Risk (Rules primary)
- Layers: Rules, Behavior, Money, Technology
- Evidence bar: Higher "Established" threshold (legal review required for many claims)
- Narrow points: Regulator concentration, enforcement history, change detection

---

## Questions Before You Start Your Own Audit

1. **Who is the decision-maker?** (They approve at each stage.)
2. **What records can you access?** (Bank, contracts, logs, incident history, insurance policies)
3. **What is your evidence bar?** (Board = Author's construction OK; Counsel = Established only)
4. **How many layers matter?** (Seven is comprehensive; pick 4–5 for speed)
5. **How much time do you have?** (Slow: 4 weeks with detailed records; Fast: 2 weeks if records are ready)

---

**Next:** See `FRAMEWORK.md` for full reference, or start your own audit by editing `setup/questionnaire.md`.
