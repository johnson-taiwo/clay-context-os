# Ideal customer profile - Clay

*Status: hypothesis from public information (14 Nov 2026). Clay's real ICP comes from its CRM: who closes fastest,
spends most and stays longest. Validate before building on it.*

## The one-line ICP

**B2B companies that run outbound or account-based sales, have (or are hiring) someone who builds GTM systems, and
buy data from more than one source.**

Why this works: Clay's value grows with the number of data sources and plays a team runs. One rep with one database gets
little from it. An ops person who has to stitch five vendors, a CRM and a sequencer together gets a lot.

## Firmographics

| Attribute | Fit | Notes |
|---|---|---|
| Business model | B2B, sold by a sales team (not pure self-serve B2C) | Clay needs an outbound, ABM or inbound-routing motion to serve |
| Size | 20 to 5,000 employees. Core: 50 to 1,000 | Under 20 is usually founder-led with no ops builder. Over 5,000 is Enterprise, with a longer cycle |
| Industry | Software / SaaS and AI first. Then fintech, data, security, dev tools | Same industries as the homepage logos |
| Second ring | B2B services with outbound: staffing, logistics, events (e.g. Terrapinn), agencies | Proven by Terrapinn and the Experts directory |
| Stage | Seed to late-stage VC-backed, plus profitable mid-market | Funding speeds up GTM hiring |
| Geography | US first, then UK / Europe, Australia | English-language data is richest. GDPR limits EU enrichment |
| GTM stack | A CRM (HubSpot or Salesforce) + a sequencer (Outreach, Salesloft, Instantly, Smartlead) | Clay sits between data and these tools |
| Team | Has RevOps, GTM ops, growth or a GTM engineer, or is hiring one | **The strongest fit marker** |

## Fit test (score 0-5, one point each)

1. B2B with a sales team.
2. 20 to 5,000 employees.
3. Has or is hiring RevOps / GTM engineer / growth ops.
4. Runs outbound or ABM (has SDRs or BDRs, or is hiring them).
5. Uses a CRM + a sequencer.

4-5 = priority. 3 = nurture. 0-2 = not now.

## Segments (detail and signals in `signal-matrix.md`)

| Segment | Who | Why they buy |
|---|---|---|
| A. Scaling tech companies | Series A to D SaaS / AI, 50 to 1,000 staff, growing a sales team | Need pipeline fast; ops team is small; data is scattered |
| B. Mid-market / enterprise GTM orgs | 1,000+ staff, RevOps team, several data vendors | Consolidate vendor contracts; enrich the CRM; let reps self-serve |
| C. Outbound and GTM agencies | Agencies that build lists and run campaigns for clients | Clay is their production line. Seats grow with clients |
| D. B2B services with an outbound motion | Staffing, logistics, events, professional services | Same plays, fewer GTM engineers. Needs templates and an agency |

## Anti-ICP (do not target)

- B2C / consumer brands with no sales team.
- Companies under 10 staff with no one to build (they churn after the free plan).
- Buyers who want a plain contact database and nothing else. Apollo or ZoomInfo serves them better, and they churn.
- Regulated cases where third-party enrichment is restricted (some EU public bodies, healthcare patient data).

## Things a database cannot tell you (the gate)

Does this company have a person who will **build** in Clay, and the time to do it? Headcount and industry don't answer
this. Job posts, LinkedIn titles and Clay-skill mentions do (see the signals).
