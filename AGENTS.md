# Supply Web Audit

One audit of one client's supply web (not chain), treated as an infinite game: players enter, exit, and are recycled. A signed report and a list of re-audit triggers leave this workspace.

Built on ICM: folders carry sequencing, hierarchy carries context, files carry state. Works with any agent or a person that can read and write files. If something needs explaining, it goes in that folder's CONTEXT.md.

## Where things live

| Folder | What it holds |
|---|---|
| `stages/` | the pipeline, in execution order (`01_` to `08_`) |
| `_shared/` | factory: principles, layers, payoffs, evidence labels, client profile |
| `_templates/` | blank starters for run artifacts (copy, never start blank) |
| `setup/` | one-time questionnaire that configures this copy for a client |

## Route by what just happened

| If | Go to | Then stop at |
|---|---|---|
| new client copy, no profile yet | `setup/questionnaire.md` | answers written to `_shared/client-profile.md` |
| starting a run | `stages/01_scope/CONTEXT.md` | human reads the output |
| a stage output approved | next numbered stage's `CONTEXT.md` | human reads the output |
| asked for status | scan `stages/*/output/` | report what exists |

## Always

- Label every claim Established / Author's construction / Gap (`_shared/evidence-labels.md`).
- Do not assume. Name what is unclear and ask.
- Load only what the current stage's contract lists.

## The one rule

Nothing moves to the next stage until a person has read the output of the last one.
