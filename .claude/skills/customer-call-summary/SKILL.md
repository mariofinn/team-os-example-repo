---
name: customer-call-summary
description: Customer Call Transcript Processing
---

# Customer Call Summary Style Guide

This skill defines how to summarize customer call transcripts for FINN Remarketing Tech. It applies to both **supplier** calls (OEM / leasing partners — e.g. Nissan, Renault, MG) and **buyer** calls (B2B dealer / trade-buyer accounts).

## Summary Structure

Every customer call summary should include these sections in order:

### 1. Executive Summary

A detailed overview that orients the reader and captures the key takeaways.

**Quotes:** Always weave relevant verbatim quotes directly into the executive summary paragraphs. Quotes bring the exec summary to life — this is the most-read section. Use italicized quotes inline within paragraphs (e.g., *"We need this before Q3." — Lars*), not just in insight tables.

**Opening paragraph:** Status updates and any quick wins/progress since the last meeting.

**Second paragraph:** Orient the reader: *"This call focused on X areas: (1) [topic], and (2) [topic]."*

**Topic sections:** For each major topic discussed, add a bold header and a detailed paragraph:
- `**[Topic Name]**` (e.g., "Pricing surface in supplier portal")
- Include specific context, decisions made, and any blockers

**How [Customer] is Using [Specific Feature/Workflow]:** Scope this heading to the specific features or workflows discussed on *this* call — not a comprehensive overview of all product usage.

**Opportunity Areas:** Paragraph or numbered list describing opportunities. Tie back to their workflows.

**Key Product Gaps:** Bullet list of gaps with specific descriptions. Actively identify *implied* feature gaps — things the customer is working around, doing manually, or switching to another tool for. Don't just capture what they explicitly request; listen for pain points that imply a missing capability.

```markdown
**Key Product Gaps**
- **[Gap 1]:** [Specific description with context]
- **[Gap 2]:** [Specific description with context]
```

### 2. Insights / Learnings

Organize insights by topic. Each topic section includes:

**Topic heading (H3):** Group related insights together
**Summary:** 1–2 sentence summary of what we learned in this topic area
**Table format:**

```markdown
| Insight | Details |
|---------|---------|
| **[Insight headline]** | [Detailed description with specific examples from the call]<br><br>*"[Verbatim quote]" — [Speaker]* |
```

**Level of detail:** Include enough context that someone who wasn't on the call understands:
- The "why" behind the insight, not just the "what"
- Specific examples mentioned
- Multiple quotes if they add different perspectives

### 3. Feature Requests

Organize feature requests by area:

```markdown
| Feature | Details |
|---------|---------|
| **[Feature name]** | [Detailed description]<br><br>*"[Verbatim quote]" — [Speaker]* |
```

Note any **Blockers** above the table where they affect the request.

### 4. Next Steps

Organize action items by category, with owners:

```markdown
## Next Steps

### [Category] (e.g., "Onboarding", "Pricing model")
- [Action item] — [Owner]
- [Action item] — [Owner]
```

### 5. Follow-up Email

Draft a follow-up email to send to the customer contact:

```markdown
## Follow-up Email

**To:** [Customer contact]
**Subject:** [Meeting Topic] Recap + Action Items

Hi [Name],

Thanks for the discussion today. Here's a quick recap:

**What we covered:**
- [Key topic 1]
- [Key topic 2]

**Action items for you:**
- [ ] [Item 1]
- [ ] [Item 2]

**From our side:**
- [Item 1]
- [Item 2]

Let me know if I missed anything.

Best,
[Your name]
```

### 6. Slack Summary

Draft a ready-to-post Slack message summarizing the call for internal stakeholders.

**Format:**
- Opening line: "Great [frequency] sync with [Customer] today. Full recap: [link]"
- Bold topic headers for each major area
- Detailed paragraphs covering each major topic with inline customer quotes
- Numbered lists for specific fixes or action items
- End with "Jira tickets to come for all items raised above." when applicable

**Content guidelines:**
- Hit ALL key takeaways — be specific (list every fix, not "a couple of fixes")
- Include quotes that capture enthusiasm, frustration, or key feedback
- Include metrics or data points discussed
- Note when the customer is already taking action

## Action Item Management

Action items are tracked in the customer's `account-context.md` (one file per account), not per-meeting.

### account-context.md tables

Maintain these tables in each customer's `account-context.md`:

```markdown
## Open Action Items

### FINN
| Action Item | Owner | From Meeting |
|-------------|-------|--------------|

### [CustomerName]
| Action Item | Owner | From Meeting |
|-------------|-------|--------------|

## Completed Action Items

### FINN
| Action Item | Owner | From Meeting | Completed |
|-------------|-------|--------------|-----------|

### [CustomerName]
| Action Item | Owner | From Meeting | Completed |
|-------------|-------|--------------|-----------|
```

### Each meeting: update the tables

1. Review existing Open Action Items against what was discussed
2. Ask user about unclear status — e.g. "Was [action item] completed?"
3. Move completed items to the Completed table with completion date
4. Add new action items from this meeting to the Open tables

## Verbatim Guidelines

1. **Always italicize** with speaker attribution: *"Quote text" — Speaker*
2. **Put quotes on separate lines** in tables using `<br><br>` before the quote
3. **Choose quotes that are:** specific, particularly revealing of customer needs, supporting evidence for key insights
4. **Keep quotes concise** — trim to the essential part if needed
5. **Preserve exact wording** — don't paraphrase within quotes
6. **Include multiple quotes** when they add different perspectives

## Level of Detail

The summary should be detailed enough that someone who wasn't on the call understands the full picture:

- Include specific examples from the call
- Capture the "why" behind insights, not just the "what"
- Use real examples mentioned by the customer
- Provide context for feature requests (what problem they solve, who needs them)
- Note blockers and dependencies that affect next steps

## Quality Checklist

Before finalizing the summary, verify:

- [ ] Executive Summary has opening status paragraph + topic focus paragraph
- [ ] Executive Summary includes bold topic headers with detailed paragraphs
- [ ] Executive Summary includes relevant verbatim quotes woven into paragraphs
- [ ] Feature/workflow headings are scoped to this call (not a comprehensive product-usage overview)
- [ ] "Opportunity Areas" ties opportunities back to current workflows
- [ ] "Key Product Gaps" has specific descriptions with context
- [ ] Implicit feature gaps identified (not just explicit requests)
- [ ] Insights organized by topic with Summary paragraphs
- [ ] Insights use table format with quotes on separate lines (`<br><br>`)
- [ ] Feature Requests organized by area with Summary paragraphs
- [ ] Blockers noted where applicable
- [ ] Next Steps organized by category with owners
- [ ] Follow-up Email drafted with recap and checkbox action items
- [ ] Slack summary drafted (note channel: `#rem_tech_general` for cross-team, `#rem_tech_internal` for sensitive)
- [ ] Action item tables in `account-context.md` updated (completed moved, new added)
- [ ] Feature requests filed as Jira tickets in `FRT` with customer + pillar labels
