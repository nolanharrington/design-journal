---
title: Design journal
description: A standalone product design journal connecting reasoning, strategy, evidence, and outcomes.
status: canonical
tier: 1
last_updated: 2026-11-06
related_files: [AGENTS.md, project.md, INDEX.yaml, templates/project-setup.md]
---

# Design journal

A lightweight journal for product design projects. Keep working notes close to
your decisions, track what changed for users and the product, and reuse the
evidence in case studies and performance reviews.

**One repository = one project.** Markdown files are the source of truth. No
application, dependencies, or analytics integrations are required.

## Start a project

1. The template owner enables **Settings → General → Template repository** on
   GitHub. This is a manual setting, not something these files enable.
2. Choose **Use this template → Create a new repository** for each project.
   Choose visibility deliberately; a private copy does not make sensitive data
   appropriate to share with an AI service.
3. Open the new repository in your preferred AI agent and use the prompt below.
   The instructions are model-independent, including for Luna and Sonnet;
   confirm your tool actually loads [AGENTS.md](AGENTS.md).
4. Answer a few questions at a time. The agent helps draft [project.md](project.md)
   and, optionally, a first working note. Review the drafts and approve the exact
   files before the agent saves them. No research or metrics are needed to start.

> Read AGENTS.md and guide me through setting up this design journal. Ask a few
> questions at a time, use only public-safe information, and show me the drafts
> before saving any files.

The [setup guide](templates/project-setup.md) covers context, strategy, success,
and an optional first entry. You can skip questions, say “unknown,” or pause.
To resume, ask the agent to review existing project context and continue setup;
it should preserve what you already recorded.

**Prefer manual setup?** Fill in `project.md`, then copy
[the note template](templates/note.md) into `notes/` and start writing. Templates
are optional scaffolding, not required forms.

The included [example note](notes/example-fictional.md) is entirely fictional.
It is not evidence about your project. Remove it from your new copy if unwanted.

## Directory map

| Path | Purpose |
| --- | --- |
| [project.md](project.md) | Problem, strategy, goals, constraints, and your role |
| [notes/](notes/README.md) | Informal, dated observations and working notes |
| [research/](research/README.md) | Public-safe research summaries and evidence |
| [decisions/](decisions/README.md) | Options, trade-offs, rationale, and revisits |
| [impact/](impact/README.md) | Success measures, baselines, and observed outcomes |
| [outputs/](outputs/README.md) | Evidence-backed case-study and review drafts |
| [templates/](templates/) | Copyable formats for each kind of record |
| [INDEX.yaml](INDEX.yaml) | Inventory of template documents, not a task backlog |

## A small routine

- **During work:** capture a note when something important happens. Rough
  bullets are enough. Separate observations from interpretations.
- **At a decision:** record the alternatives, why you chose one, and what would
  make you revisit it. Link the supporting notes or research.
- **Weekly or at a milestone:** review assumptions, update outcome measures,
  and note missing evidence. Record follow-up actions in a GitHub issue or your
  approved task tracker, using only public-safe wording.
- **At a review or project close:** ask the agent to draft a case study or
  performance-review summary from linked records. Review every claim yourself.

Use `YYYY-MM-DD-short-topic.md` for notes and research,
`DEC-001-short-topic.md` for decisions, and `short-measure-name.md` for impact.
Keep relative links between records. Update `INDEX.yaml` when adding or renaming
documents if you continue using the inventory.

## Working with an AI agent

The agent helps you clarify and organize; it does not decide what happened.
Give it only information you are authorized to share with the selected service.
It should propose drafts and destination paths, then wait for approval to save.

Example prompts:

> Read AGENTS.md and project.md. Help turn these public-safe bullets into a
> dated note. Preserve my wording and ask about gaps. Show the draft before saving.

> Review this week's notes. Suggest which decisions deserve a record, and link
> the evidence. Do not change any files yet.

> Draft an impact record. Distinguish our target from observed results, and mark
> missing baselines or attribution limits rather than inventing numbers.

> Draft a case study from the records I name. Link each substantive claim to its
> source, distinguish my contribution from the team's, and flag unsupported claims.

## Public-safe by default

This template is public. Treat journal content as potentially publishable even
if your project copy is private.

- Do not include secrets, credentials, customer or participant identifiers,
  personal information, raw interviews, confidential strategy, internal URLs,
  unpublished business metrics, or proprietary screenshots and attachments.
- Use only approved, non-identifying summaries and approved aggregate metrics.
  Removing names alone may not prevent re-identification in small groups.
- Keep restricted source material in an approved system outside this repository.
  Use a generic reference such as “restricted research source; not included”
  rather than a sensitive link, title, or identifier.
- Review files, metadata, links, attachments, issue text, and agent drafts before
  committing or publishing. Do not send restricted material to an AI agent to
  redact it; prepare a safe summary first.
- If sensitive material is committed, stop publication and follow your
  organization's incident process. Deleting a file does not remove Git history.

## Verification and review

Before sharing a record, check: is it public-safe, are sources linked, are targets
separate from measured results, and is individual contribution accurate? Check
relative links and required frontmatter when adding documents. This documentation
template has no automated CI, build, or test suite; human privacy and accuracy
review is still required.

All AI-assisted drafts require human review before publication. Mark substantial
AI assistance in the record or pull request. The existing [MIT license](LICENSE)
applies to this template; confirm rights before adding third-party material.
