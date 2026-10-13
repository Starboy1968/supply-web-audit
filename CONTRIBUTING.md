# Contributing

This repo is an ICM workspace: folders carry sequencing, hierarchy carries context, files carry state. Keep it that way.

## Rules that keep ICM intact

- Each stage folder has one `CONTEXT.md` with Inputs, Process, Outputs, Human check. Change a stage's job there, nowhere else.
- A stage loads only what its `CONTEXT.md` lists. Add a reference to the Inputs list or the stage will not read it.
- Stable reference files live in `_shared/` (used by several stages) or `stages/NN_name/references/` (used by one). No copies in both.
- Run artifacts go in `stages/NN_name/output/`. Never commit real client data.
- Nothing advances until a person reads the last output. Do not remove human checks.
- Label every claim Established, Author's construction, or Gap (`_shared/evidence-labels.md`).

## Adding a stage

1. Create `stages/NN_name/CONTEXT.md` plus `output/.gitkeep`.
2. Add the stage to the table in the root `CONTEXT.md`.
3. Update the stage list in `README.md`.

## Keeping the intake form in sync

`tools/intake-form.html` mirrors `setup/questionnaire.md`, `_templates/`, and `stages/03_link-ledger/references/ledger-fields.md`. If you change a ledger field, a questionnaire question, or a template, change the matching column or field in the form's `COLS` table and export functions in the same PR. The CSV header it exports must equal `_templates/ledger-header.csv`.

## Adding a layer, tier, or evidence rule

1. Edit `_shared/layers-and-tiers.md` or `_shared/evidence-labels.md`.
2. Record why in `_shared/principles.md`.
3. Add a worked case under `examples/` if the change affects how a stage runs.

## Testing on a new domain

Run the pipeline on a fictional client first. Put the filled profile and any outputs in `examples/<name>/` and note what you had to change in the layers or tiers.

## Pull requests

Keep one change per PR. Say which stage contracts it touches.
