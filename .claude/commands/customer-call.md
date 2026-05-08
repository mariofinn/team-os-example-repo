# Customer Call Transcript Processing

You are an expert at processing customer call transcripts and extracting key insights for product management at FINN Remarketing Tech.

**Summary guidelines:** Read `.claude/skills/customer-call-summary/SKILL.md` for detailed formatting instructions.

## Task Overview

Process a customer call transcript by:
1. Determining the customer type (buyer or supplier)
2. Checking for existing customer files
3. Managing action items (update existing, add new, ask about unclear status)
4. Creating separate summary and transcript files with cross-references
5. Generating a comprehensive, detailed summary

## Step 1: Determine Customer Type

Ask the user which customer type this call relates to (or infer from context):

- **Supplier** — RaaS supplier conversations (OEMs / leasing partners — e.g. Nissan, Renault, MG)
- **Buyer** — B2B buyer / dealer conversations

Base paths for customer calls:

```
product-development/product/customers/accounts/suppliers/{name}/calls/summaries/
product-development/product/customers/accounts/suppliers/{name}/calls/transcripts/
product-development/product/customers/accounts/buyers/{name}/calls/summaries/
product-development/product/customers/accounts/buyers/{name}/calls/transcripts/
```

## Step 1.5: Granola Connectivity Check

If the user indicates the transcript is in Granola, run a connectivity check before proceeding:

1. Call `mcp__granola__list_meetings` with `time_range: "this_week"` as a test
2. If it fails or times out, tell the user: "Granola MCP isn't connected. Check that the Granola plugin is running, then try again. In the meantime, you can paste the transcript or provide a file path."
3. If it succeeds, proceed normally

Skip this check if the user pastes a transcript or provides a file path.

## Step 2: Check for Existing Customer Files

**Always check both folders before creating new files:**

1. Search `accounts/{type}/{name}/calls/summaries/` for prior summaries
2. Search `accounts/{type}/{name}/calls/transcripts/` for prior transcripts

**If files exist:**
- Review existing Open Action Items in the account-context.md
- Ask user about any items where status is unclear (e.g., "Was [action item] completed?")
- Save the new meeting as a new dated file (one per meeting, not appended)

**If no files exist:** Create the customer's account folder and the standard subfolders (`calls/summaries/`, `calls/transcripts/`, plus `account-context.md`).

## Step 3: Gather Information

Ask the user for:
- **Customer name** (supplier name or buyer/dealer name)
- **Meeting title**
- **Meeting date** (YYYY-MM-DD)
- **Meeting participants**
- **Transcript source**: Either:
  - "I'll provide the transcript" (user will paste it)
  - "It's in Granola" (search Granola for the meeting)
  - "It's in an existing file" (user will provide the file path)

## Step 4: Process and Generate Summary Content

1. Get the transcript content from the source
2. Read the summary style guide: `.claude/skills/customer-call-summary/SKILL.md`
3. Generate the **summary content** following the SKILL guide. Include:
   - Executive Summary (with inline quotes, topic headers, opportunity areas, key product gaps)
   - Insights / Learnings (organized by topic, table format with quotes)
   - Feature Requests (organized by area, table format with quotes)
   - Next Steps (organized by category with owners)
   - Follow-up Email draft
   - Slack summary draft
4. Run through the Quality Checklist from SKILL.md before proceeding

## Step 5: Write Files

### 5a. Write Summary File

Save the summary to `product-development/product/customers/accounts/{type}/{name}/calls/summaries/{YYYY-MM-DD}.md`.

Each meeting is its own file. Cross-reference the transcript at the top of the summary.

### 5b. Write Transcript File

Save the transcript to `product-development/product/customers/accounts/{type}/{name}/calls/transcripts/{YYYY-MM-DD}.md`. Cross-reference the summary at the top.

For large transcripts (>15KB), write the header via the Write tool and append the body via Python's `open(file, "a")` with triple-quoted strings (handles all special characters cleanly).

### 5c. Update account-context.md

Update the customer's `account-context.md` with:
- New insights from this call
- Updated open / completed action items
- Any change in status, blockers, or next steps

### 5d. Log Feature Requests

For each feature request surfaced in the call, file a Jira ticket in the `FRT` project with:
- Customer label (`buyer:{name}` or `supplier:{name}`)
- Pillar label (`pillar:buyer`, `pillar:supplier`, or `pillar:operations`)
- Link back to the call summary

## Step 6: Present Slack Summary Draft

Present the Slack summary draft to the user for review. Format follows the Slack Summary section in `.claude/skills/customer-call-summary/SKILL.md`.

Default channel: `#rem_tech_general` for cross-team awareness, `#rem_tech_internal` for sensitive customer detail.

## Important Notes

### Anchor links
- Use lowercase, spaces become hyphens, special characters removed
- Example: heading `# 2026-05-08 — Discovery call` → anchor `#2026-05-08--discovery-call`

### Line length
- Keep lines under 150 chars to avoid processing issues — wrap long speaker turns at sentence boundaries

### Granola Meeting ID
- When source is Granola, include `**Granola Meeting ID:** {uuid}` in the transcript header so we can re-pull or audit later
