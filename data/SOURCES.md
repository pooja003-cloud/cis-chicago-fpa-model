# Data Sources

All data is public. Figures are tagged in the workbook as **Filing** (taken directly
from a Form 990) or **Assumption** (my estimate, with the reason stated).

## Primary source
- **Communities In Schools of Chicago (EIN 36-3591326), Form 990 filings, FY2021–FY2025**
  (fiscal years end June 30)
  - ProPublica Nonprofit Explorer: https://projects.propublica.org/nonprofits/organizations/363591326

| Form 990 section | What it gives the model |
|---|---|
| Part VIII – Statement of Revenue | Revenue by source (contributions, government grants line 1e, program service revenue, investment income) |
| Part IX – Statement of Functional Expenses | Expenses by type and by function (program / management & general / fundraising) |
| Part X – Balance Sheet | Cash, investments, pledges receivable, net assets without / with donor restrictions (lines 27–28) |
| Part III – Program Service Accomplishments | Program descriptions, schools / students served (if reported) |
| Schedule B (public version) | Size of large contributions (donor names are redacted) |

## Context sources
- The 74, "Three Chicago nonprofits get $55 million…" (Nov 2018) — AbbVie's $6M gift to CIS Chicago:
  https://www.the74million.org/article/three-chicago-nonprofits-get-55-million-to-help-low-income-students-graduate-largest-gift-ever-communities-in-schools/

## Known gaps
- FY2025 has no PDF on ProPublica yet; use the web version of the e-filed return.
- ProPublica's summary does not show government grants (Part VIII line 1e) or restricted vs.
  unrestricted net assets (Part X lines 27-28); these must be read from the filings.
- Schedule B details are often not included in the public copy.
- Line items were extracted from ProPublica's web render of each e-filed return and passed
  all tie-out checks (1a-1f = 1h; revenue lines = line 12; Part IX B+C+D = A; Part X 27+28 = 32;
  assets - liabilities = net assets; opening balance sheet = prior year's closing).
- FY2024 reports staff wages on Part IX line 6 instead of line 7; personnel cost uses lines 5-10 combined.
- Part III "students served" changes definition (500 -> 1,300 -> 80,000+), so it is not comparable across years.
- FY2021 government grants ($1.63M) are far above other years; the reason is not stated on the face of the return.
- FY2018-FY2020 are kept for context (the FY2019 AbbVie gift); the model uses FY2021-FY2025.
