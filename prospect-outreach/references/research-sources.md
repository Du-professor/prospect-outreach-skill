# Prospect Research Sources

Use this guide when researching companies, judging evidence strength, or deciding what to do when inputs are incomplete.

## Source Priority

Prefer sources in this order:

1. Official company website: about, products, services, solutions, industries, support, partner, downloads, certifications, and contact pages.
2. Official product pages, datasheets, manuals, case studies, press releases, annual reports, sustainability reports, and investor materials.
3. Official hiring pages and job descriptions when they reveal current technology, expansion, or project signals.
4. Official social channels and verified company profiles.
5. Credible third-party sources: reputable news, trade publications, public databases, tender portals, patent pages, conference/exhibition listings, app marketplaces, partner directories, and channel pages.
6. Lower-confidence sources: scraped directories, SEO pages, old PDFs, forums, and unverifiable reposts.

## Evidence Handling

- Prefer recent and official evidence.
- Treat undated pages as stable only for facts such as company location, broad product categories, and longstanding services.
- Mark evidence older than 24 months as stale unless the fact is unlikely to change.
- When sources conflict, explain the conflict and prefer official or more recent sources.
- Do not infer procurement intent from industry overlap alone.

## Missing Information Behavior

| Missing Input | What To Do |
|---|---|
| User company website or description | Stop. Output a missing information checklist only. Do not score or draft outreach. |
| Prospect website, company name, or description | Output a generic ICP hypothesis and missing information checklist. Do not score or draft sales outreach. |
| Prospect website inaccessible but company identity can be verified elsewhere | Proceed with low evidence confidence and apply relevant hard caps. |
| Prospect identity cannot be verified | Treat as P4/research-only. |
| Contact name missing | Continue if company evidence is sufficient. Write role-neutral outreach. |
| Contact role missing | Score contact role conservatively and write routing-oriented outreach. |
| Target market/language missing | Infer from prospect website, country, and business context; default local language to Chinese only when unclear. |

## Research Questions To Answer

- What does the prospect sell, build, integrate, operate, or support?
- Which product lines, services, or solutions create a workflow where the user's company could help?
- What technical environment is visible: automation, robotics, HMI, SCADA, MES, machine vision, edge AI, cloud, embedded systems, industrial networks, compliance, or lifecycle services?
- What buying trigger is visible: expansion, new products, modernization, hiring, certification, new facility, new market, public tender, partner program, or support issue?
- Who likely owns the topic: engineering, automation, procurement, IT/OT, digitalization, maintenance, plant operations, product management, channel, or executive team?
- What evidence is missing before sales claims would be safe?

## Batch Prospect Output

When the user provides multiple prospects, first output a compact table:

| Company | Fit Score | Priority | Best Angle | Missing Evidence | Recommended Next Action |
|---|---:|---|---|---|---|

Then provide detailed analysis only for P1/P2 accounts unless the user asks for every account.
