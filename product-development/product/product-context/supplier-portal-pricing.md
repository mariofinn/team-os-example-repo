# Pricing Concepts: Normalized vs. All-In

## Normalized Price (Clean RV)
The residual value of a vehicle **without** any damage or excess mileage deductions. This is the "clean" baseline value — what the car would be worth if it had no damages and standard mileage.

- Nissan (and other OEMs/suppliers) think and communicate in normalized prices
- The Target RV that Nissan provides is always a normalized value (e.g. 55% of MSRP)
- Enables apples-to-apples comparison between different vehicles and deals regardless of condition

## All-In Price
The residual value **after** subtracting damage costs and mileage deductions. This is what the buyer actually pays — everything included.

- FINN thinks and communicates in All-In prices
- Derived from the Normalized price by subtracting deductions

## The Relationship

**Target RV direction (Nissan provides Normalized → FINN derives All-In):**
```
Normalized − Damages − KM deductions = All-In
```

**Offer/Counter direction (buyer makes All-In offer → Normalized is calculated back):**
```
All-In + Damages + KM deductions = Normalized
```

## In the Supplier Portal UI
Both values are shown in separate column groups so Target RV and Offer Price are directly comparable on a normalized basis. Tooltips on each column explain the calculation in the other direction.
