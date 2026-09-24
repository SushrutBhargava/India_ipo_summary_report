# Peshwa Wheat IPO — DRHP / RHP cross-check (24 Sep 2026)

BSE SME, book built, fresh issue only. Bidding Sep 24 – Sep 28, 2026. All figures are copied exactly from the source named. ₹ lakh as reported in the RHP (100 lakh = 1 crore). "pdfp N" = PDF page number.

## Documents (all in this folder)

| File | Document | Source | SHA-256 (first 16) |
|---|---|---|---|
| peshwa-wheat-drhp.pdf | DRHP dated December 16, 2025, 370 pages | bsesme.com/download/381031/SME_IPO InPrinciple/DRHPPESHWA_20251216153357.pdf (chittorgarh DRHP link) | a5cbd8814fae83d0 |
| peshwa-wheat-rhp.pdf | RHP dated September 18, 2026, 380 pages | previous run (already in folder) | 40c8664e7fb9eafc |
| peshwa-wheat-gid.pdf | General Information Document, 47 pages | BSE zip `RHP&GID- Peshwa Wheat Limited_230920262248.zip` (chittorgarh RHP link) | d8896ad138b6e28f |

The BSE zip also contains an RHP (SHA-256 8890a475f1f9a149…) that is not byte-identical to the folder copy: it was re-exported 14 minutes later (CreationDate Sep 18, 2026 18:36 vs 18:22). pdftotext output differs only in whitespace/layout; the set of numbers in both texts is identical (checked with a multiset diff of every numeric token). The BSE duplicate was not kept.

The RHP's issue size (52,99,200 shares) matches chittorgarh. The DRHP (up to 55,00,000 shares, FY25 + 4M Jul 2025 financials) is stale and is used only for the change table.

Price band advertisement: not found. The RHP leaves price, P/E and market cap as `[●]`. Band ₹95–₹101 is from chittorgarh.

## DRHP to RHP changes

| Item | DRHP (Dec 16, 2025) | RHP (Sep 18, 2026) |
|---|---|---|
| Fresh issue | up to 55,00,000 shares | 52,99,200 shares |
| Market maker / net issue | [●] / [●] | 2,95,200 / 50,04,000 |
| Capex – plant & machinery | ₹ 1,000.11 lakh | ₹ 669.09 lakh |
| Capex – civil construction | ₹ 499.90 lakh | ₹ 501.20 lakh |
| Working capital | ₹ 2,950.00 lakh | ₹ 2,650.00 lakh |
| Latest period | FY25 + 4 months to Jul 31, 2025 (PAT 545.32, not annualised) | FY26 |
| Peer P/E: Baba Foods / Megastar Foods | 12.45 / 74.25 (avg 43.35; prices Dec 11, 2025) | 13.10 / 40.93 (avg 27.02; prices Jul 31, 2026) |

## Offer

- Price band ₹95 to ₹101 (chittorgarh). Lot 1,200 shares; individual minimum 2,400 shares (₹2,42,400).
- Shares: 1,37,28,996 pre-issue; 1,90,28,196 post-issue (pre + 52,99,200; matches chittorgarh).
- RHP "The Issue" (pdfp43): market maker 2,95,200; net issue 50,04,000; QIB 49,200 (anchor portion **Nil**); NII not less than 24,51,600 (8,17,200 + 16,34,400); individual investors not less than 25,03,200.
- Issue at cap: 52,99,200 × ₹101 = ₹53,52,19,200 (computed; chittorgarh body ₹53.52 crore).

### Valuation (computed — no price band ad found)

- FY26 EPS 11.51 (basic = diluted, RHP pdfp120). P/E 8.77x at ₹101 (8.7750), 8.25x at ₹95 (8.2537).
- Post-issue market cap: ₹1,92,18,47,796 at ₹101; ₹1,80,76,78,620 at ₹95.
- P/BV on FY26 NAV 31.37: 3.22x at ₹101 (3.2196).
- RHP weighted-average EPS 9.39; weighted-average RoNW 39.04%. Industry P/E: high 40.93, low 13.10, average 27.02.

## Financials (RHP, restated standalone, ₹ lakh)

The company was a partnership firm until Dec 25, 2023. "FY24" in the RHP P&L is the company's period Dec 26, 2023 – Mar 31, 2024 only; the partnership's period Apr 1 – Dec 25, 2023 is a separate column. MD&A (pdfp270) shows a combined FY24.

| | FY26 | FY25 | Period to Mar 31, 2024 | Period to Dec 25, 2023 | FY24 combined (MD&A) |
|---|---|---|---|---|---|
| Revenue from operations | 21,593.52 | 17,153.50 | 4,379.30 | 4,433.68 | 8,812.98 |
| Total income | 21,595.88 | 17,154.88 | 4,380.75 | 4,433.69 | 8,814.43 |
| Profit before exceptional items & tax | 2,124.34 | 1,604.21 | 668.55 | 104.13 | 772.68 |
| Exceptional / prior-period items | – | – | – | – | – |
| Profit after tax | 1,580.82 | 1,183.61 | 521.06 | 53.29 | 574.35 |
| EBITDA | 2,273.34 | 1,804.59 | 690.52 | 148.63 | — |
| Net worth | 4,306.44 | 2,725.62 | 1,542.01 | 728.57 | — |
| RoNW (PAT / closing NW) | 36.71% | 43.43% | 33.79% | 7.31% | 37.25% (Basis for Issue Price, "full FY") |
| RoE (avg equity) | 44.96% | 55.47% | 45.90% | 9.94% | — |
| Total borrowings (LT + ST) | 2,373.60 | 2,260.14 | 792.67 | 567.40 | — |
| Debt/equity | 0.55 | 0.83 | 0.51 | 0.78 | — |
| EPS (post-bonus) | 11.51 | 8.62 | 3.91 | 0.43 | 4.54 (Basis for Issue Price) |
| NAV per share (post-bonus) | 31.37 | 19.85 | 11.58 | 5.88 | 12.20 (Basis for Issue Price) |

Sources: P&L pdfp48, balance sheet pdfp46, other financial information pdfp261, KPIs pdfp123, capitalisation pdfp278 (FY26 total borrowings 2,373.60; D/E 0.55). FY25/FY24 borrowings = long-term + short-term from the balance sheet (46.97 + 2,213.17; 22.63 + 770.04; 3.63 + 563.77), computed.

Growth FY26 over FY25 (computed): total income +25.89%, PBT +32.42%, PAT +33.56%.

### Exceptional / one-time items

No exceptional items in any period ("Exceptional/Prior Period Items: –").

Tax-line item worth noting (not an exceptional item): FY26 tax includes an "Excess / (Short) Income tax Provision last year" credit of (838.64) and a deferred-tax charge of 840.20. The RHP (pdfp251) says the 838.64 "represents the tax effect of deductions allowed during the current year in respect of expenditure disallowed in earlier years under the Income-tax Act due to TDS-related provisions". FY25 had the mirror image: current tax 1,260.29 offset by a deferred-tax credit of (839.69). The two FY26 items net to +1.56 (computed), so FY26 PAT is not inflated by it. FY26 total tax 543.52 on PBT 2,124.34.

## Objects (RHP pdfp85, ₹ lakh)

| Object | Amount |
|---|---|
| Capex – purchase of plant & machinery | 669.09 |
| Capex – civil construction | 501.20 |
| Working capital | 2,650.00 |
| General corporate purposes | [●] (≤15% of gross proceeds or ₹1,000.00 lakh, whichever lower) |

## Chittorgarh vs RHP

| Field | Chittorgarh | RHP / computed | Verdict |
|---|---|---|---|
| Issue size | ₹53.52 Cr (body), ₹54 Cr (header) | 52,99,200 × ₹101 = ₹53,52,19,200 | Body matches. Header rounded. |
| Shares pre / post | 1,37,28,996 / 1,90,28,196 | same | Match |
| Market cap post | ₹192.18 Cr | ₹1,92,18,47,796 | Match |
| Market cap pre | ₹138.66 Cr | 1,37,28,996 × 101 = ₹1,38,66,28,596 | Match |
| FY26 / FY25 total income | 215.96 / 171.55 | 21,595.88 / 17,154.88 | Match |
| FY24 total income | 43.81 | 4,380.75 (Dec 26, 2023 – Mar 31, 2024 only) | STALE-basis: chittorgarh shows the 3-month company period, not the combined FY24 of 8,814.43. Its "revenue up 26%" is FY26 vs FY25 and is fine, but any FY24→FY25 growth read off its table is wrong |
| FY26 / FY25 / FY24 PAT | 15.81 / 11.84 / 5.21 | 1,580.82 / 1,183.61 / 521.06 | Match (FY24 same caveat; combined FY24 PAT 574.35) |
| FY26 EBITDA | 22.73 | 2,273.34 | Match |
| Net worth FY26 / FY25 / FY24 | 43.06 / 27.26 / 15.42 | 4,306.44 / 2,725.62 / 1,542.01 | Match |
| Total borrowing | 23.74 / 22.60 / 7.93 | 2,373.60 / 2,260.14 / 792.67 | Match |
| KPI ROE / ROCE / D/E / RoNW / PAT margin / EBITDA margin / NAV | 44.96% / 33.44% / 0.55 / 36.71% / 7.32% / 10.53% / 31.37 | same | Match |
| Price to book | 3.22 | 3.2196 at ₹101 | Match |
| Pre-IPO EPS / P/E | 11.51 / 8.77 | 11.51 / 8.7750 at cap | Match |
| Post-IPO EPS / P/E | 8.31 / 12.15 | not RHP figures (FY26 PAT / post-issue shares) | Chittorgarh's own calc |
| Promoter holding pre / post | 72.61% / 52.39% | 72.61% / 52.39% (99,68,000 shares, pdfp74) | Match |
| Objects | 6.69 / 5.01 / 26.50 / total 38.20 | 669.09 / 501.20 / 2,650.00 | Match (rounded) |

## Peer set (RHP pdfp122, "Comparison of Accounting Ratios with Industry Peers", verbatim)

| Name of Company | Current Market Price (₹) | Face Value | EPS Basic | EPS Diluted | PE | RoNW (%) | NAV per Equity Share (₹) | Total Income (₹ in Lakhs) |
|---|---|---|---|---|---|---|---|---|
| Peshwa Wheat Limited** | [●] | 10 | 11.51 | 11.51 | [●] | 36.71% | 31.37 | 21,593.52 |
| Baba Foods Processing India Limited | 24.75 | 10 | 1.89 | 1.89 | 13.10 | 4.63% | 40.64 | 20,504.12 |
| Megastar Foods Limited | 331.95 | 10 | 8.11 | 8.11 | 40.93 | 8.97% | 90.42 | 53,257.72 |

Peer data: audited results for year ended March 31, 2026; market prices dated July 31, 2026. (The RHP's own "Total Income" for Peshwa, 21,593.52, is actually its revenue from operations; total income is 21,595.88.)

## Not yet sourced

- Price band advertisement (official P/E, market cap). Tried: chittorgarh page (no ad link), BSE RHP+GID zip. Figures above are computed.
- Market maker name is from chittorgarh (Bhansali Value Creations); not re-verified in RHP.
- Post-issue promoter % beyond the RHP's own table (final Prospectus).
- Gross proceeds, issue expenses and GCP amount ([●] in RHP).
