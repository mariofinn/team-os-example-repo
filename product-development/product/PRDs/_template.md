# [Feature name] — PRD

**Status:** Draft | In Review | Approved | Shipped | Deprecated
**Author:** [PM]
**Pillar:** supplier | buyer | operations
**Last updated:** YYYY-MM-DD
**Related:** [Jira epic FRT-XXX] · [Figma] · [Eng plan] · [RFC]

---

## 1. Overview

**Problem.** What pain are we solving? Whose pain — supplier, buyer, or operations?

**Goal.** What outcome counts as success? State as a metric where possible (cycle time, GPU, conversion, etc.).

**Non-goals.** What we are explicitly not solving in this scope.

---

## 2. User stories / JTBD

Use the JTBD format from `../strategy/frameworks/jtbd-canvas.md`:

> When [situation], I want to [motivation], so I can [outcome].

List 1–3 primary user stories. Identify the persona (e.g. "Compound ops lead", "Independent dealer", "OEM remarketing manager").

---

## 3. Requirements

### Must-have (P0)

- [ ] [Requirement]

### Nice-to-have (P1)

- [ ] [Requirement]

### Non-functional

- Performance / SLA targets
- Compliance / data-handling constraints
- Internationalisation / market specifics (DACH-only? EU? UK?)

---

## 4. Design

Link to Figma frames. Embed key flow screenshots. Note open design questions.

---

## 5. Technical considerations

- Architecture sketch (link to RFC for depth)
- Integration points: HubSpot / BigQuery / OEM systems / Make.com scenarios / etc.
- Data model changes
- Dependencies on other teams / services

---

## 6. Launch plan

- Rollout strategy (feature flag, % rollout, by market, by customer)
- Success criteria — how do we know it's working
- Kill criteria — when do we roll back
- Post-launch monitoring (Looker dashboard, Amplitude funnel)

---

## 7. Open questions

- [Question] — owner, target resolution date
