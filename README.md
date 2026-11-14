# Clay Context OS

A Claude Code **Context OS** for **Clay** (clay.com): one folder that holds everything Claude needs to know to run
go-to-market work for the company. ICP, buyer personas, positioning, messaging, a signal matrix, playbooks, skills,
meetings, weekly priorities and a work log.

Built by **Johnson Taiwo** for the **GTM Co-op, week 1** (Nov 2026; facilitator Bolaji Anifowose).

> **Study build from public information only.** I don't work at Clay. Every fact carries its source and date
> (`context/docs/research/clay-company-research.md`); conflicting figures are marked UNVERIFIED.

## What's inside

| Folder | What it holds |
|---|---|
| `CLAUDE.md` | Project instructions Claude reads every session: the company, where things live, the rules |
| `context/docs/research/` | Clay facts: product, pricing, funding, customers, sources |
| `context/icp/` | ICP (with a 5-point fit test), personas by company size, **signal matrix** |
| `context/positioning/` | Positioning statement, value prop per persona, competitors |
| `context/messaging/` | Core message, pillars, angle per signal, **facts.md** (the only facts copy may use) |
| `context/brand-kit/` | Tone of voice |
| `knowledge-base/playbooks/` | Method docs (signal matrix framework, workflow anatomy, copy rules, Clay docs) |
| `knowledge-base/learnings/` | What worked and what didn't |
| `meetings/` | Class and call notes |
| `output/campaigns/` | Campaign briefs; first one: W1 "Hiring a GTM builder" |
| `weekly-priorities/` · `work-log/` | One file per week each, linked |
| `tools/` · `.claude/skills/` | Scripts and slash-command skills |

## The signal matrix in one look

- **Rows:** does the company have a GTM builder? (has one / hiring one / none). It's observable from LinkedIn titles
  and job posts, and it changes the angle.
- **Columns:** scaling tech · mid-market / enterprise · outbound agencies · B2B services.
- **Top cell:** scaling tech companies **hiring a GTM engineer / RevOps** (budget approved, stack not yet chosen).
- **11 live signals, 3 killed.** 9 are universal: one "Find Jobs" build serves four segments.
- **6 planned workflows**, starting with W1 "Hiring a GTM builder".

## How to use it

1. Clone it and open the folder in Claude Code (VS Code or the terminal).
2. Copy `.env.example` to `.env` and add your own keys. `.env` is git-ignored.
3. Type `/` to see the skills. Suggested order: `/signal-matrix refresh` -> `/build-workflow-spec` ->
   `/campaign-copy` -> `/clay-build-plan`.

## Credits

Skills, playbooks and tools come from Bolaji Anifowose's
[GTM starter kit](https://github.com/bolaji-ships/gtm-starter-kit), with third-party licenses in `THIRD-PARTY.md`.
The Clay-specific context (everything under `context/`, `meetings/`, `output/`, `weekly-priorities/`, `work-log/`,
`knowledge-base/learnings/`) is mine.
