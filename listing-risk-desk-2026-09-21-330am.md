# IPO Listing-Day Risk Desk — 21 September 2026 (3:30 AM IST run)

**Advisory only — analysis of public data, not personalized investment advice. Never an executed or simulated order.**

Cohort: 7 tracked issues (5 closed-awaiting-listing, 2 upcoming). No Fyers pre-listing symbols exist yet — none of the 7 have listed (confirmed via `fyers_pull.py quotes NSE:NSE-EQ` / `NSE:SONA-EQ` / `NSE:VARMORA-EQ`, all returned "Please provide a valid symbol" — expected pre-listing). Fyers `holdings` call succeeded: `count_total: 0`, empty list. No positions to flag.

Figures below are unchanged from the 5:20 AM run — investorgain.com's live GMP/subscription table has not refreshed since its 18 Sep timestamp (book-closing day for all 5 closed issues); no fresher print available.

## 1. SS Retail — Mainboard
- GMP: ₹147 (34.67% over ₹424 issue price)
- Subscription: 107.41x overall (QIB 246.90x)
- Anomaly flag: **EXTREME** (overall subscription far exceeds 75x threshold)
- Anchor unlock: not disclosed in DRHP extract to date — **pending**
- Risk score: 78/100 — **High**
- Recommendation: If allotted, consider selling within first 15 min of listing. Advisory only, not an order.
- Holdings flag: not held.

## 2. Jindal Supreme (India) — Mainboard
- GMP: ₹29 (31.18% over ₹93)
- Subscription: 177.03x overall
- Anomaly flag: **EXTREME**
- Anchor unlock: pending — not disclosed
- Risk score: 80/100 — **High**
- Recommendation: If allotted, consider selling within first 15 min of listing. Advisory only.
- Holdings flag: not held.

## 3. Hero Motors — Mainboard
- GMP: -₹2 (-2.38% over ₹84) — negative
- Subscription: 7.01x overall
- Anomaly flag: none
- Anchor unlock: pending
- Risk score: 42/100 — **Medium**
- Recommendation: Hold — monitor, no urgent exit signal.
- Holdings flag: not held.

## 4. NSE — Mainboard
- GMP: ₹48 (2.69% over ₹1,785)
- Subscription: 1.04x overall
- Anomaly flag: none
- Anchor unlock: pending
- Risk score: 25/100 — **Low**
- Recommendation: Hold — monitor, no urgent exit signal.
- Holdings flag: not held.

## 5. Sonaselection India — Mainboard
- GMP: not yet active
- Subscription: 0.20x overall — undersubscribed
- Anomaly flag: none (undersubscription is a negative demand signal, not an anomaly per the >75x/GMP>50% definitions)
- Anchor unlock: pending
- Risk score: 55/100 — **Medium**
- Recommendation: Hold — monitor, no urgent exit signal (score below High threshold). Caution: soft subscription is itself a red flag for allotted investors regardless of score band.
- Holdings flag: not held.

## 6. Varmora Granito — Mainboard (Upcoming, opens 22 Sep)
- GMP: ₹9 (6.08% over ₹148)
- Subscription: pending (book not yet open)
- Anomaly flag: none
- Anchor unlock: pending
- Risk score: not yet computable — book not open. Preliminary read: Low-Medium on modest GMP.
- Recommendation: Monitor at book open.
- Holdings flag: not held.

## 7. Pooja Logistics — SME (Upcoming, opens 23 Sep)
- GMP: not yet active
- Subscription: pending (book not yet open)
- Anomaly flag: none
- Anchor unlock: pending
- Risk score: not yet computable.
- Recommendation: Monitor at book open.
- Holdings flag: not held.

## Fyers status this run
- `quotes`: called for NSE, SONA, VARMORA symbols — all returned "invalid symbol" (expected, none listed yet).
- `holdings`: called successfully — `count_total: 0`, empty holdings list. No personal exposure to flag.

## Gemini ground-check
Not invoked this run — no EXTREME-flag issue had an internally inconsistent primary-source figure this run; SS Retail and Jindal Supreme's subscription/GMP data matches the previously-verified 5:20 AM run values exactly.

## Bottom line
SS Retail and Jindal Supreme remain the two EXTREME-flagged names (High risk, fast-exit-on-allotment advisory). Hero Motors, NSE, and Sonaselection sit at Medium/Low with a hold-and-monitor stance. Varmora Granito and Pooja Logistics have not opened books yet — nothing to score. All figures unchanged from the 5:20 AM run (investorgain data still shows the 18 Sep close timestamp, no fresher print). This is analysis of public data only, not personalized investment advice, and no order of any kind was placed or simulated.
