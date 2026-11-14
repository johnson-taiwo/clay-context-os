# Signal matrix - Clay

*Method: `knowledge-base/playbooks/signal-matrix-framework.md` (Bolaji's kit). Built 14 Nov 2026 from public
information. **Work in progress**: segments and signals are hypotheses to validate with Clay's sales and data
teams. Volumes are estimates until a test pull runs. Nothing here has been run in Clay yet.*

---

## Matrix 1: Segments

### The axes, and why

- **Rows = does the company have a GTM builder?** Clay's value depends on someone building in it. This can be seen
  from outside, through LinkedIn titles and job posts, and it changes the angle: a team with a builder needs
  consolidation, a team hiring one needs speed, a team without one needs templates or an agency.
- **Columns = company type** (the segments in `icp.md`): A scaling tech, B mid-market / enterprise, C agencies,
  D B2B services.

How each row is detected:
- **Has a builder:** at least 1 current employee titled GTM Engineer, Growth Engineer, RevOps or Sales/Marketing Ops
  (Clay "Find People" at company, title filter).
- **Hiring a builder:** open job with one of those titles in the last 30 days (Clay "Find Jobs at Company" / LinkedIn
  Jobs via Apify).
- **No builder:** has 3+ sales titles (AE, SDR, BDR) but none of the builder titles.

Every cell must be **observable, mutually exclusive, actionable and big enough** (framework rules).

### The grid

| | **A. Scaling tech** (Series A-D SaaS / AI, 50-1,000 staff) | **B. Mid-market / enterprise** (1,000+ staff, RevOps team) | **C. Outbound / GTM agencies** | **D. B2B services with outbound** (staffing, logistics, events, pro services, 50-1,000 staff) |
|---|---|---|---|---|
| **Has a builder** | **MEDIUM.** Builder exists, so Clay is either already in use or is up against a database. Angle: replace scattered vendors, more coverage per row. | **HIGH.** Several data contracts; RevOps owns the CRM. Angle: one contract for many vendors, CRM enrichment, rep self-serve. | **HIGH.** Agencies with a Clay builder already exist. Angle: Growth/Enterprise seats, Experts directory listing, cost per row. | **LOW.** Rare cell. Small volume. |
| **Hiring a builder** | **HIGHEST.** Budget approved, tools not yet chosen, new hire will want Clay. Angle: "set the new hire up with the stack from day one". | **HIGH.** Building a GTM engineering team. Angle: the platform the team builds on; enterprise controls. | **MEDIUM.** Agency hiring a "Clay specialist" = growth. Angle: partner programme, templates. | **MEDIUM.** First ops hire at a services firm. Angle: proven plays (Terrapinn-type results). |
| **No builder** | **LOW (now).** Founder-led or SDR-only. Angle: templates, Free / Launch plan, or an Expert agency. | **LOW.** Rare at this size. | n/a (an agency without a builder isn't a Clay agency) | **MEDIUM via partners.** Route to Expert agencies, not direct. |

### Cell detail for the priority cells

**A x Hiring a builder (HIGHEST)**
- Target: US/UK B2B SaaS or AI company, Series A-D, 50-1,000 staff, open GTM Engineer / RevOps / Growth Engineer role
  posted in the last 30 days.
- Company examples: Requires Clay research with filters: job title in {GTM Engineer, Growth Engineer, RevOps Manager,
  Revenue Operations}, posted < 30 days, company 50-1,000 staff, industry Software / AI, country US or UK.
  (I could not verify named companies with open roles today; the public job sites I checked hid the company name.)
- Lookalike seeds (existing Clay customers on the homepage, same profile): Cursor, Lovable, ElevenLabs, Hex, Legora,
  Vanta, Ramp.
- Angle: the new hire's first 90 days. "When [new role] starts, they'll want the data and the plays in one place."

**B x Has a builder (HIGH)**
- Target: 1,000+ staff, B2B, RevOps team of 2+, uses Salesforce or HubSpot, buys from 2+ data vendors (job posts or
  LinkedIn mention ZoomInfo, Apollo, Cognism, 6sense).
- Company examples: Requires Clay research with the filters above.
- Lookalike seeds (homepage customers): Rippling, Intercom, Datadog, Okta, Workday, HubSpot, Siemens.
- Angle: vendor consolidation + CRM enrichment ("a marketplace of data vendors under one contract").

**C x Has a builder (HIGH)**
- Target: outbound / lead-gen / GTM agencies, 5-200 staff, website or LinkedIn mentions Clay, runs campaigns for clients.
- Company examples (on Clay's own Experts directory, so already partners; use them as lookalike seeds, not prospects):
  ColdIQ, Growth Engine X. Prospects: Requires Clay research with filters: industry Marketing / Advertising services,
  website text contains "Clay" AND ("outbound" OR "lead generation"), staff 5-200.
- Angle: margin per client: templates across clients, credits per row, Growth plan controls.

**B x Hiring a builder (HIGH)** and **D x Hiring a builder (MEDIUM)**: same build as A x Hiring, with a different size
filter and angle.

### Priority ranking (Phase 2)

| Rank | Cell | Signal density | Product fit | Reach (data) | Why |
|---|---|---|---|---|---|
| 1 | A x Hiring a builder | High (job posts every week) | High | High (US/UK) | Fresh budget + a builder arriving |
| 2 | B x Has a builder | Medium | High | High | Biggest deals; vendor consolidation |
| 3 | C x Has a builder | Medium | High | Medium | Agencies grow seats with clients |
| 4 | B x Hiring a builder | Medium | High | High | Same build as rank 1 |
| 5 | D x Hiring a builder | Low-Medium | Medium | Medium | Proof exists (Terrapinn); fewer builders |

---

## Matrix 2: Signals

Status key: VERIFIED = the source exists and can be accessed. COMPOUND = only use with another signal. PARTIAL =
patchy coverage. KILLED = fails the Iron Law question: "Could I send this to a Clay operator right now with zero
ambiguity?" Volumes are **estimates (UNVERIFIED)** until a test pull runs. Credit costs: check
`knowledge-base/playbooks/clay/actions-data-credits.md` (Clay changed its pricing in March 2026).

| # | Type | Signal | Data source / Clay action | Key filters | Cadence | Est. volume | Status | Cells |
|---|---|---|---|---|---|---|---|---|
| S1 | Universal | **Hiring a GTM builder** | Clay "Find Jobs at Company"; or LinkedIn Jobs via Apify, then Clay | Title: GTM Engineer, Growth Engineer, RevOps, Revenue Operations, Sales Ops, Marketing Ops. Posted < 30 days. US/UK | Weekly | Hundreds / month | VERIFIED | A, B, D x Hiring |
| S2 | Niche | **Job post names Clay as a skill** | LinkedIn Jobs via Apify (full description text) -> Clay formula | Description contains "Clay" AND ("enrichment" OR "GTM" OR "outbound"). The pairing rule removes pottery / modelling jobs | Weekly | Tens-hundreds / month | VERIFIED | All rows. Hottest intent |
| S3 | Universal | **Champion moved company** | Clay job-change signal (Launch plan and up) on people whose title or skills show Clay use | Moved < 90 days; new company fits the ICP; past company is a known Clay customer (homepage logos as a seed list) | Monthly | Tens / month | VERIFIED | A, B, C |
| S4 | Universal | **New sales / RevOps leader** | Clay "Find People" at company: title + start date | CRO, VP Sales, VP RevOps, Head of Growth; start date < 90 days | Monthly | Hundreds / month | VERIFIED | A, B |
| S5 | Universal | **SDR/BDR hiring push** | Clay "Find Jobs at Company" + job count per company | 3+ open SDR/BDR/AE roles at once | Weekly | Hundreds / month | VERIFIED | A, B, D |
| S6 | Universal (VC only) | **Recent funding** | Crunchbase via Clay "Find Organization" / funding enrichment | Series A-D, < 60 days, B2B software / AI | Every 2 weeks | Hundreds / month (US) | VERIFIED | A only |
| S7 | Universal | **Sales team growth** | Clay company headcount enrichment, compared over two snapshots | +25% in 6 months | Quarterly | Unknown | COMPOUND | A, B (pair with S1 or S5) |
| S8 | Universal | **Uses a competing data vendor** | Job post text (S2 pipeline) mentioning ZoomInfo / Apollo / Cognism. BuiltWith **cannot** see these back-end tools | Mention in a live job post | Weekly | Unknown | COMPOUND | B x Has a builder |
| S9 | Niche | **Agency says Clay on its site** | Website text via Claygent or crawl4ai | Homepage/services page mentions "Clay" + outbound / lead generation | Monthly | Low hundreds total | VERIFIED (PARTIAL) | C |
| S10 | Universal | **Event attendance** | Clay Club / GTM event attendee pages (Luma etc.) via Apify | Attended in the last 30 days | Per event | Tens per event | VERIFIED (PARTIAL) | A, C |
| S11 | Universal | **Engages with GTM-engineering content** | LinkedIn post engagers via a LinkedIn scraper (Apify) | Liked / commented on Clay or GTM-engineering posts, < 14 days | Weekly | Hundreds / week | VERIFIED (PARTIAL) | A, C |
| K1 | - | Website visitors to clay.com | RB2B / Clay's own data | - | - | - | KILLED for this build: only Clay has it (first-party) | - |
| K2 | - | Funding for services firms (D) | Crunchbase | - | - | - | KILLED: services firms rarely raise VC; returns almost nothing | - |
| K3 | - | CRM / sequencer from BuiltWith alone | BuiltWith | - | - | - | KILLED as a main signal: back-end tools can't be seen from websites. Kept only inside S8 | - |

**The compounding insight:** 9 of the 11 live signals are universal. One "Find Jobs" build (S1, S2, S5, S8) serves
four segments by swapping title keywords and size filters. Only S9 (agency websites) needs its own build.

**Signal stack for the top cell (A x Hiring a builder):** S1 (mother intent) -> ICP filter (`icp.md` fit score 4+)
-> secondary signal S6 funding or S5 SDR push -> route the copy angle:
- S1 + S6: "just raised, building the GTM team"
- S1 + S5: "SDR team is growing, the builder will need the data plumbing"
- S1 + S2: "the job post already names Clay": shortest path, lead with templates for week one

---

## Matrix 3: Workflow tracker

| W # | Status | Workflow | Mother intent | Persona | Segment | Size | Secondary | Channel | Cadence |
|---|---|---|---|---|---|---|---|---|---|
| W1 | Planned | Hiring a GTM builder | S1 | Hiring manager: VP Sales / Head of Growth | A | 50-1,000 | S6 / S5 | Email + LinkedIn | Weekly |
| W2 | Planned | Job post names Clay | S2 | Hiring manager + RevOps lead | A, B, D | 50+ | S1 | Email | Weekly |
| W3 | Planned | Champion moved | S3 | The champion (a past Clay user) | A, B, C | 20+ | S4 | Email + LinkedIn | Monthly |
| W4 | Planned | New sales leader | S4 | The new CRO / VP | A, B | 50+ | S5 / S7 | Email | Monthly |
| W5 | Planned | Vendor consolidation | S8 + S1 | VP RevOps, CFO | B | 1,000+ | S7 | Email | Monthly |
| W6 | Planned | Agency builders | S9 | Agency founder | C | 5-200 | S10 / S11 | Email + LinkedIn | Monthly |

Columns to fill once live (from the framework): campaigns, launch date, iterations, changelog, Clay URL, copy URL,
leads, emails sent, progress, bounce rate.

## Next steps

1. Run a free test pull for S1 (preview only) and record the real volume against the estimate.
2. Validate the axes with someone on Clay's GTM team (or a Clay Club lead).
3. Run `/build-workflow-spec` on W1, then `/campaign-copy` against `context/messaging/facts.md`.
