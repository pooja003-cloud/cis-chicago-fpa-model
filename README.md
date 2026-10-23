# Funding Shock Stress Test: Communities In Schools of Chicago

> **Independent portfolio project** using public IRS Form 990 data. Not affiliated with
> Communities In Schools of Chicago. Not financial advice.

## The question
Communities In Schools (CIS) of Chicago connects students in 239 Chicago Public Schools with
social, health and enrichment services through about 200 partner organizations. Its expenses
rose every year from FY2021 to FY2025, while its revenue swung with large one-time gifts.

**If no new major gift arrives, how long do its unrestricted reserves last, and what level of
spending can it sustain?**

## The answer
**CIS's recurring revenue no longer covers its costs.** The base budget ran a **$1.1M deficit
in FY2025**, and the gap widens to **$2.2M by FY2028**. Unrestricted reserves cover
**9.5 months** of expenses today but fall to **4.4 months by FY2028** even if a new $5M gift
arrives on schedule, and **below the 3-month floor** if it does not. Holding its position
requires a gift of about **$7.2M every 4 years**, 44% more than it has historically received.

![Dashboard](images/dashboard.png)

## Key findings
- **Revenue depends on large, irregular gifts.** Contributions are ~89% of revenue. Revenue went
  $4.4M → $11.1M → $7.0M (FY2021–FY2025) while expenses rose every year, $5.3M → $8.1M.
- **The cushion is thinner than it looks.** Net assets of $12.9M look like 19 months of expenses,
  but half ($6.5M) is donor-restricted and $6.4M of assets are pledges not yet received.
  Unrestricted runway fell from 15.1 months (FY2022) to 9.5 months (FY2025).
- **Efficiency is below sector guidelines.** Program services are 69–72% of spending
  (guideline 75%+); the cost to raise $1 rose from $0.10 to $0.22.

## Scenarios (unrestricted runway at end of FY2028)
| Scenario | What changes | Reserves | Runway | Below 3-month floor |
|---|---|---|---|---|
| Base | Assumptions below; next $5M gift in FY2027 | $3.5M | 4.4 mo | No |
| No major gift | No new large gift | $1.0M | 1.2 mo | FY2028 |
| Government cut | Government grants fall 50% | $2.0M | 2.5 mo | FY2028 |
| Cost discipline | Expenses grow 3% instead of 6% | $5.0M | 6.9 mo | No |
| Combined shock | No gift and government cut | ($0.5M) | Runs out | FY2027 |

**Recommendations:** slow cost growth to ~3% a year (the one lever management controls), grow
recurring unrestricted revenue, and adopt a 6-month reserve policy. Details in the
[memo](reports/CIS_Chicago_Memo.pdf).

## What's inside
| Path | Contents |
|---|---|
| `excel-model/CIS_Chicago_FPA_Model.xlsx` | 5-tab model with live formulas and a scenario dropdown |
| `reports/CIS_Chicago_Memo.pdf` | 1-page memo: findings and recommendations |
| `data/raw/990_extraction_template.csv` | Every Form 990 line used, FY2021–FY2025 |
| `data/raw/FILING_LINKS.md` | Links to each year's filing |
| `data/processed/cis_chicago_990_summary.csv` | Summary figures, FY2018–FY2025 |
| `data/SOURCES.md` | Sources, tie-out checks and known gaps |
| `images/dashboard.png` | Dashboard screenshot |

### The workbook
1. **Dashboard** — KPI tiles and five charts; forecast years follow the active scenario
2. **Inputs** — Form 990 data FY2021–FY2025 with automatic tie-out checks; base-case assumptions, each tagged *Filing* or *Assumption* with its rationale
3. **Historical** — growth, funding mix, spending ratios, runway (total vs. unrestricted), volatility
4. **Forecast** — FY2026–FY2028: recurring revenue, a major-gift switch, structural vs. reported surplus, unrestricted reserve roll-forward
5. **Scenarios** — dropdown (cell C5) plus all five scenarios calculated side by side, with break-even figures

**Colour key:** blue = number from a filing, yellow = key assumption you can change,
black = formula, green = link from another tab.

## Key assumptions (base case)
| Assumption | Value | Source | Why |
|---|---|---|---|
| Non-government recurring giving growth | 3% / year | Assumption | Roughly inflation |
| Government grants | Flat at $989k | Assumption | Grew from $43k in three years; public funding uncertain |
| School service contracts | Flat at $560k | Filing trend | $557k–$719k for five years, no trend |
| Expense growth | 6% / year | Assumption | About half the 11% historical pace |
| Major gift | $5M every 4 years, spread over 4 years | Filing evidence | FY2023 pledges receivable +$5.1M and restricted net assets +$5.3M; AbbVie's $6M in FY2019 |
| Reserve floor | 3 months of expenses | Sector guideline | Common range is 3–6 months |

## Data and checks
All figures come from CIS of Chicago's e-filed Form 990s (via ProPublica Nonprofit Explorer).
Each year passes tie-out checks: contributions lines sum to the total, revenue lines sum to
total revenue, functional expenses sum across columns, restricted + unrestricted = total net
assets, assets − liabilities = net assets, and each opening balance sheet matches the prior
year's close. Key lines were also verified by hand against the filings.

## Limitations
- Form 990s are published with a lag; FY2025 (year ended June 2025) is the latest available.
- Existing restricted net assets ($6.5M) are not released into the forecast because their timing
  isn't public, so the runway is conservative.
- Major-gift size and timing are estimated from balance-sheet changes, not reported directly.
- Expenses grow at a single rate; "students served" is defined differently across years, so no
  per-student cost is calculated.

## Why this project
I volunteer as a data science fellow at a grassroots Chicago education nonprofit, which got me
interested in how wraparound student-support organizations stay financially sustainable.
