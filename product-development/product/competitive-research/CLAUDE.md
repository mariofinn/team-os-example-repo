# Competitive Research

Competitive intelligence for FINN Remarketing Tech — tracking RaaS platforms, dealer auction tools, and other vehicle remarketing competitors.

## Where to start

The current overview lives in [`../customers/research/competitive-raas-platforms.md`](../customers/research/competitive-raas-platforms.md). When per-competitor depth is needed, drop a folder under `competitors/{competitor-slug}/` with `tldr.md` + `pricing.md`.

## Folder Structure

```
competitive-research/
└── competitors/
    └── {competitor-slug}/
        ├── tldr.md            # 1-page summary: what they do, strengths, weaknesses, differentiation
        ├── pricing.md         # Pricing model, tiers, comparison to FINN
        └── images/            # Optional: screenshots, pricing pages
```

## What to track

| Dimension | Why it matters |
|-----------|---------------|
| Coverage | Do they cover supplier / buyer / operations, or just one slice? |
| Geographies | Active in DACH? EU-wide? UK? Global? |
| Pricing model | Take-rate vs. SaaS vs. listing fee — implications for our supplier pitch |
| Inventory model | Do they carry inventory or pure marketplace? |
| Trust mechanisms | Inspections, condition reports, dispute resolution |
| Integration depth | OEM/DMS integrations they advertise |

## When to Update

- After competitive deal wins/losses (supplier or buyer side)
- When a competitor launches a notable feature
- After supplier or buyer calls where competitors are mentioned
- Quarterly review of pricing and positioning
