# Rulebook Starter Seed

Your whole business, modelled once: this seed holds an
`effortless-rulebook/effortless-rulebook.json` and generates everything that
can be derived from it without writing software.

## What `effortless build` produces

| Folder | From | What it is |
|---|---|---|
| `postgres/` | rulebook-to-postgres | The schema, `vw_*` views, functions and seed data |
| `docs/` | rulebook-to-markdown | Documentation of every table, field and rule |
| `rulespeak/` | rulebook-to-rulespeak | Business-readable RuleSpeak statements |
| `explainer-dag/` | rulebook-to-explainer-dag | Interactive dependency graph of every derived value |
| `xlsx/` | rulebook-to-xlsx | An Excel workbook with the model and live formulas |
| `effortless-rulebook/docker/` | effortless-rulebook-editor | A Docker image: Postgres + the generated API + the browser rulebook editor |

Nothing generated is meant to be edited or committed: change
`effortless-rulebook/effortless-rulebook.json`, run `effortless build`, and
every surface follows.

## Getting started

```bash
effortless build                            # generate everything
./effortless-rulebook/edit-rulebook.sh      # open the rulebook editor (needs Docker)
```

Replace the starter `WelcomeNotes` table with your own model — or drop your
existing `effortless-rulebook.json` over the one in `effortless-rulebook/`.

## Requirements

- the `effortless` CLI (`npm i -g @effortlessapi/cli`), signed in
- Docker, only for the rulebook editor
