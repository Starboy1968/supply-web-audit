---
type: audit-output
stage: 01_scope
client: Apex Digital Services
date: 2026-10-13
---

# Scope: Apex Digital Services Cyber Risk Supply Web

## Client, Decision, Beneficiary

**Client:** Apex Digital Services — 150-person SaaS platform (financial reporting automation), $8M ARR, AWS-hosted, 40+ active integrations.

**Decision:** Board-requested cyber risk visibility before acquisition talks. **Due:** 2026-11-15.

**Beneficiary:** CEO, board (investor perspective). Secondary: M&A due diligence counsel and acquirer's tech team — they need concentration risk, incident history, regulatory exposure.

---

## Layers in play and boundary cut

### Layers included

1. **Technology** — AWS infrastructure, cloud services, API integrations, data pipeline, encryption, secret management.
2. **Rules** — Regulatory exposure (GDPR, SOX, state data privacy), breach notification requirements, insurance claims.
3. **Behavior** — Vendor access practices, incident response procedures, patch management discipline, key person dependencies.
4. **Money** — Insurance coverage (E&O, cyber liability), recovery costs, customer contracts (SLAs), payment interruption risk.

### Layers explicitly excluded

- **Narrative** (brand, market positioning) — not material to this decision.
- **Physical** (data center locations, office security) — AWS handles it; not Apex's operational risk.
- **Ecology** (supply chain carbon, labor conditions, geopolitical resource chains) — out of scope for cyber audit.

### Boundary on players

**Inside:**
- Apex (host, orchestrator)
- AWS (infrastructure tier)
- 40 active integration partners (accounting software, banking APIs, identity providers)
- Vendors: cloud security tools, threat intelligence, incident response retainer

**Outside:**
- Customer accounts (Apex's customers' IT teams) — implementation risk is theirs, not part of supply web.
- Regulatory bodies (SEC, FTC, ICO) — enforcement bodies, not part of the web.
- Employees as individuals — policies score firm behavior only (per legal review).
- Competing SaaS platforms — not in Apex's supply web, only in market.

### Tiers

- **Top tier:** AWS, identity providers, payment processors.
- **Middle tier:** API integrations (40 partners), security tool vendors.
- **Bottom tier:** Apex's customers (by contract) and support contractors.

---

## What is not known (gaps)

1. **AWS security posture detail.** We have logs and cost history; we lack AWS account audit results, credential rotation policy, and VPC configuration sketch.
2. **Vendor risk scoring.** No formal risk matrix yet for the 40 partners (SaaS maturity, SOC 2 status, incident history).
3. **Incident root cause analysis.** Log exists of 3 past events (past 2 years); we lack technical post-mortems.
4. **Insurance policy fine print.** E&O and cyber liability policies documented; coverage gaps (retroactive dates, exclusions) not yet reviewed.
5. **Customer contract concentration.** Top-N revenue concentration not yet measured against SLA breach liability.
6. **Key person audit.** No functional redundancy map for critical roles (CISO, DevOps lead, sole integrations owner).

---

## Confidence and next step

**Boundary is tight and defensible for an M&A cyber audit.** The four layers (Tech, Rules, Behavior, Money) map directly to acquirer concerns. Gaps are data-sourcing, not conceptual.

**Next:** Approve this boundary (edit in place if needed). Once human confirms, Stage 02 will roster the players and map their AI uses.

