---
title: Agent-guided project setup
description: A conversational onboarding guide for a new or partially configured design journal.
status: draft
tier: 3
last_updated: 2026-11-09
related_files: [../AGENTS.md, ../README.md, ../project.md, note.md, ../INDEX.yaml]
---

# Agent-guided project setup

Help the designer get started, not complete a lengthy intake form. Follow
[AGENTS.md](../AGENTS.md), keep answers public-safe, and ask at most three
questions per turn. Use answers already given; skip irrelevant questions.
“Unknown,” “not recorded,” and “not measured” are valid answers.

## 1. Orient and protect

Read [project.md](../project.md) and [the inventory](../INDEX.yaml). Identify
yourself as an AI assistant. Explain that no files will change until the designer
approves the drafts, and that sensitive information must not enter either the
conversation or repository. Do not ask for secrets, raw research, internal links,
personal details, or unapproved business metrics.

If project context is already filled in, summarize it and ask whether to resume
setup or update specific sections. Do not replace existing context wholesale.
Do not read unrelated records or treat the fictional example as actual work.

## 2. Establish context

Ask about public-safe project context:

- What are you designing, and what public-safe name should the journal use?
- What stage is the project in, and what timeframe is known?
- What is your role, and how does your contribution relate to the team's?

Map answers to **Overview** in `project.md`. Use roles rather than identifying
individuals. If the designer pauses, offer a partial draft instead of pressing
for more detail.

## 3. Understand the problem and strategy

Spread these prompts across turns, adapting to what is already known:

- Who is the intended audience, and what is difficult in their current experience?
- What approved evidence supports that need? “Not yet available” is fine;
  do not request restricted source files to fill the gap.
- What user and product outcomes are you aiming for, and why?
- What approach are you considering, and what assumptions underpin it?
- Which principles, constraints, risks, and non-goals will guide trade-offs?

Map answers to **Problem and evidence** and **Design strategy**. Distinguish
evidence from interpretation and planned strategy from decisions already made.
If useful, offer tentative wording for a design rationale or assumption only as a
proposal for the designer to confirm; never invent their reasoning. Do not frame
predicted outcome metrics as impact or success measures.

## 4. Define success and boundaries

- Has completed work led to an observed change? What approved evidence or
  measure supports that? If it is not quantified, what public-safe metric or
  evidence source could help find or measure the change, or be tracked in future
  work? Do not predict an outcome or set an impact target.
- What is the current experience or baseline for comparison? If an approved value
  is available, include its units, time period, source, and limitations. Otherwise,
  record “unknown” or “not measured”; an approved qualitative description is also
  useful.
- What accessibility or quality guardrails matter, and when should you review
  the strategy?
- What categories of information must stay outside this journal?

Map answers to **Success and review**. Keep the journal retrospective: metrics
suggestions are for finding or collecting evidence, not forecasting results.
Summarize approved baseline information in `project.md` or link an existing impact
record. Do not treat a measurement taken after a change as a pre-change baseline.
Missing baselines do not block setup.
Do not create impact records or analytics integrations during setup; additional
records require a separate scoped proposal. Do not record identifying details
while describing publication boundaries.

## 5. Offer a first note

Ask whether the designer wants to record current work, an open design question,
or a recent activity. This is optional. If yes, use [the note template](note.md)
and ask for the event date rather than assuming it happened today.

Propose `notes/YYYY-MM-DD-short-topic.md`, confirm the date and filename, and
check that the path is unused. If a date is unknown, leave it “not recorded”
in the entry and confirm a filename using the actual recording date. Include
only user-provided observations and clearly labeled interpretations. Open
questions are not automatically tasks; concrete follow-up work must follow
the tracking and authorization rules in `AGENTS.md`.

## 6. Review before saving

Show the complete proposed `project.md` and optional note, plus any inventory
addition. Keep unreviewed records in `draft` status, use the actual edit date,
and note AI-assisted drafting without implying human approval.

Summarize uncertainties and ask:

> Does this accurately reflect your project, and is everything safe to include?
> May I save these specific drafts to the listed paths?

Wait for explicit approval. If the designer requests revisions, show the revised
drafts before saving. Preserve existing entries and evolution history; propose
dated context changes rather than silently rewriting earlier strategy.

## 7. Save and verify the approved scope

After approval, save only the named files. Add an approved new note to
`INDEX.yaml`; the existing project file is already indexed. Check required
frontmatter, relative links, inventory consistency, and separation of claims
from evidence. Review for obvious sensitive content without claiming privacy
certification. Report actual results and any blockers.

End with changed paths and the next simple action: capture a working note when
something meaningful happens. Do not commit, push, publish, delete the example,
or create external issues as part of setup without separate authorization.

## Review scenarios

Use these scenarios for human review of the instructions; they are not evidence
that any specific agent model has been tested:

| Scenario | Expected behavior |
| --- | --- |
| New project, minimal answers | Draft partial context; label unknowns; no required metrics |
| Existing context or resumed setup | Use prior answers; propose scoped updates; preserve history |
| Designer declines first note | Propose only project context; no new note or inventory entry |
| Approval withheld or revisions requested | No writes until exact revised drafts are approved |
| Potentially sensitive answer | Stop without repeating it; request a safe summary |
| Missing baseline or date | No invented value or event date; confirm recording-date filename if needed |
| Note filename already exists | Propose another path or ask; never overwrite without specific permission |
