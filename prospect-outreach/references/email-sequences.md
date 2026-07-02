# Consultative Outreach Email Sequences

Draft gradual outreach. The sequence should feel like an informed business-development inquiry: clear about the intent to explore cooperation or fit, but restrained enough that it does not become an immediate product pitch.

## Language Selection

- Always generate two versions of the outreach sequence: a prospect-local language version and an English version.
- Use the user's requested language as the prospect-local language when specified.
- Otherwise infer the prospect-local language from the prospect website, company location, contact region, or business context.
- If unclear, default the prospect-local language to Chinese.
- The English version is required even when the prospect-local language is already English; in that case, output one polished English sequence and label it as both local and English rather than duplicating identical text.

## Sequence Structure

### Initial Email

Purpose: open a conversation and, when the score supports it, transparently state the sender's cooperation or fit-exploration intent.

Rules:
- Mention one specific, non-sensitive observation about the prospect.
- State the sender's intent in a restrained way, such as exploring potential cooperation, understanding whether a relevant product/solution/service direction fits, or finding the right team to discuss a possible match.
- Ask one low-pressure qualifying question about their current priority, workflow, technical direction, evaluation criteria, ownership, or openness to relevant context.
- Do not introduce a detailed product pitch, pricing, broad catalog, unsupported ROI claim, or aggressive demo request.
- Do not attach decks, request a demo, or ask for a meeting as the main CTA unless the user explicitly asks.

Recommended timing: Day 0.

### Follow-Up 1

Purpose: add light value and clarify relevance.

Rules:
- Send after 3-5 business days.
- Refer back to the initial question.
- Add one useful insight, comparison, or operational angle related to the prospect's business.
- Ask whether the topic is owned by the recipient or someone else on the team.

### Follow-Up 2

Purpose: introduce the user's relevant capability gently.

Rules:
- Send 7-10 business days after follow-up 1.
- Briefly connect one user-company capability to the prospect's possible scenario.
- Use conditional language: "if this is relevant", "if you are evaluating", "if your team is looking at".
- Ask whether it would be useful to exchange context, not whether they want to buy.

### Final Follow-Up

Purpose: close the loop politely.

Rules:
- Send around 14 calendar days after follow-up 2.
- Acknowledge it may not be a current priority.
- Offer to reconnect later or be routed to the right person.
- Do not use guilt, urgency, false scarcity, or pressure.

## Email Output Fields

For P1-P3 accounts, output every email in both the prospect-local language version and the English version with:

- Subject
- Body
- Personalization basis
- Recommended send timing
- Follow-up interval

For P4 accounts, do not write a normal four-email sales sequence by default. State that active outreach is not recommended. If the user explicitly still wants a message, output only one neutral research or routing note in both languages with the same fields above, and omit follow-up pressure.

## Tone Rules

- Be concise: usually 80-150 words per email unless the user asks for long-form.
- Use plain language and one clear ask.
- Avoid exaggerated claims, buzzwords, and broad product catalogs.
- Do not imply privileged knowledge of the prospect's systems.
- Do not cite scraped personal details unless they are business-relevant and public.
- Keep the sender credible by saying less, but making the observation precise.

## Example Progression

1. Initial: "I noticed your team is working in [specific area]. How are you currently thinking about [workflow or technical challenge]?"
2. Follow-up 1: "Teams in this area often compare [approach A] and [approach B]. Is that evaluation happening in your team?"
3. Follow-up 2: "If [scenario] is relevant, our team may have useful experience around [capability]. Would it be useful to compare notes?"
4. Final: "I will close the loop for now. If this becomes relevant later, I would be glad to reconnect or speak with the right colleague."


## Score-Based Email Strategy

Use the final score and priority tier before drafting:

- **P1 / 80-100:** Write with a confident cooperation angle. The first email may name the most relevant solution area, but should still ask whether it matches current priorities.
- **P2 / 60-79:** Write as fit exploration. The first email may say the sender is exploring potential cooperation or whether a product/solution/service direction is relevant, but should avoid listing products until the recipient confirms the topic.
- **P3 / 40-59:** Write as research or routing. Ask who owns the topic or whether it is relevant later; avoid recommending products directly.
- **P4 / below 40:** Recommend not sending an active sales sequence. If the user explicitly still needs a message, write a neutral information-gathering note, not a sales email, and do not create repeated follow-ups unless asked.

The first email can be explicit about intent, but not pushy. Good intent phrases include:

- "想了解贵司是否有相关方向的合作空间"
- "想判断我们在某一类场景上是否有交流价值"
- "希望先请教这个方向是否由您或相关团队负责"
- "I am reaching out to understand whether there may be a relevant cooperation angle"
- "I wanted to check whether this solution area is something your team is evaluating"

Avoid phrases that make the email feel like a hard sell:

- "我们可以立刻帮贵司解决"
- "请安排演示"
- "我们是最佳供应商"
- "This will reduce your costs by X%" unless sourced and specific.
