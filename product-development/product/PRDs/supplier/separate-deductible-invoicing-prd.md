# Separate Deductible Invoicing — PRD

**Status:** Draft (Stage: Team Kickoff)
**Author:** Mario Schiefer (PM) · Ana Costa (Product Engineer)
**Pillar:** supplier
**Last updated:** 2026-04-28 (Confluence v4)
**Related:** [Confluence PRD](https://finn.atlassian.net/wiki/spaces/FP/pages/4824694814/PRD+Separate+Deductible+Invoicing) · [Solution Design](../../../engineering/rfcs/supplier/separate-deductible-invoicing-rfc.md) · [Confluence Design](https://finn.atlassian.net/wiki/spaces/FP/pages/4828463224/Design+Separate+Deductible+Invoicing) · Jira epic [FRT-1986](https://finn.atlassian.net/browse/FRT-1986)

---

## 1. Hypothesis

Buyback Partners currently receive a single invoice that bundles the car price with all deductibles (damage, mileage, age). Since outgoing invoice item types require a valid appraisal before any invoice can be issued, cars sit uninvoiced for an average of **~3 weeks post-return**. This extends the finance period and increases interest costs.

> **If we** split invoicing into two separate documents (car invoice upon return, deductible credit note / invoice after appraisal), **then** we can invoice the car up to 3 weeks earlier per unit, **because** the car price is known at return and does not depend on the appraisal outcome.

**Supporting evidence:**

- Avg. time from return to approved appraisal: **~3 weeks**
- Estimated bottom-line impact for opted-in Buyback Partners: **>€100k for Feser**, **>€1M** if other partners are included
  - Feser (VW Brands) — €3.75/day × 894 incoming cars × 21-day potential
  - Skoda — €3.75/day × 42 incoming cars
  - Seat — €3.75/day × 284 incoming cars
  - Cupra — €3.75/day × 568 incoming cars

---

## 2. Strategic Fit

Directly supports FINN's profitability goal by end of 2026. Reduced finance period = lower interest cost per car. Pure bottom-line initiative with no dependency on volume growth.

**Impact sizing:**

- Finance period reduction: up to 3 weeks per car for opted-in partners
- Revenue impact: **>€1M projected for 2026** (to be validated)
- Confidence: **Medium** (depends on partner opt-in rate, average car value, and partners not pushing back)

**Alternatives considered:**

| Alternative | Why not |
|-------------|---------|
| Keep single invoice, speed up appraisal process | Appraisal timeline is largely external (partner-side logistics). Hard to compress reliably. |
| Manual workaround for high-volume partners only | Not scalable, creates operational overhead. |

---

## 3. Approach

**Two-document model:**

| Trigger | Document | Category |
|---------|----------|----------|
| Car return | Car invoice | WHOLESALE |
| Approved appraisal | Credit note (we owe partner) — negative invoice amount | CLAIMS |
| Approved appraisal | Invoice (partner owes us) — positive invoice amount | FINANCING |

**Technical approach:**

- Separate invoice creation triggered automatically once an approved appraisal exists
- Payout triggered automatically based on `payment_terms_days` from the contract (same terms as for the car invoice)
- Expose separate invoice in invoicing retool

**Opt-in model:** Feature configured per Order based on the `xxx_invoice_item_type` setting (`damage_invoice_item_type`, `mileage_invoice_item_type`, `age_invoice_item_type`). A new enum value `outgoing_separately` carves the specific deductible into the new flow.

For the full data-model and API contract, see the [solution design](../../../engineering/rfcs/supplier/separate-deductible-invoicing-rfc.md).

---

## 4. Non-Goals

- Replacing or redesigning the existing appraisal process
- Changing how credit notes are handled for non-deductible line items
- Ensuring payout only happens after the car invoice has been paid
- Exposing the separate invoice in the partner portal

---

## 5. Success Metrics

**Primary:** Avg. days from car return to car invoice issued (target: same day as return, vs. current ~3 weeks).

**Secondary:**

- Finance cost per car for opted-in Buyback Partners (baseline TBD with Finance)
- Complaint rate from Remarketing Partners

**Guardrail:** Zero invoicing errors / mismatches on split documents for opted-in partners in the first 90 days.

---

## 6. Rollout

- Go-Live with all open Feser buyback orders by **5th May EOD**
- Monitor closely that the process works as expected
- Keep Tino informed to ensure correct booking + Victor to reflect in cash collection

---

## 7. Open Questions

- [ ] How do we ensure automated payout? Get in touch with P&R on whether we have an option to set a delay on when to pay out (Jonathan Hippe)

---

## 8. Stakeholders

| Person | Role |
|--------|------|
| Lena | CLM |
| Victor Franz | Cash collection |
| Mario Schiefer | Product |
| Tino | Accounting / bookkeeping |
| Ana Costa | Product engineer (also lead author of the solution design) |
