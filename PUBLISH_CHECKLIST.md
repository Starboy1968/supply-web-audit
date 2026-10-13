# GitHub Publication Checklist

All files below are ready to commit and push. This framework is designed to be published (with client data excluded).

## ✓ Framework Files (Commit All)

### Core documentation
- [x] `README.md` — Overview, quick start, structure
- [x] `AGENTS.md` — Framework architecture (ICM pattern)
- [x] `CONTEXT.md` — Pipeline flowchart and stage contracts
- [x] `.gitignore` — Keeps sensitive data out of repo

### Docs folder
- [x] `docs/FRAMEWORK.md` — Full reference (layers, tiers, evidence labels, roles)
- [x] `docs/AUDIT_EXAMPLE.md` — Worked example (Apex Digital Services cyber risk)

### Stage structure
- [x] `stages/01_scope/CONTEXT.md` — Stage 01 contract and process
- [x] `stages/02_scope/CONTEXT.md` through `08_report/CONTEXT.md` — All stage definitions
- [x] `stages/01_scope/output/scope.md` — EXAMPLE ONLY (Apex, delete before shipping if you want a clean repo, or keep as reference)
- [x] All stage reference files (`references/*.md` in each stage)

### Factory (_shared)
- [x] `_shared/principles.md` — Framework principles
- [x] `_shared/layers-and-tiers.md` — Layer and tier definitions
- [x] `_shared/payoffs.md` — Who wins/loses at each layer
- [x] `_shared/evidence-labels.md` — Evidence labeling guide
- [x] `_shared/client-profile.md` — EXAMPLE (Apex, update for your client)

### Templates
- [x] `_templates/` — Blank starters (never edit directly; copy before use)

### Setup
- [x] `setup/questionnaire.md` — One-time client configuration

---

## ✗ DO NOT Commit (Excluded in .gitignore)

- Client records (CSV, XLSX, PDF)
- Bank statements
- Audit logs
- Incident reports
- Insurance policies
- Any file in `/client-records/`, `/bank-statements/`, etc.

---

## Files You Should Edit Before Publishing

### If customizing for your domain
1. **`_shared/principles.md`** — Document any changes to layers, tiers, or evidence bars
2. **`docs/FRAMEWORK.md`** — Add domain-specific examples or customizations

### If publishing as a template repo
1. **Remove or replace the Stage 01 example** — `stages/01_scope/output/scope.md` and `_shared/client-profile.md` are examples (Apex Digital Services demo)
   - Either delete them (clean slate for users)
   - Or keep them labeled as "EXAMPLE" and add a note in README

---

## How to Publish to GitHub

### Quick version
```bash
cd supply-web-audit
git init
git add .
git commit -m "Initial supply web audit framework"
git remote add origin https://github.com/YOUR_ORG/supply-web-audit.git
git push -u origin main
```

### With explanatory commit message
```bash
git commit -m "Supply web audit framework: game theory-based risk auditing across seven layers

Includes:
- 8-stage pipeline for supply web risk auditing
- Framework documentation (FRAMEWORK.md)
- Worked example (Apex Digital Services cyber risk audit)
- Stage definitions and templates
- Evidence labeling system for audit transparency

Ready to customize for cyber, supply chain, operational, or financial risk domains."
```

---

## Repository Structure When Published

```
.gitignore
README.md                                # Start here
AGENTS.md                               # Framework architecture
CONTEXT.md                              # Pipeline overview
PUBLISH_CHECKLIST.md                    # This file

docs/
  ├── FRAMEWORK.md                      # Full reference
  └── AUDIT_EXAMPLE.md                  # Worked example

setup/
  └── questionnaire.md                  # Client configuration

stages/
  ├── 01_scope/
  │   ├── CONTEXT.md                    # Stage contract
  │   ├── references/
  │   └── output/
  │       └── scope.md                  # Example output (Apex)
  ├── 02_scope/
  │   ├── CONTEXT.md
  │   ├── references/
  │   └── output/
  │       ├── roster.md                 # Stage template (empty or example)
  │       └── ai-uses.md                # Stage template (empty or example)
  ... (03 through 08 follow same pattern)

_shared/
  ├── client-profile.md                 # Example: Apex Digital Services
  ├── principles.md
  ├── layers-and-tiers.md
  ├── payoffs.md
  └── evidence-labels.md

_templates/
  ├── stage-output.md                   # Blank starter for stage outputs
  └── ledger-template.csv               # Blank starter for link ledger
```

---

## Options for Publishing

### Option 1: Public Framework Repo
- Publish as a template/tool others can use
- Include the Apex example as reference
- License: MIT or CC-BY-4.0 (you choose)

### Option 2: Private Audit Results Repo
- One repo per client or client group
- Publish only `stages/*/output/` and `_shared/client-profile.md`
- Never publish records (bank, logs, contracts)
- Share with board, counsel, M&A team

### Option 3: Both
- Public repo with framework + Apex example (template for others)
- Private repos for each real client's audit results

---

## After Publishing

1. **Add a LICENSE file** (MIT, CC-BY-4.0, or internal use only — your choice)
2. **Add CONTRIBUTING.md** if you want external contributions or domain customizations
3. **Set up a GitHub Actions workflow** (optional) to validate stage outputs or check evidence labels
4. **Add CITATION.md** if you want academic/professional attribution

---

## Questions?

- **For framework questions:** See `docs/FRAMEWORK.md`
- **For audit workflow:** See `CONTEXT.md` and each stage's `CONTEXT.md`
- **For a worked example:** See `docs/AUDIT_EXAMPLE.md`

