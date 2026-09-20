# IPO Listing-Day Risk Desk
**Date:** 21 September 2026, 11:40 AM IST
**Status:** Advisory / report only — no orders placed, simulated, or drafted.

## Holdings Check (Fyers)
- Fyers holdings: **empty** — 0 positions. No holdings-aware flag applies to any tracked issue this run.
- Fyers auth working this run (prior runs had auth errors).

## Live Price Cross-Check (Fyers)
- No tracked issue has an assigned NSE/BSE trading symbol yet (all pre-listing) — Fyers quotes not applicable this run. Re-check from listing day morning (23 Sep for SS Retail/Jindal Supreme/Hero Motors, 24 Sep for NSE/Sonaselection, 29 Sep for Varmora, 30 Sep for Pooja Logistics).

## Risk Desk Cohort

| Issue | Status | GMP Rs. | GMP % | Sub (Overall) | Fyers Price | Holdings | Risk | Label | Rec |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| SS Retail | Closed — awaiting listing | Rs.147 | 34.67% | 107.41x | N/A (pre-listing) | No holdings | 72/100 | High — EXTREME | If allotted, consider selling within first 15 min — EXTREME: 107.41x sub > 75x threshold, plus 34.67% GMP = strong pop signal. |
| Jindal Supreme (India) | Closed — awaiting listing | Rs.29 | 31.18% | 177.03x | N/A (pre-listing) | No holdings | 72/100 | High — EXTREME | If allotted, consider selling within first 15 min — EXTREME: 177x sub > 75x threshold = high gap-up signal. |
| Hero Motors | Closed — awaiting listing | Rs.-2 | -2.38% | 7.01x | N/A (pre-listing) | No holdings | 55/100 | Medium | Hold — monitor. Negative GMP and weak 7x sub argue caution, not urgent exit. |
| NSE | Closed — awaiting listing | Rs.48 | 2.69% | 1.04x | N/A (pre-listing) | No holdings | 34/100 | Medium | Hold — monitor, no urgent exit signal. Quality business but muted demand and no anomaly. |
| Sonaselection India | Closed — awaiting listing | not yet active | 0.00% | 0.20x | N/A (pre-listing) | No holdings | 40/100 | Medium | Hold — monitor. Weak subscription despite decent fundamentals; no anomaly flag. |
| Varmora Granito | Upcoming (opens 22 Sep) | Rs.9 | 6.08% | pending | N/A (pre-listing) | No holdings | 52/100 | Medium | Hold — monitor. Book not yet open; GMP has softened ahead of opening. |
| Pooja Logistics | Upcoming (opens 23 Sep) | not yet active | 0.00% | pending | N/A (pre-listing) | No holdings | 35/100 | Low | Hold — monitor, no urgent exit signal. No market signal yet; fundamentals reasonable. |

## Gemini Cross-Check
- Jindal Supreme's EXTREME flag (177.03x subscription > 75x threshold) triggers a cross-check. Gemini script not run this session (out of scope for this environment's available tools this run) — primary source (chittorgarh.com, confirmed 177.03x at book close 18 Sep 16:05) accepted as authoritative; no internal inconsistency found in the figure across chittorgarh, NSE-derived combined data, or investorgain.com's subscription column.
- No other issue triggered the cross-check condition (no internally inconsistent or stale-looking GMP/subscription figures found).

## Anomaly Flags
- Jindal Supreme (India): subscription 177.03x > 75x threshold → **EXTREME**.
- SS Retail: subscription 107.41x > 75x threshold → **EXTREME** as well (corrects the 20 Sep run, which had flagged this issue as High only — subscription clears the same 75x bar as Jindal Supreme).
- Hero Motors: negative GMP + weak 7x sub — caution flag but not EXTREME (below thresholds).
- NSE, Sonaselection, Varmora, Pooja Logistics: no anomaly triggers (subscription and GMP below thresholds or pending).

## Anchor Lock-In / Unlock Ratio
- SS Retail, Jindal Supreme, Hero Motors: anchor allocation ~27-30% of QIB portion across the three closed issues (per chittorgarh anchor disclosure carried from RHP). 30-day unlock ~21 Oct 2026, 90-day unlock ~20 Dec 2026. Anchor Unlock Ratio (anchor shares unlocking ÷ total free float) remains in the 12-16% range for each — **Low** qualitative flag, consistent with the 20 Sep run.
- NSE: anchor participation not separately disclosed as OFS-only mega-issue; treating as **Low** unlock risk given the extremely broad 19-lead-manager distribution base.
- Sonaselection, Varmora, Pooja Logistics: anchor books not yet finalized/disclosed at this stage (Varmora books open 22 Sep, Pooja 23 Sep) — marked **pending**.

## Bottom Line
Three listings 23 Sep: Jindal Supreme (177x sub, 31% GMP, EXTREME) and SS Retail (107x sub — also crosses the 75x EXTREME threshold, 35% GMP) both point to strong listing-day pops but are priced for it (53x and 14x P/E respectively — Jindal Supreme's cheap P/E offsets some downside risk on a flat open, SS Retail's rich 53x P/E does not). Hero Motors — negative GMP, weak 7x sub, steep 92x P/E — no urgent exit signal since it never had a pop to sell into; hold and monitor only. NSE and Sonaselection closed 21 Sep at modest (1.04x) and weak (0.20x) subscription respectively — no anomaly, no urgent action, monitor for listing-day open. Varmora Granito and Pooja Logistics remain pre-open; re-assess once bidding begins.

---
*Advisory only. Not investment advice. No orders placed or simulated. No brokerage API order-placement endpoints were called at any point in producing this report.*
