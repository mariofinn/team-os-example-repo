# Step 3: Customer Updates

## Goal

Update customer / pilot exec summaries, deep dives, and the cross-customer summary if new call data changes the narrative.

---

## Automated Part

### 1. Identify customers with new calls

Check which active suppliers and buyers had calls in the last 2 weeks (from Step 2 data).

The list of "active" accounts changes — read each account's `account-context.md` to determine current pilot/onboarding/active status. Don't hardcode account names here; let the folder structures under `../../suppliers/accounts/` and `../../buyers/accounts/` be the source of truth.

### 2. Compare new data against existing sections

For each customer with a new call, read the existing exec summary and deep dive from the previous bi-weekly output. Compare against the new call summary to identify:

- **New pain points** not covered in the existing write-up
- **New use cases** observed since last update
- **New feature gaps** surfaced in the call
- **Changed satisfaction signals** (more positive, more negative, or new concerns)
- **New quotes** that are stronger than existing ones
- **Status changes** (pilot expanded, timeline shifted, new stakeholders, etc.)

### 3. Flag changes

For each customer, prepare a summary of what's new:
- List specific changes with before/after context
- Note whether changes affect the exec summary, deep dive, or both
- Note whether the cross-customer summary needs updating

---

## Interactive Part

### 4. Present changes per customer

For each customer with new data, present:

**"Here's what's new for [Customer] since the last update:"**
- [List of specific changes]
- **Recommendation:** [Update exec summary / Update deep dive / No update needed]

Ask: **"Should we update the exec summary and/or deep dive?"**

### 5. Draft updates if approved

If the PM approves updates:
- Draft the updated sections
- Present for review
- Write to the output file

### 6. Check cross-customer summary

If customer sections changed, check whether the cross-customer summary still accurately reflects:
- Shared feature gaps
- Conversion path
- Buyer / supplier ICP characterization

Ask: **"The cross-customer summary currently says [X]. Based on [new data], should we update it?"**

### 7. Write to output file

Write updated customer sections and cross-customer summary to the dated output file.

---

## When to Carry Forward vs. Rewrite

### Carry forward (copy from previous cycle)
- Background sections (company overview, team structure)
- Pain points that haven't changed
- Feature gaps that haven't been addressed or newly validated
- Existing quotes that are still the best available

### Rewrite
- Exec summary opening paragraph (should reflect current state)
- "Use Cases Today" if new use cases emerged
- Feature gap status if engineering progress changed the situation
- Any section where a stronger quote replaced a weaker one

### Add new
- New feature gaps surfaced in calls
- New pain points or use cases observed
- New pilot or active accounts

---

## Cross-Customer Summary Structure

The cross-customer summary sits between "Customer Calls" and the first customer section. It covers:

1. **Combined business impact** (volume, revenue / GHG-quota / GPU contribution, % of OKR target)
2. **Shared persona** (supplier-side OEM characterization or buyer-side dealer characterization)
3. **Shared feature gaps** (table with per-customer needs and status)
4. **Emerging product direction** (next investment areas)
5. **Per-customer unique needs** (bullets)

---

## Notes

- Customer sections are the most labor-intensive part of the bi-weekly. Most cycles need only minor updates or none at all.
- If a customer hasn't had a call in the last 2 weeks, carry forward the existing sections unchanged.
- If a new customer becomes a pilot, create a new exec summary and deep dive following the format of the most recent active pilot.
