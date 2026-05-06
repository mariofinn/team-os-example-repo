# Supplier Pain Points — Cross-Supplier Synthesis
**Last updated:** 2026-04-16
**Interviews:** 4 — Nissan x2, Renault x1, MG x1
**Sources:** Full transcripts read via Granola

---

## 1. Everything runs on Excel and email — painful at scale
**Frequency:** 4/4

Every OEM manages vehicle data, price approvals, and status updates via CSV or email today. It works at current volumes. It breaks as FINN's fleet grows. Christoph (Nissan): "von mir aus geborene ich euch ab morgen jeden Tag hundert Autos. Ist nicht das Problem." The bottleneck is process and pricing, not willingness. Kirsten (Renault) has been running a manual FCM workaround for 3 years — nobody has fixed it because other markets have priority. Stefan (MG) manually exports CSV from Salesforce to AutoProf for every batch.

---

## 2. Lean teams everywhere — no room for new manual work
**Frequency:** 4/4

- MG: Stefan + 0.5 colleague for 7,000+ vehicles
- Nissan: Christoph relies entirely on DEKRA operationally — "operativ mach ich gar nix"
- Renault: Kirsten submits manual minimum prices to BCA monthly because FCM automation is broken

Any integration that adds steps on the OEM side will be quietly abandoned. The pitch has to be zero-touch from their end.

---

## 3. Vehicle blocking without visibility is an active problem
**Frequency:** 2/4 (Nissan directly; Renault implied)

Christoph named a specific incident: cars blocked for FINN for weeks that FINN no longer wanted. Nissan had no visibility and couldn't sell them elsewhere. "Die hätten wir vielleicht in der ganzen Zeit schon verkaufen können." Renault has a related version: no visibility on FINN fleet vehicles in FCM until appraisal, invoice, and docs are complete — no pre-sale or reservation possible without a custom integration.

---

## 4. Document management is a persistent bottleneck
**Frequency:** 3/4 (MG most acutely; present at Nissan/Renault via DEKRA)

MG: Letters, Fahrzeugscheine, and keys split across two compounds with no central system. Stefan is still a manual relay between AutoProf and the compound teams. He's actively working to remove himself from this flow. Nissan and Renault manage this via DEKRA — less painful, but the underlying complexity is the same.

---

## 5. Pricing requires OEM sign-off — automation doesn't remove control
**Frequency:** 4/4

- Nissan: Christoph escalates to Finance Director for large deviations from residual value
- Renault: Kirsten's Finance team reviews every payment before release
- MG: Stefan auto-rejects/accepts within thresholds, manually reviews everything in between

Build fast approval flows. Never remove the OEM's final say.

---

## 6. System fragmentation creates errors
**Frequency:** 3/4

- MG: Salesforce wasn't configured for re-marketing vehicles — required custom dev. Wrong compound assignments caused logistics errors.
- Renault: FCM pricing automation "funktioniert noch nicht so rein" — Kirsten manually corrects monthly.
- Nissan: UWMS/Lineos (DEKRA system) not connected to FINN — status updates are email-based.

---

## 7. No pre-return visibility — FINN gets supply after primary channels have first pick
**Frequency:** 2/4 (MG and Renault directly)

MG is launching a pre-sale model: vehicles listed on AutoProf 3-4 months before physical return. Renault's pre-marketing (dealer feedback round) started March 2026. In both cases FINN is currently not in the pre-sale window — it only sees vehicles after the primary channel has had first pick. Getting into the pre-sale window is a meaningful supply advantage.

---

## Appendix: Interview Sources

| Interview | Granola ID | Date |
|-----------|------------|------|
| Nissan x FINN v1 | 1c83d4fb-d1a3-453f-84bd-c02ba42a606d | Jan 30, 2026 |
| Finn/Nissan Follow-up | ded273d2-a26f-437f-a5f2-fe1e3ca743fe | Feb 4, 2026 |
| FINN x Renault Produkt Interview | 0c72ff18-89c3-44ec-a275-aa6ed5211c00 | Feb 19, 2026 |
| FINN & MG Austausch | 9b3dec34-b367-4e68-9147-86fc20765123 | Apr 14, 2026 |
