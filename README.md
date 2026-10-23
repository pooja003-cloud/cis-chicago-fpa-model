# Funding Shock Stress Test: Communities In Schools of Chicago

> **Independent portfolio project** using public IRS Form 990 data. Not affiliated with
> Communities In Schools of Chicago. Not financial advice.

## The question
Communities In Schools (CIS) of Chicago places social workers in high-poverty Chicago
Public Schools to connect students with academic, emotional and basic-needs support.
Its expenses roughly doubled between FY2019 and FY2025, while its revenue swings with
large one-time gifts.

**If no new major gift arrives, how long do its unrestricted reserves last, and what
level of spending can it sustain?**

## The answer
_To be written once the model is complete — lead with the headline number._

![Dashboard](images/dashboard.png)

## What's inside
| Path | Contents |
|---|---|
| `excel-model/` | 5-tab Excel model (live formulas, scenario switch) |
| `reports/` | 1-page memo with findings and recommendations |
| `data/raw/` | Form 990 extracts |
| `data/processed/` | Cleaned figures used by the model |
| `data/SOURCES.md` | Every source, plus known gaps |
| `images/` | Dashboard screenshots |

### The workbook
1. **Inputs & Assumptions** — 5 years of 990 data; every assumption tagged *Filing* or *Assumption*
2. **Historical Analysis** — growth, funding mix, program expense ratio, months of reserves (total vs. unrestricted)
3. **Forecast** — 3-year driver-based forecast with a major-gift on/off switch
4. **Scenarios** — Base / No major gift / Cost discipline, plus break-even gift size
5. **Dashboard** — revenue vs. expenses, runway, funding mix, expense split

## Key assumptions
| Assumption | Value | Source | Why |
|---|---|---|---|
| _to fill in_ | | Filing / Assumption | |

## Limitations
- Form 990s are published with a lag; the latest year available is FY2025.
- The split between recurring and one-time gifts is estimated, not reported.
- The forecast depends on assumptions; it is a stress test, not a prediction.

## Why this project
I volunteer as a data science fellow at a grassroots Chicago education nonprofit, which
got me interested in how wraparound student-support organizations stay financially
sustainable.
# cis-chicago-fpa-model
