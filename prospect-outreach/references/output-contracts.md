# Prospect Outreach Output Contracts

Select one mode before formatting. Use `standard` unless the user explicitly asks for a short result, deep research, batch processing, or an artifact with different requirements.

## Contents

- Brief Mode
- Standard Mode
- Deep Mode
- Batch Mode
- CRM Schema
- Artifact Rule

## Brief Mode

Return:

1. Decision snapshot
2. Account Fit Score and Outreach Readiness Score
3. Base priority, applied caps, and final priority
4. Primary opportunity path and best angle
5. Three most important evidence gaps
6. Recommended next action
7. First permitted message in the required languages, or the reason outreach is withheld

## Standard Mode

Return these sections in order:

### Input and Research Status

- User company, prospect, contact, sender, prior-contact status, research date, output mode, analysis language, and sendable languages
- Missing inputs and browsing limitations

### Decision Summary

- Whether the account is worth developing
- Account Fit, Outreach Readiness, final priority, primary opportunity path, contact-now decision, and next action

### Prospect Profile

- Company role, business model, relevant locations or business units
- Product, service, and solution content
- Applications, target customers, technical architecture clues, buying organization, current initiatives, constraints, pain hypotheses, and triggers

### User-Company Fit

- Relevant demonstrated products, services, solutions, differentiators, and proof
- Strong matches, weak matches, non-matches, competitive constraints, and questions to verify

### Evidence Ledger

Use the mandatory fields in `research-sources.md`. Standard mode may include only evidence that materially affects a score, priority, or message.

### Opportunity Path

- Primary path, credible secondary path, rejected paths, rationale, reactivation conditions, and reasons not to contact now

### Product Mapping Matrix

| Prospect scenario or need | User-company capability | Proof | Gap or risk | Verification question |
|---|---|---|---|---|

### Scores and Priority

- Account Fit table with all five dimensions
- Outreach Readiness table with all five dimensions
- Base priority, Readiness cap, hard caps, contact-status gates, final priority, and downgrade reasons

### Contact Recommendation

- Best role or team, available public business channel type, source, routing rationale, and roles to avoid
- Do not invent an address when none is public

### Outreach Package

- Apply language and sequence rules from `email-sequences.md`
- State why messages are withheld for P4 or suppressed accounts

### CRM Fields

Return the fields in the CRM schema below.

### Pre-send QA

- Report pass/fail for every required check
- List unresolved placeholders and mark affected drafts `Needs input`

### Compliance and Risk Notes

- Privacy, consent/opt-out, regional uncertainty, sensitive-industry concerns, evidence gaps, and stop-contact status

## Deep Mode

Return all Standard sections and add:

- Full evidence ledger with URLs and dates
- Detailed technical architecture and integration hypotheses
- Buying-committee map
- Likely objections and safe discovery questions
- Contact-channel comparison
- Customer, OEM, systems-integrator, channel, and technical-partnership path comparison
- Reactivation signals and 30/60/90-day research actions when contact-now is not recommended

Do not manufacture technical detail merely to make Deep mode longer.

## Batch Mode

Normalize and deduplicate before scoring. Preserve all original source names and the most restrictive contact status.

Start with:

| Normalized company | Source names | Account Fit | Readiness | Final priority | Contact status | Primary path | Best angle | Missing evidence | Next action | Next review |
|---|---|---:|---:|---|---|---|---|---|---|---|

Then:

- Deeply analyze P1/P2 accounts only unless the user explicitly requests every account.
- Give P3 accounts a short research/nurture note and reactivation condition.
- Give P4 or suppressed accounts a no-contact reason and research action.
- Do not generate a second initial message for `contacted`, `paused`, or `do not contact` records.

## CRM Schema

- Normalized account name
- Original source name
- Website and relevant business unit
- Research date
- Last verified source date
- Account Fit Score
- Outreach Readiness Score
- Base and final priority
- Primary and secondary opportunity path
- ICP fit summary
- Pain hypothesis
- Buying trigger
- Decision-maker and influencer roles
- Contact name and role, when supplied
- Contact-channel type and public source
- Contact status
- Last outreach stage and date, when supplied
- Best outreach scenario
- Email angle
- Next step
- Follow-up or next-review date
- Downgrade reason
- Risk and missing evidence
- Stop-contact status and reason

## Artifact Rule

When the user requests an `.md` file, write the complete selected-mode result to one Markdown file. Use a descriptive filename containing the prospect or batch name and research date. Do not place private contact data or non-public customer information in a public repository.
