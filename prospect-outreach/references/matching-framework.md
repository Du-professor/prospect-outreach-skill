# Prospect Matching Framework

Score each prospect out of 100. Use evidence from the prospect's public information, the user's company information, and clearly labeled inference. Do not award full points for a dimension unless the evidence is direct and relevant.

## Scoring Dimensions

| Dimension | Max | What to Evaluate |
|---|---:|---|
| Product / scenario fit | 25 | The prospect's products, use cases, workflows, or customers align with the user's product or solution scope. |
| Technical solution fit | 20 | The prospect's apparent stack, architecture, integration needs, equipment, software, or technical constraints match what the user's company can support. |
| Pain point and trigger relevance | 20 | There are visible growth signals, operational challenges, compliance needs, modernization needs, new launches, hiring, expansion, or other triggers that make outreach timely. |
| Contact role relevance | 15 | The named contact's role plausibly owns, influences, evaluates, or can route the problem being discussed. |
| Timing and priority | 10 | The account appears active, reachable, in-market, expanding, launching, hiring, or otherwise likely to respond now. |
| Evidence confidence | 10 | Claims are backed by current public sources or user-provided facts rather than broad assumptions. |

## Priority Tiers

| Score | Tier | Recommendation |
|---:|---|---|
| 80-100 | P1 | Prioritize outreach. Use a highly tailored message and a normal sales follow-up cadence. |
| 60-79 | P2 | Contact if capacity allows. Keep the email consultative and verify fit early. |
| 40-59 | P3 | Nurture or research more before active selling. Use a light-touch exploratory message only if there is a strong reason. |
| 0-39 | P4 | Do not actively sell now. Track the account or ask for more information before outreach. |

Apply hard caps after calculating the numeric score. The final priority cannot exceed the capped tier even when the raw score is higher.

## Hard Caps and Downgrades

| Condition | Maximum Priority | Required Handling |
|---|---|---|
| No official source for the prospect can be found | P2 | Mark evidence confidence low and avoid strong product claims. |
| Prospect website or identity cannot be verified | P4 | Do not score beyond a research note unless the user provides credible information. |
| No prospect product, service, solution, or workflow evidence | P3 | Do not claim fit; ask a routing or research question. |
| Only same broad industry, no specific workflow or technical evidence | P3 | Use nurture/research angle, not a product recommendation. |
| No contact role is provided | P3 | Score contact role conservatively and write routing-oriented outreach. |
| Contact appears unrelated to the topic | P3 | Ask for the right owner instead of pitching. |
| Low evidence plus high technical claims would be required | P3 | Mark high risk and remove unsupported technical promises. |
| Sensitive industry with weak evidence, such as medical, financial, public sector, defense, or critical infrastructure | P3 | Use restrained language and compliance-oriented questions. |
| User company information is missing | No score | Output missing information checklist only. |
| Prospect information is missing | No score | Output generic ICP hypothesis only; do not draft sales emails. |

## Evidence Labels

Use these labels in scoring rationale:

- **Sourced fact:** Directly supported by public source or user-provided material.
- **Reasonable inference:** Plausible conclusion from visible product, hiring, messaging, or technical clues.
- **Unknown:** Important factor is not available.
- **Weak signal:** Some relevance exists but is not enough to rely on for a sales claim.

## Source Notes

For each important claim, record the source type and freshness:

- Official prospect source: company website, product page, press release, annual report, job post, or official social channel.
- Official user-company source: user-provided material, company website, product page, case study, or datasheet.
- Third-party source: news, directory, marketplace listing, public database, or analyst page.
- Inference: conclusion drawn from visible evidence; do not present it as fact.

When public pages conflict, prefer official and recent sources. If the evidence is older than 24 months or no date is visible, mark the evidence confidence lower unless the fact is stable.

## Evidence Strength Matrix

Before scoring, map important claims into this matrix:

| Evidence strength | Use in scoring | Outreach wording |
|---|---|---|
| Official fact | Can support direct scoring and specific observations. | "I noticed on your website..." |
| Third-party fact | Can support context but should be cross-checked. | "Public sources suggest..." |
| Weak signal | Can support hypotheses only. | "If this is relevant..." |
| Inference | Can guide questions, not claims. | "I wanted to understand whether..." |
| Unknown | Should lower confidence or trigger a missing-info question. | Do not mention as fact. |

## Scoring Discipline

- Penalize missing evidence in the evidence confidence dimension rather than inventing facts.
- If the user's company fit depends on a capability not shown in the provided information, mark it as a question to verify.
- Do not use the user's product category alone as proof of fit; tie the score to a prospect workflow, product line, project signal, technical requirement, or role.
- Apply hard caps even if the raw score appears high.
- Prefer a lower priority when confidence and business fit disagree.
- A high technical fit with no visible buying trigger should usually be P2, not P1.
- A promising company with an irrelevant contact should lose points under contact role relevance and receive a routing-oriented email.
- If the account is low fit, the email should ask a research or routing question, not pitch a solution.

## Account Development Decision

After scoring, explicitly decide whether the prospect is worth developing as a customer or partner.

| Tier | Account-development meaning | Outreach angle |
|---|---|---|
| P1 | Strong development target. The prospect has clear product/solution overlap, credible triggers, and a plausible buying or partnership path. | State a clear cooperation intent and propose a focused exchange around the highest-fit scenario. |
| P2 | Worth developing, but fit or timing must be verified. | State the intent to explore cooperation or relevant solution fit, then ask one qualifying question before introducing details. |
| P3 | Possible long-term nurture target. Current fit is uncertain or evidence is weak. | Use a light-touch research or routing email. Avoid product recommendations unless the user specifically asks. |
| P4 | Not a current development target. | Do not write an active sales sequence unless the user insists; recommend monitoring, enrichment, or finding a better contact. |

## Email Calibration by Score

- For scores 80-100, the first email may mention a specific cooperation direction because account fit is strong.
- For scores 60-79, the first email may state the sender is exploring cooperation or relevant product/solution/service fit, but must ask a qualifying question before describing offerings.
- For scores 40-59, the first email should focus on learning, routing, or permission to send context later.
- For scores below 40, recommend not sending a sales email; if a message is required, keep it as a neutral research inquiry.
