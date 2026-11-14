# CLAUDE.md - Clay Context OS

*Read automatically at the start of every Claude Code session in this folder. It says what the company is, where every
fact lives and the rules for working here. Built by Johnson Taiwo for the GTM Co-op (week 1, Nov 2026).*

## The company in one paragraph

**Clay** (clay.com) is a go-to-market data and workflow platform. Its homepage headline is "Build systems to grow
revenue", with the line "Infrastructure to get any data, run agentic workflows, and launch GTM plays." Teams use it to
pull data from 150+ sources into one table (waterfall enrichment), research accounts with AI agents (Claygent), score
and route leads, and push the result to email, ads and the CRM. It sells to B2B GTM teams, from startups to enterprises
like Anthropic, OpenAI, Figma, Rippling and Vanta, and to the agencies that run outbound for them.
Full facts and sources: `context/docs/research/clay-company-research.md`.

> This is a **study build from public information only**. I don't work at Clay, and nothing here is Clay's internal data.
> Every number carries its source and date. Anything unconfirmed is marked **UNVERIFIED**.

## Where everything lives

| Need | Open |
|---|---|
| Company facts, numbers, sources | `context/docs/research/clay-company-research.md` |
| Who buys (ICP) | `context/icp/icp.md` |
| Buyer types and what each one cares about | `context/icp/personas.md` |
| Segments + buying signals + workflow tracker | `context/icp/signal-matrix.md` |
| Positioning, value proposition | `context/positioning/positioning.md` |
| Competitors and how to talk about them | `context/positioning/competitors.md` |
| Core message and pillars | `context/messaging/messaging.md` |
| The ONLY facts copy may use | `context/messaging/facts.md` |
| Tone of voice | `context/brand-kit/tone-of-voice.md` |
| Method docs the skills read | `knowledge-base/playbooks/` |
| What worked and what didn't | `knowledge-base/learnings/` |
| Call and class notes | `meetings/` |
| Campaigns we design | `output/campaigns/` |
| This week's priorities | `weekly-priorities/` |
| What was done, when | `work-log/` |
| Scripts and tools | `tools/` (each has its own README) |
| Skills | `.claude/skills/` (type `/` to list them) |

## How to work here

1. **Read before writing.** For any GTM task, read the ICP, personas, signal matrix and facts file first.
2. **Facts gate.** Prospect-facing copy uses only what is in `context/messaging/facts.md`. Anything else becomes a
   `{{placeholder}}`, never a number from memory.
3. **Signal first, then ICP filter.** A workflow starts from a buying signal, then filters to the ICP, then stacks one
   secondary signal for the angle (`knowledge-base/playbooks/workflow-anatomy.md`).
4. **No fake companies.** Every company named must be real and checked. If research comes up empty, write
   "Requires Clay research with filters: ...".
5. **Log as you go.** Each finished task adds one line to this week's file in `work-log/`: time, what, numbers, next.
6. **Learnings compound.** When something works or fails, add a dated note in `knowledge-base/learnings/`.
7. **Keys stay secret.** API keys go in `.env` (git-ignored). Never paste a key into chat or commit it. `.env.example`
   lists the names only.
8. **Never spend credits without asking.** Clay, enrichment and AI runs cost money. Forecast rows x cost first.

## Skills in this repo (from Bolaji's GTM starter kit)

Research to copy: `/campaign-strategy` -> `/signal-matrix` -> `/build-workflow-spec` -> `/campaign-copy`.
Clay builds: `/build-clay`, `/clay-build-plan`, `/prompt-builder`, `/campaign-qa`, cost skills.
Licenses and credits: `THIRD-PARTY.md`.
