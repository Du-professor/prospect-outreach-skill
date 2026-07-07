---
name: prospect-outreach
description: >
  Analyze a user's company and prospective customer companies in depth,
  including product content, service content, solution content, technical fit,
  and account development potential, then draft score-aware consultative
  outbound email sequences. Use when the user asks for prospect analysis,
  customer matching, lead qualification, outreach email drafting, sales email
  drafts, account research, potential customer fit scoring, consultative
  outbound sales, partner development, or gradual follow-up sequences. Also
  use for Chinese requests such as 潜在客户分析, 客户匹配, 外联邮件, 拓客邮件,
  销售邮件草稿, 客户开发, and 合作伙伴开发. Inputs may include the user's
  company website or description, prospect websites or descriptions, contact
  names/roles, target market, preferred language, and relevant product lines.
---

# Prospect Outreach

Use this skill to turn company and prospect information into a fit analysis and a gradual, personalized outreach sequence. The goal is consultative business development: understand the prospect first, ask low-pressure questions, and only introduce the user's relevant products after a fit has been established.

## Required References

- Load `references/matching-framework.md` before scoring fit or assigning priority.
- Load `references/email-sequences.md` before drafting any email sequence.
- Load `references/compliance-rules.md` before drafting outreach or compliance notes.
- Load `references/research-sources.md` before researching companies, judging evidence strength, or handling missing information.

## Core Workflow

1. **Identify inputs and decide whether to proceed.** Extract the user's company website or description, prospect company website or description, contact details, target market, preferred language, outreach scenario, and any product line constraints. If the user's company information is missing, stop and output only the missing information checklist. If prospect information is missing, output only a generic ICP fit hypothesis and missing information checklist; do not score or draft outreach. If contact role is missing, continue but score `Contact role relevance` conservatively and write routing-oriented outreach.
2. **Research current facts.** When URLs, company names, or public claims are provided, gather current public information using available web tools and `references/research-sources.md`. Prefer official company pages, product pages, public news, and credible business sources. Separate sourced facts from interpretation, include source freshness when it affects confidence, and build an evidence strength matrix. If browsing is unavailable, use only the provided material and state that limitation.
3. **Profile the user's company.** Summarize relevant products, technical capabilities, target use cases, differentiators, and proof points. Focus only on capabilities that could matter to the prospect.
4. **Profile each prospect deeply.** Produce a detailed account profile covering company role, business model, product content, service content, solution content, target industries, application scenarios, likely customers, technical architecture or stack clues, buying organization, current signals, possible pain points, and partnership/customer-development potential.
5. **Match, score, and judge developability.** Use `references/matching-framework.md` to score the account on six dimensions and apply hard caps or downgrade rules before assigning priority. Decide whether the user's company can realistically develop the prospect into a customer, channel partner, technical partner, distributor, or long-term nurture account. Explain what is known, inferred, unknown, strong, and weak.
6. **Draft score-aware outreach.** Use `references/email-sequences.md` and `references/compliance-rules.md` to generate two gradual email packages: one in the prospect-local language and one in English. Calibrate the first email to the score and outreach scenario. It may transparently state the sender's intent to explore cooperation, partnership, or relevant product/solution/service fit, but it must not hard-sell products, make unsupported claims, or push a demo before confirming relevance. For P4 accounts, do not force an active sales sequence; provide a neutral research note only when the user explicitly still wants a message.
7. **Prioritize action.** Assign P1/P2/P3/P4 priority, recommend whether to contact now, and provide a sending cadence. Do not send emails, connect to inboxes, or prepare bulk-spam workflows.

## Output Format

Always return these sections:

For multiple prospects, start with an account priority table:
- Company
- Fit score
- Priority
- Best angle
- Missing evidence
- Recommended next action
- Follow-up date or research action

### Customer Profile Analysis
Provide a detailed analysis, not a short summary. Cover:
- Company role, business model, market position, and relevant locations or business units
- Product content: major product lines, equipment, software, platforms, or deliverables
- Service content: lifecycle services, engineering services, support, training, maintenance, modernization, consulting, or managed services
- Solution content: end-to-end solutions, system integration, digitalization, automation, AI, inspection, logistics, monitoring, or industry-specific packages
- Technical solution or likely architecture
- Application scenarios and target customers or users
- Buying organization and likely decision influencers
- Possible pain points, buying triggers, current initiatives, and constraints
- Evidence, assumptions, unknowns, and source freshness

### Evidence Strength Matrix
List the important conclusions with:
- Claim
- Evidence strength: official fact, third-party fact, weak signal, inference, or unknown
- Source or reason
- Confidence impact

### Our Fit Analysis
- Relevant user-company products, services, and solutions
- Direct matching points by prospect product/service/solution area
- Potential entry points for cooperation, partnership, or customer development
- Non-matching points, competitive constraints, or weak evidence
- Whether the prospect can realistically be developed as a customer or partner, with rationale
- Recommended account-development angle
- Questions to verify before selling
- Reasons not to contact now when fit is P3/P4, what information would change the recommendation, and which role would be better to find

### Fit Score
Use a table with the six scoring dimensions from `references/matching-framework.md`, including max score, assigned score, rationale, evidence type, and any hard cap or downgrade applied.

### Outreach Priority
State the priority tier, whether to contact now, whether the prospect is worth developing as a customer or partner, why, and the suggested first action. The email angle must follow the score tier guidance in `references/matching-framework.md`.

### Email Package
For P1-P3 accounts, provide both a **Prospect-local language version** and an **English version**. For each email in each language, provide:
- Subject
- Body
- Personalization basis
- Recommended send timing
- Follow-up interval

Include four emails in each language: initial email, follow-up 1, follow-up 2, and final follow-up.

For P4 accounts, state that active outreach is not recommended. If the user explicitly asks for a message anyway, provide only a neutral research or routing note in the prospect-local language and English, and explain why a sales follow-up sequence is withheld.

### CRM Fields
Return compact CRM-ready fields:
- ICP fit
- Pain hypothesis
- Buying trigger
- Decision maker guess
- Best outreach scenario
- Next step
- Risk
- Email angle
- Follow-up date

### Pre-send QA
Run the checklist in `references/email-sequences.md` and state pass/fail for each item. Revise drafts before final output when an item fails.

### Compliance and Risk Notes
State any data gaps, inferred claims, compliance risks, consent/opt-out considerations, sensitive-industry concerns, and restraint rules from `references/compliance-rules.md`. Do not fabricate relationships, private knowledge, customer logos, metrics, or case studies. Do not imply the sender inspected non-public systems. If evidence is weak, keep the email exploratory.

## Quality Rules

- Keep outreach human, specific, and brief. Avoid generic "we are a leading provider" openings.
- Lead with the prospect's context and a clear cooperation intent, not the user's product catalog.
- Ask one clear question per email whenever possible.
- Do not over-personalize from sensitive personal data.
- Do not generate deceptive subject lines, fake referrals, fake prior conversations, or pressure tactics.
- Do not use private emails, personal phone numbers, or sensitive personal information unless the user provides a lawful business reason and the contact is clearly business-relevant.
- Do not generate large-scale automated outreach, mailbox connection steps, scraping workflows, or spam-like sequences.
- For low-fit accounts, recommend nurture or research instead of forcing a sales pitch.


