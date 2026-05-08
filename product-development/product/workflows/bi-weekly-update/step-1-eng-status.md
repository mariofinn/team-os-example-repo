# Step 1: Engineering Status

## Goal

Produce the "What the Team Is Building Now" section with OKR/workstream tables showing current status.

---

## Automated Part

### 1. Pull completed tickets

Query Jira for issues completed in the last 2 weeks.

**Filters:**
- Project: `FRT`
- Board: 245
- Status: completed (Done / Released / equivalent terminal status)
- Updated: last 14 days

### 2. Map issues to OKR workstreams

Read the current trimester OKR file (`../../strategy/okrs-tN-YYYY.md`). Categorize each completed Jira issue into the relevant Key Result / workstream.

If an issue doesn't map cleanly, surface it for the PM in the interactive part.

### 3. Generate draft status tables

For each Key Result / workstream, draft a status update based on what was completed and what appears to be in progress (not-yet-done tickets in active sprints).

---

## Interactive Part

### 4. Present ticket summary to PM

Show:
- List of completed issues grouped by workstream / KR
- Any issues that don't map cleanly to existing workstreams
- Draft status tables

### 5. Ask for additional context

Prompt: **"Dump any additional context — decisions, meeting outcomes, status changes, things not in tickets."**

The PM will provide a single context dump. This is the primary source for nuanced status updates that Jira can't capture (e.g., "Design complete but eng hasn't started" or "Blocked on legal review of the Nissan contract").

### 6. Synthesize and draft

Combine ticket data + PM's context into the full "What the Team Is Building Now" section:
- Opening paragraph framing the trimester's objectives
- One table per Key Result / workstream
- "Designs Complete" list (if applicable)
- Pillar-level rollups if useful (supplier / buyer / operations)

### 7. Write to output file

Write the section to the dated output file. Present draft for review before moving to Step 2.

---

## Output Format

```markdown
# {Month YYYY}: What the Team Is Building Now

[Opening paragraph: What we're trying to move this trimester, anchored to the OKRs.]

## {KR1 name}

**Goal:** [from OKRs]

| Workstream | Why It Matters | Status |
|---|---|---|
| **[Workstream]** | [Business impact] | [Current status] |

## {KR2 name}

**Goal:** [from OKRs]

| Workstream | Why It Matters | Status |
|---|---|---|
| **[Workstream]** | [Business impact] | [Current status] |

## Designs Complete (Ready for Engineering)

- [Item 1]
- [Item 2]
```

---

## Notes

- The OKR goals don't change within a trimester. Only the workstream rows and status column change cycle to cycle.
- If a new workstream appears (not in previous cycle), add it and flag it to the PM.
- If a workstream is complete and shipped, move it out of the table and note it in the opening paragraph or a "Shipped" section.
