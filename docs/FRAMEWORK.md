# Supply Web Audit Framework — Full Reference

## Core Concept

A **supply web** is not a supply chain. Chains are linear: A→B→C→end customer. Webs are meshed, where:
- Players have multiple suppliers and customers
- Credit and losses flow down; labor/goods flow up
- A single player can change payoffs for many others
- New players enter; exits cascade

**Infinite game:** Players are recycled. You audit the web at one moment in time, but know that players will enter/exit/change roles. The audit prepares for that.

## Seven Layers

Every link between players can be analyzed on seven layers (all connected):

1. **Money** — Cash flow, credit, buffers, insurance, concentration
2. **Physical** — Tangible assets, locations, throughput, scarcity
3. **Rules** — Law, regulation, contracts, enforcement, compliance
4. **Narrative** — Brand, story, trust, reputation, marketing
5. **Technology** — Systems, data, integrations, automation, AI
6. **Behavior** — Practice, incident response, culture, discipline, slack
7. **Ecology** — Environment, resources, labor conditions, geopolitical supply

**Ranking:** Not all layers matter equally for every audit. Client risk appetite sets priority. For cyber risk: Technology > Rules > Behavior > Money. For supply chain: Physical > Money > Rules > Ecology.

## Three Tiers

Every link is assigned to one tier (not per-player, per-relationship):

- **Top tier:** Strategic players, concentrated, slow to replace (AWS, major partners, regulators)
- **Middle tier:** Operational players, some slack, moderate to replace
- **Bottom tier:** Replaceable, high velocity, labor-intensive

**Flow rules:**
- Credit and losses flow DOWN (top absorbs most shocks)
- Labor and goods flow UP (bottom does the work)
- Middle is the swing tier (where pressure builds and breaks)

## The Pipeline (8 Stages)

### 01_scope
**Input:** Client brief or owner notes + profile  
**Output:** scope.md (what's in, what's out, gaps)  
**Human check:** Read aloud, confirm boundary is right

**Job:** Fix the boundary. Declare which layers matter. List what you don't know yet.

### 02_players-and-ai
**Input:** 01's scope  
**Output:** roster.md (all players), ai-uses.md (who uses AI, who approves)  
**Human check:** Owner confirms roster is complete

**Job:** Add a player only if removing it changes another player's payoffs. Include insurers, chokepoints, gatekeepers, shadow players.

### 03_link-ledger
**Input:** 02's roster, client contracts/records  
**Output:** ledger.csv (one row per link, 8 columns)  
**Human check:** Owner spot-checks 3 rows

**Job:** Write every relationship. Columns: source player, sink player, flow type (money/goods/data/labor), tier, volume/value, contract terms, risk notes, owner.

### 04_money-map
**Input:** 03's ledger, bank records, insurance  
**Output:** money-map.md (credit trace, buffer map)  
**Human check:** Owner confirms top 3 lenders

**Job:** Who has cash? Who is leveraged? What insurance exists? Where can credit dry up? Map recovery cost if a top link breaks.

### 05_narrow-points
**Input:** 03 + 04 outputs  
**Output:** narrow-points.md (chokepoints, single points of failure)  
**Human check:** Owner confirms top 3

**Job:** Find where the web is thin. A player with no backup? A link no one else can replace? A regulation that blocks all alternatives? Rank by speed-of-consequence.

### 06_behavior
**Input:** 03's ledger, 6–12 months of transaction records (two periods)  
**Output:** behavior.md (patterns, incidents, slack)  
**Human check:** Owner reviews alternative explanations

**Job:** Read records for what actually happens (vs. what policy says). Incident history? Patch delays? Vendor access discipline? Where is slack and where is it tight?

### 07_test-moves
**Input:** 05 + 06 outputs  
**Output:** tests.md (shock scenarios, move outcomes)  
**Human check:** Owner picks which scenarios matter

**Job:** Model scenarios: "If AWS region fails / top customer defaults / regulator changes rules / vendor goes down — how long until impact? Who survives?"

### 08_report
**Input:** All 7 stage outputs  
**Output:** report.md (signed risk report + re-audit triggers)  
**Human check:** Owner signs off

**Job:** Synthesize findings. State confidence (Established/Author/Gap). Set triggers: "Re-audit if X changes" (new player, new regulation, incident, policy change, X months elapse).

---

## Evidence Labels (Required)

Every claim uses one label:

- **Established** — From client records, public data, signed documents, or direct observation. No interpretation.
  - Example: "AWS account has MFA enabled (from audit log, 2026-10-13)"

- **Author's construction** — Derived reasoning, framework analysis, inferred from established facts. Transparent about the leap.
  - Example: "Because AWS is the only provider and has no regional redundancy (established), loss of one region means total platform downtime (author's construction)"

- **Gap** — Data we don't have, why it matters, how to fill it.
  - Example: "Vendor X's SLA is not in our contracts (gap). Knowing it affects failure recovery time. Filled by: request contract from procurement."

**Readers use these labels to judge what to trust.** Board might accept "Author's construction" for strategic implications, but counsel needs "Established" for breach likelihood.

---

## Roles in an Audit

- **Owner** — The client (CEO, risk officer, board). Makes approval gates. Provides records. Answers gaps.
- **Auditor** — The person/agent running the pipeline. Reads inputs, writes outputs, asks clarifying questions.
- **Beneficiary** — Who uses the report (board, counsel, acquirer, regulator). May not be the owner.

An audit can have multiple beneficiaries with different needs. The report must surface all of them.

---

## When to Use This Framework

✓ **Good fit:**
- Pre-acquisition due diligence (cyber, financial, operational risk)
- Board risk oversight (supply concentration, regulatory exposure, key person dependencies)
- Vendor assessment (can we survive their failure?)
- Resilience planning (what breaks first? how do we rebuild?)

✗ **Not a fit:**
- Compliance audits (use a compliance framework)
- Technical penetration testing (use a security framework)
- Market analysis (different methodology)
- One-off vendor risk screening (do this, then expand to a full audit if high risk)

---

## Customization

**Layers:** Can change per risk domain. Example:
- Cyber risk: drop Physical and Ecology; emphasize Technology, Rules
- Geopolitical supply chain: emphasize Ecology, Physical, Narrative
- Financial stress test: emphasize Money, Rules, Behavior

**Tiers:** Can expand for complex webs. Example: add "super-top" for central banks, or "sub-bottom" for gig labor.

**Evidence bars:** Legal/financial audits may require higher "Established" threshold. Resilience planning may accept more "Author's construction."

Document changes in `_shared/principles.md` before you start.

