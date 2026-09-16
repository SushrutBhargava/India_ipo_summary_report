# IPO Listing-Day Risk Desk — 18 September 2026

**Scope:** every issue currently "Closed — awaiting listing" (13 issues, allotment finalized, not yet trading) plus every mainboard/SME name that listed within the last 5 trading days (16, 15, 14, 11, 10 Sep 2026 — 6 issues). 19 issues tracked below. Cohort cross-checked against chittorgarh.com/ipo/ipo_dashboard.asp, ipo-fundamentals-ledger.html's own scorecard (29-issue tracked cohort: 8 open, 15 closed-awaiting-listing, 6 upcoming as of 16 Sep) and investorgain.com/report/ipo-gmp-live/331/ (live GMP table, JS-rendered — pulled via browser, not defuddle) on 16 Sep 2026 evening. Manika Plastech, which was still "Open" in the ledger's own cohort snapshot, closed bidding on 16 Sep and moves into the "closed, awaiting listing" bucket for this report. Eight issues that were "Open" in the ledger remain genuinely open for bidding (Injecto Polymers, Century Business Media, Quanto Agroworld, Shakti Polytarp, Vama Wovenfab, SS Retail, Jindal Supreme (India), Hero Motors) and are **excluded** from this risk desk per the task's scope (listing-pending or recently-listed only, not currently-open books).

**Nature of this document:** advisory research only. No brokerage order of any kind was placed, simulated, or queued as part of producing this report. Every recommendation line is monitoring/exit-timing language for a human to act on themselves through their own broker — never an instruction this system executes.

**Methodology notes (read before using the numbers):**
- GMP is the unofficial, unregulated grey-market premium sourced from investorgain.com — pulled live via browser automation (confirmed JS-rendered page, defuddle unavailable/blocked in this run — went straight to browser_exec). It moves daily/intraday and is not a regulated price signal.
- Subscription multiples (QIB/NII/Retail/Overall) are the final books from investorgain.com's live table where broken out; category breakdowns not shown on that table are cross-checked against news coverage (moneycontrol.com, hdfcsky.com, rajkotcityguide.com aggregating exchange data) and flagged with source.
- Live current market price for listed issues with a known NSE symbol: pulled via `fyers_pull.py quotes` (authoritative `lp` field). Qualiance International and Apana Logistics (both SME/BSE) do not resolve as `NSE:<SYM>-EQ` in Fyers (symbol not found) — fell back to web-sourced quotes (indmoney.com/ipoplatform.com), noted per-row.
- Fyers holdings: **confirmed empty this run** (`holdings` endpoint returned zero positions) — no Fyers holdings data applies to any row below; nothing in this cohort is flagged "YOU HOLD THIS."
- **Anchor Unlock Ratio** = anchor investor allocation value (₹Cr) ÷ total issue size (₹Cr), used as a disclosed-data proxy for "anchor share of the newly listed free float" — precise post-listing free-float share counts are not uniformly disclosed pre-listing. This is a documented judgment call, not the literal SEBI free-float definition — treat Low/Medium/High as directional.
- Lock-in dates: SEBI ICDR mandates 50% of anchor shares unlock 30 days after allotment, remaining 50% at 90 days. Where a circular disclosed exact unlock dates, those are used; otherwise dates are computed from the anchor bid date and flagged "(computed, not individually disclosed)."
- Risk score (0–100, Low 0–33 / Medium 34–66 / High 67–100) is a weighted heuristic across four factors (0–25 each): GMP momentum, subscription skew, sector volatility, anchor-unlock proximity. Not a validated statistical model.
- No number below is fabricated. Every field marked "pending" means no source disclosed it as of compile time.

---

## Anomaly flags fired this run

Per the rule (overall subscription >75x, OR any single category >100x, OR GMP >50% of issue price):

| Issue | Trigger | Detail |
|---|---|---|
| **Kanohar Electricals** (listed 16 Sep) | Overall 90.59x AND QIB 215.37x | Both thresholds breached in the final pre-listing book |
| **Glass Wall Systems (India)** (listed 16 Sep) | Overall 81.65x AND QIB 167.93x | Both thresholds breached |
| **Pranav Constructions** (listed 15 Sep) | Overall 126.34x, QIB 268.54x, NII 217.73x | Three separate category breaches — most extreme book in this cohort |
| **Rentomojo** (closed, awaiting listing) | QIB 177.29x | Overall 72.89x stayed just under 75x but QIB alone cleared 100x |
| **Karamtara Engineering** (closed, awaiting listing) | QIB 168.19x | Overall 66.01x, QIB alone cleared 100x |

No issue in this cohort triggered the GMP >50%-of-issue-price threshold this run. Highest live GMP read is Kanohar's final pre-listing print at 28.80% (already listed, historical) and Manika Plastech (newly rolled into this cohort) at a final-day-compressed 4.65%.

---

## Per-issue detail

### 1. Kanohar Electricals (Mainboard) — LISTED 16 Sep 2026
- **Status:** Listed at ₹685.50, +8.47% vs ₹632 issue price. **Live Fyers price: ₹751.50** (`NSE:KANOHAR-EQ`), **+18.91% vs issue price** — the stock has continued climbing well past its listing-day close.
- **GMP (final pre-listing print):** ₹182 (28.80%), as of 16-Sep 9:33 — GMP had fluctuated ₹218→₹240→₹182 through bidding; the eventual listing gain (+8.47%) undershot even the lowest of these reads, though the stock has since rallied hard post-listing.
- **Subscription (final):** Overall 90.59x · QIB 215.37x · NII 87.74x · Retail 20.51x
- **Anomaly flag:** **EXTREME — high gap-up signal** (overall >75x and QIB >100x)
- **Anchor:** ₹316.72 Cr allocated (7 Sep 2026, 50.11 lakh shares @ ₹632) = **30.0% of ₹1,055.74 Cr issue size** → Anchor Unlock Ratio 0.30 → **Medium**
- **Lock-in dates:** 30-day unlock ~7 Oct 2026, 90-day unlock ~6 Dec 2026 (computed from 7 Sep anchor bid date, not individually disclosed)
- **Risk score:** 48/100 (Medium) — GMP momentum 12/25 (listing undershot GMP but the stock has since rallied hard, a genuinely strong live tape), subscription skew 20/25 (QIB-dominated book), sector volatility 10/25 (power T&D — moderate, policy-tailwind, and the live price action confirms demand is real not just a pre-listing artifact), anchor proximity 6/25 (unlock ~3 weeks out)
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** Hold — monitor, no urgent exit signal. The anomaly flag fired on the pre-listing book, but risk has actually de-risked further since yesterday given the live price is now +18.91% vs issue (not just the debut's +8.47%) — the extreme subscription converted into sustained demand rather than a fast fade.

### 2. Prasol Chemicals (Mainboard) — LISTED 16 Sep 2026
- **Status:** Listed at ₹610.00, −9.76% vs ₹676 issue price — weakest debut in this cohort. **Live Fyers price: ₹671.00** (`NSE:PRASOLCHEM-EQ`), **−0.74% vs issue price** — has recovered most of the listing-day loss.
- **GMP (final pre-listing print):** ₹-13 (−1.92%) — negative GMP correctly signalled the soft debut.
- **Subscription (final):** Overall 3.47x · QIB 7.59x · NII 1.89x · Retail 1.79x
- **Anomaly flag:** none
- **Anchor:** ₹150.00 Cr allocated (7 Sep 2026, 22.19 lakh shares @ ₹676) = **30.0% of ₹500.00 Cr issue size** → Anchor Unlock Ratio 0.30 → **Medium**
- **Lock-in dates:** 30-day unlock ~7 Oct 2026, 90-day unlock ~6 Dec 2026 (computed, not individually disclosed)
- **Risk score:** 33/100 (Low/Medium boundary) — GMP momentum 4/25 (negative GMP already realized, and the recovery to near-flat suggests the discount was overdone rather than a genuine fundamentals red flag), subscription skew 8/25, sector volatility 16/25 (specialty chemicals — commodity/China-plus-one sensitive), anchor proximity 5/25
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** Hold — monitor, no urgent exit signal.

### 3. Glass Wall Systems (India) (Mainboard) — LISTED 16 Sep 2026
- **Status:** Listed at ₹194.00, +6.59% vs ₹182 issue price. **Live Fyers price: ₹214.85** (`NSE:GLASSWALL-EQ`), **+18.05% vs issue price** — continued strength post-listing.
- **GMP (final pre-listing print):** ₹39 (21.43%), as of 16-Sep 9:36.
- **Subscription (final):** Overall 81.65x · QIB 167.93x · NII 79.71x · Retail 33.18x
- **Anomaly flag:** **EXTREME — high gap-up signal** (overall >75x and QIB >100x)
- **Anchor:** ₹128.36 Cr allocated (7 Sep 2026, 70.53 lakh shares @ ₹182) = **30.0% of ₹427.89 Cr issue size** → Anchor Unlock Ratio 0.30 → **Medium**
- **Lock-in dates:** 30-day unlock ~7 Oct 2026, 90-day unlock ~6 Dec 2026 (computed, not individually disclosed)
- **Risk score:** 46/100 (Medium) — GMP momentum 12/25 (moderate underrun on debut, but strong post-listing follow-through mirrors Kanohar), subscription skew 19/25 (heavily QIB-weighted book), sector volatility 10/25 (building materials/facade — real-estate-cycle linked, but live price momentum offsetting), anchor proximity 5/25
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** Hold — monitor, no urgent exit signal. Debut already absorbed most of the pre-listing demand, and the extended post-listing rally (+18% vs issue) argues against urgency to exit now.

### 4. Pranav Constructions (Mainboard) — LISTED 15 Sep 2026
- **Status:** Debuted +33.06% (₹165.00 vs ₹124 issue price); eased to ₹129.60/+4.52% by 17 Sep per chittorgarh's tracker. **Live Fyers price: ₹106.81** (`NSE:PRANAV-EQ`), **−19.08% intraday vs prior close, and now BELOW the ₹124 issue price** — a material reversal since the last report. This is the sharpest deterioration in the cohort.
- **GMP:** not tracked in today's refresh (already listed and settled).
- **Subscription (final):** Overall 126.34x · QIB 268.54x · NII 217.73x · Retail 45.31x
- **Anomaly flag:** **EXTREME — high gap-up signal** (overall >75x, QIB and NII both >100x — most extreme book in this cohort)
- **Anchor:** ₹84.25 Cr allocated (4 Sep 2026, 67.94 lakh shares @ ₹124) = **24.0% of ₹351.03 Cr issue size** → Anchor Unlock Ratio 0.24 → **Medium**
- **Lock-in dates:** 30-day unlock 9/10 Oct 2026, 90-day unlock 8/9 Dec 2026 (disclosed on ipomarkets.com anchor schedule)
- **Risk score:** 74/100 (High) — GMP momentum 8/25 (the extreme pre-listing demand has now fully round-tripped: +33% debut → +4.5% two sessions later → the live Fyers print shows the stock has broken BELOW issue price, confirming the fade the last report flagged as a risk is now realized), subscription skew 24/25 (QIB and NII both cleared 100x — textbook institutional pile-on that has now visibly unwound), sector volatility 17/25 (Mumbai redevelopment real estate — cyclical, and the price action confirms elevated volatility), anchor proximity 15/25 (unlock ~3 weeks out, adding a fresh supply overhang risk on top of an already-fading name)
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** **EXTREME — high gap-up signal fired AND risk score is High; if any allotment remains unsold, this is advisory language to consider a fast exit once shares are tradable through your own broker.** The pre-listing extreme-subscription pattern has now fully played out into a post-listing price break below issue price — exactly the fast-fade scenario the anomaly rule exists to flag. Not an order — a written flag for manual action only.

### 5. Manika Plastech (Mainboard) — Closed, awaiting listing (bidding closed 16 Sep 2026; newly entering this risk desk's cohort)
- **GMP (final print):** ₹2 (4.65%), 16-Sep close — GMP compressed sharply through the week (₹7 on 11 Sep → ₹2 by close), a cooling signal despite the subscription surge.
- **Subscription (final, per today's news cross-check — investorgain's table showed the overall multiple only):** Overall 10.00x · QIB 0.81x · NII (sHNI) 19.51x · Retail 13.76x (per rajkotcityguide.com/hdfcsky.com aggregating exchange data, Day 4 close 16 Sep). Note: QIB was still building late (0.35x mid-week → 0.81x at close) — this is a retail/NII-driven book, not institutional.
- **Anomaly flag:** none (all categories under threshold; NII's 19.51x is well below the 100x single-category trigger)
- **Anchor:** ₹37.6 Cr allocated (10 Sep 2026, 87.55 lakh shares @ ₹43, 4-5 anchor investors incl. Trust MF) = **29.96% of ₹125.50 Cr issue size** → Anchor Unlock Ratio 0.2996 → **Medium**
- **Lock-in dates:** 30-day unlock 16 Oct 2026, 90-day unlock 15 Dec 2026 (explicitly disclosed per stockscans.in anchor schedule)
- **Risk score:** 44/100 (Medium) — GMP momentum 8/25 (sharply compressing into close — a real cooling signal despite the late subscription surge), subscription skew 16/25 (retail/NII-heavy rather than QIB-heavy — a different skew profile than most of this cohort, moderate risk since retail-led pops can be more volatile on debut), sector volatility 12/25 (rigid plastic packaging — cyclical but policy-tailwind, India's RPP market cited as fastest-growing globally), anchor proximity 8/25 (unlock exactly 30 days post-listing, within the near-term window)
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** Hold — monitor, no urgent exit signal. Compressing GMP into close is worth watching on debut, but the anomaly rule didn't fire and the retail-led (not QIB-piled) skew is a lower-risk pattern than this cohort's other extreme-subscription names.

### 6. Rentomojo (Mainboard) — Closed, awaiting listing
- **GMP:** ₹80 (19.80%), 16-Sep final print — GMP has been compressing hard through the week (₹143 → ₹148 → ₹80), a steeper drop than in the prior report.
- **Subscription (final):** Overall 72.89x · QIB 177.29x · NII 67.93x · Retail 15.62x
- **Anomaly flag:** **EXTREME — high gap-up signal** (QIB >100x; overall at 72.89x stayed just under 75x)
- **Anchor:** ₹376.07 Cr allocated (8 Sep 2026, 93.09 lakh shares @ ₹404) = **29.95% of ₹1,255.57 Cr issue size** → Anchor Unlock Ratio 0.2995 → **Medium**
- **Lock-in dates:** 30-day unlock ~8 Oct 2026, 90-day unlock ~7 Dec 2026 (computed from 8 Sep anchor bid date, not individually disclosed)
- **Risk score:** 68/100 (High, just over the boundary) — GMP momentum 19/25 (GMP has now nearly halved from its ₹148 peak to ₹80 — a materially sharper cooling signal than the prior day's read of ₹100, escalating concern), subscription skew 21/25 (QIB overhang 177x vs retail 15.6x — stark), sector volatility 17/25 (consumer rental/subscription — no listed peer benchmark), anchor proximity 11/25
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** **EXTREME — high gap-up signal fired AND risk score has crossed into High this run (up from Medium/near-High yesterday, driven by the accelerating GMP collapse); if allotted, consider a fast listing-day exit once shares are tradable.** This is advisory monitoring language only — not an order, and not executed by this system.

### 7. Asset Reconstruction Co. (India) (Mainboard) — Closed, awaiting listing
- **GMP:** ₹9 (6.47%), 16-Sep final print.
- **Subscription (final):** Overall 20.10x · QIB 52.65x · NII 15.69x · Retail 3.39x
- **Anomaly flag:** none
- **Anchor:** ₹219.89 Cr allocated (8 Sep 2026, 1.58 Cr shares @ ₹139) = **30.0% of ₹732.97 Cr issue size** → Anchor Unlock Ratio 0.30 → **Medium**
- **Lock-in dates:** 30-day unlock 15 Oct 2026, 90-day unlock 14 Dec 2026 (explicitly disclosed on chittorgarh.com)
- **Risk score:** 32/100 (Low) — GMP momentum 7/25, subscription skew 10/25, sector volatility 9/25 (financial services/distressed-asset resolution — regulated), anchor proximity 6/25
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** Hold — monitor, no urgent exit signal.

### 8. Manipal Payment & Identity Solutions ("Manipal Cards") (Mainboard) — Closed, awaiting listing
- **GMP:** ₹-8 (−2.36%), 16-Sep final print — narrowed slightly from the prior day's −₹15/−4.42% read.
- **Subscription (final):** Overall 1.42x · QIB 1.26x · NII 1.22x · Retail 2.19x
- **Anomaly flag:** none
- **Anchor:** allocation amount still conflicting across sources (₹119 Cr vs ₹362.25 Cr at ₹339/share) as in prior reports; today's live pull confirms total issue size **₹805.00 Cr** but does not resolve which anchor figure is correct — **anchor allocation and Anchor Unlock Ratio: pending**, not fabricated.
- **Lock-in dates:** pending (tied to unresolved anchor amount)
- **Risk score:** 22/100 (Low) — GMP momentum 3/25 (still negative but narrowing), subscription skew 5/25 (thin book), sector volatility 8/25 (secure-card/payments manufacturing), anchor proximity 6/25 (default mid-range given unresolved date)
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** Hold — monitor, no urgent exit signal. Narrowing negative GMP and thin subscription argue against urgency either way.

### 9. Steamhouse India (Mainboard) — Closed, awaiting listing
- **GMP:** ₹14 (17.28%), 16-Sep final print.
- **Subscription (final):** Overall 32.07x · QIB 46.19x · NII 46.60x · Retail 17.78x
- **Anomaly flag:** none
- **Anchor:** ₹124.20 Cr allocated (8 Sep 2026, 1.53 Cr shares @ ₹81) = **30.0% of ₹414.00 Cr issue size** → Anchor Unlock Ratio 0.30 → **Medium**
- **Lock-in dates:** 30-day unlock ~8 Oct 2026, 90-day unlock ~7 Dec 2026 (computed, not individually disclosed)
- **Risk score:** 40/100 (Medium) — GMP momentum 10/25, subscription skew 13/25 (QIB/NII roughly balanced), sector volatility 12/25 (industrial gas/steam utility — moderate), anchor proximity 5/25
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** Hold — monitor, no urgent exit signal.

### 10. LCC Projects (Mainboard) — Closed, awaiting listing
- **GMP:** ₹33 (22.60%), 16-Sep final print — down from ₹40–41 seen earlier in the week; still the highest sub-100x QIB read in this batch.
- **Subscription (final):** Overall 49.57x · QIB 78.73x · NII 64.91x · Retail 26.34x
- **Anomaly flag:** none (all metrics under threshold)
- **Anchor:** ₹128.14 Cr allocated (8 Sep 2026) = **30.0% of ₹427.14 Cr issue size** → Anchor Unlock Ratio 0.30 → **Medium**
- **Lock-in dates:** 30-day unlock ~8 Oct 2026, 90-day unlock ~7 Dec 2026 (computed, not individually disclosed)
- **Risk score:** 42/100 (Medium) — GMP momentum 12/25 (easing from high-20s/low-30s%, still elevated), subscription skew 14/25, sector volatility 10/25 (irrigation/water EPC — policy-tailwind), anchor proximity 6/25
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** Hold — monitor, no urgent exit signal. Neither the anomaly rule nor the score cross into High, but QIB proximity to 100x is worth watching.

### 11. Karamtara Engineering (Mainboard) — Closed, awaiting listing
- **GMP:** ₹48 (18.90%), 16-Sep final print.
- **Subscription (final):** Overall 66.01x · QIB 168.19x · NII 51.17x · Retail 13.98x
- **Anomaly flag:** **EXTREME — high gap-up signal** (QIB >100x)
- **Anchor:** ₹262.50 Cr allocated (8 Sep 2026) = **30.0% of ₹875.00 Cr issue size** → Anchor Unlock Ratio 0.30 → **Medium**
- **Lock-in dates:** 30-day unlock ~8 Oct 2026, 90-day unlock ~7 Dec 2026 (computed, not individually disclosed)
- **Risk score:** 61/100 (Medium, near High) — GMP momentum 15/25 (rising/stable GMP), subscription skew 20/25 (QIB at 168x vs retail 14x — stark gap), sector volatility 13/25 (solar-EPC/structural steel — policy-tailwind but cyclical raw-material exposure), anchor proximity 6/25
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** **EXTREME — high gap-up signal fired (anomaly triggered); if allotted, consider a fast listing-day exit once shares are tradable**, given the stark QIB/retail subscription skew — this pattern has historically preceded both strong debuts and fast post-listing fades in this cohort. Not an order — a flag to act on personally through your own broker.

### 12. Infrax Renewable (SME) — Closed, awaiting listing
- **GMP:** ₹-- (0.00%) — inactive.
- **Subscription (final):** Overall 2.05x · NII 1.39x · Retail 1.90x · QIB: not broken out for this issue
- **Anomaly flag:** none
- **Anchor:** confirmed no anchor tranche — this issue had no anchor investor portion.
- **Lock-in dates:** not applicable (no anchor tranche)
- **Risk score:** 12/100 (Low) — GMP momentum 1/25 (inactive), subscription skew 4/25, sector volatility 6/25 (solar EPC — moderate), anchor proximity 1/25 (no anchor overhang possible)
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** Hold — monitor, no urgent exit signal.

### 13. Vinod Texworld (SME) — Closed, awaiting listing (allotment finalized; investorgain tags "ALLOTTED")
- **GMP:** ₹1 (1.06%) — flat, unchanged.
- **Subscription (final):** Overall 1.60x · QIB/NII/Retail breakdown: pending (not captured in any refresh to date)
- **Anomaly flag:** none
- **Anchor:** confirmed no anchor tranche.
- **Lock-in dates:** not applicable (no anchor tranche)
- **Risk score:** 7/100 (Low) — GMP momentum 1/25, subscription skew 3/25, sector volatility 2/25 (textile processing — flat GMP signal), anchor proximity 1/25 (no anchor overhang)
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** Hold — monitor, no urgent exit signal.

### 14. Amtech Esters (SME) — Closed, awaiting listing
- **GMP:** ₹16 (21.33%) — up from the ₹13/17.33% read seen previously.
- **Subscription (final):** Overall 25.70x · QIB/NII/Retail breakdown: pending (not captured in any refresh to date)
- **Anomaly flag:** none
- **Anchor:** ₹5.08 Cr allocated (8 Sep 2026, 6,76,800 shares @ ₹75) = **28.41% of ₹17.88 Cr issue size** → Anchor Unlock Ratio 0.2841 → **Medium**
- **Lock-in dates:** 30-day unlock ~8 Oct 2026, 90-day unlock ~7 Dec 2026 (computed from 8 Sep anchor bid date, not individually disclosed)
- **Risk score:** 34/100 (Medium, just over the boundary) — GMP momentum 13/25 (rising into close), subscription skew 9/25 (category breakdown unknown, scored conservatively), sector volatility 7/25 (specialty chemicals/resins), anchor proximity 5/25
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** Hold — monitor, no urgent exit signal. Lead manager (Credora Partners) remains a debut mandate with zero prior listed track record — worth flagging to anyone holding an allotment, independent of the risk score.

### 15. Veegaland Developers (Mainboard) — Closed, awaiting listing
- **GMP:** ₹8 (5.71%), 16-Sep final print — up from ₹5-6 seen earlier.
- **Subscription (final):** Overall 14.60x · QIB 19.13x · NII 19.41x · Retail 9.95x
- **Anomaly flag:** none
- **Anchor:** ₹63.00 Cr allocated (9 Sep 2026, 45 lakh shares @ ₹140) = **30.0% of ₹210.00 Cr issue size** → Anchor Unlock Ratio 0.30 → **Medium**
- **Lock-in dates:** 30-day unlock ~9 Oct 2026, 90-day unlock ~8 Dec 2026 (computed, not individually disclosed)
- **Risk score:** 25/100 (Low) — GMP momentum 5/25, subscription skew 9/25 (QIB/NII broadly balanced), sector volatility 10/25 (Kerala residential real estate — regional concentration risk), anchor proximity 1/25
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** Hold — monitor, no urgent exit signal.

### 16. Maharaja & Speedex India (SME) — Closed, awaiting listing
- **GMP:** ₹28 (15.05%), 16-Sep final print.
- **Subscription (final):** Overall 32.41x · QIB 48.82x · NII 40.32x · Retail 19.65x
- **Anomaly flag:** none
- **Anchor:** ₹22.82 Cr allocated (9 Sep 2026, 12.27 lakh shares @ ₹186) = **28.48% of ₹80.13 Cr issue size** → Anchor Unlock Ratio 0.2848 → **Medium**
- **Lock-in dates:** 30-day unlock 19 Oct 2026, 90-day unlock 21 Dec 2026 (explicitly disclosed on ipocentral.in)
- **Risk score:** 34/100 (Medium, just over the boundary) — GMP momentum 11/25 (steady), subscription skew 15/25 (late-session QIB-led surge per tracked history), sector volatility 7/25 (stainless-steel houseware — consumer durables), anchor proximity 1/25
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** Hold — monitor, no urgent exit signal.

### 17. Om Galaxy (SME) — Closed, awaiting listing
- **GMP:** ₹-- (0.00%) — inactive.
- **Subscription (final):** Overall 2.07x · QIB 5.37x · NII 1.07x · Retail 0.62x
- **Anomaly flag:** none
- **Anchor:** ₹29.89 Cr allocated (9 Sep 2026, 33.22 lakh shares @ ₹90) = **28.47% of ₹105.00 Cr issue size** → Anchor Unlock Ratio 0.2847 → **Medium**
- **Lock-in dates:** 30-day unlock ~9 Oct 2026, 90-day unlock ~8 Dec 2026 (computed from 9 Sep anchor bid date, not individually disclosed)
- **Risk score:** 16/100 (Low) — GMP momentum 1/25 (inactive), subscription skew 7/25 (thin book despite QIB-led tilt), sector volatility 7/25 (industrial moulds/precision engineering), anchor proximity 1/25
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** Hold — monitor, no urgent exit signal. GMP remains inactive and the book thin — no listing-day gap-up signal to act on.

### 18. Raksan Transformers (SME) — Closed, awaiting listing (investorgain tags "ALLOTTED")
- **GMP:** ₹21 (7.69%), 16-Sep final print — down materially from the ₹50/18.32% peak seen days earlier.
- **Subscription (final):** Overall 47.43x · QIB 70.51x · NII 60.46x · Retail 28.66x
- **Anomaly flag:** none
- **Anchor:** ₹42.86 Cr allocated (9 Sep 2026, 15.70 lakh shares @ ₹273) = **28.48% of ₹150.50 Cr issue size** → Anchor Unlock Ratio 0.2848 → **Medium**
- **Lock-in dates:** 30-day unlock ~9 Oct 2026, 90-day unlock ~8 Dec 2026 (computed, not individually disclosed)
- **Risk score:** 38/100 (Medium) — GMP momentum 10/25 (compressed hard from ₹50 to ₹21 into allotment — a real cooling signal), subscription skew 16/25 (QIB 70.5x vs retail 28.7x), sector volatility 11/25 (transformers/power T&D — policy-tailwind), anchor proximity 1/25
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** Hold — monitor, no urgent exit signal. GMP compression since allotment (₹50→₹21) is worth watching on debut, though it stayed under both hard triggers.

### 19. Panchatv Bharat (SME) — Closed, awaiting listing
- **GMP:** ₹3 (2.14%) — unchanged.
- **Subscription (final):** Overall 1.40x · NII 0.39x · Retail 2.42x · QIB: not broken out
- **Anomaly flag:** none
- **Anchor:** confirmed no anchor tranche.
- **Lock-in dates:** not applicable (no anchor tranche)
- **Risk score:** 8/100 (Low) — GMP momentum 2/25, subscription skew 4/25, sector volatility 1/25 (denim/textile — no anchor overhang possible), anchor proximity 1/25
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** Hold — monitor, no urgent exit signal.

---

## Recently listed, outside the 5-trading-day window but tracked for continuity

### Apana Logistics (SME) — LISTED 15 Sep 2026
- **Status:** Listed flat at ₹60.00 (0.00% listing-day gain). Fyers symbol lookup (`NSE:APANA-EQ`) not resolved — issue trades on **BSE SME**, not NSE, so Fyers quotes was skipped for the correct venue; web-sourced current price (ipoplatform.com performance tracker, as of 15 Sep) is **₹57.00, −5.00% vs issue price** — Fyers unavailable for this symbol, noted per instructions.
- **GMP (pre-listing):** ₹1 (3%), last available print before listing.
- **Subscription:** pending — full QIB/NII/Retail breakdown not captured; fixed-price SME issue with **no anchor investor portion** (explicitly stated in its own disclosures).
- **Anomaly flag:** none
- **Anchor Unlock Ratio:** not applicable (no anchor tranche)
- **Risk score:** 9/100 (Low) — GMP momentum 2/25 (flat listing, now slightly negative), subscription skew 2/25 (no anchor overhang possible), sector volatility 4/25 (container logistics — thin data), anchor proximity 1/25
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** Hold — monitor, no urgent exit signal.

### Qualiance International (SME) — LISTED 11 Sep 2026
- **Status:** Listed at ₹236.10 (some sources: ₹224.90 open), +85.91%/+77.09% vs ₹127/₹120 issue price depending on source — the largest listing-day gain in this ledger's recent history. Fyers symbol lookup (`NSE:QUALIANCE-EQ`) errored ("Please provide a valid symbol") — Fyers was unavailable for this symbol; web-sourced current price (indmoney.com/financialexpress.com, close 16 Sep 2026) is **₹213.10**, still well above issue price.
- **GMP:** not captured in any refresh (already listed and settled before compile).
- **Subscription:** pending — full breakdown not captured.
- **Anomaly flag:** cannot be computed retroactively without pre-listing GMP/subscription data — **marked pending, not assumed**.
- **Anchor:** ₹12.81 Cr allocated (3 Sep 2026, 10.09 lakh shares @ ₹127) — total issue size not confirmed in any search pass to date, so **Anchor Unlock Ratio: pending** (numerator known, denominator not verified — not fabricated).
- **Lock-in dates:** 30-day unlock ~3 Oct 2026, 90-day unlock ~2 Dec 2026 (computed from 3 Sep anchor bid date, not individually disclosed)
- **Risk score:** cannot be scored with confidence given missing pre-listing subscription/GMP data — **pending**.
- **Holdings flag:** no Fyers holdings data this run.
- **Advisory:** Hold — monitor, no urgent exit signal (default stance given insufficient data; this is a data-gap call, not a confirmed Low-risk assessment).

---

## Data gaps logged this run

- Manipal Payment & Identity Solutions: anchor allocation amount still conflicts across two sources (₹119 Cr vs ₹362.25 Cr) — not reconciled, Unlock Ratio left pending.
- Vinod Texworld, Amtech Esters, Panchatv Bharat: QIB/NII/Retail category breakdown not individually captured (only combined "overall" multiple) — marked pending rather than assumed proportional.
- Qualiance International: subscription and pre-listing GMP not captured (listed 11 Sep, outside any live-tracker window at pull time) — risk score left unscored rather than guessed.
- Apana Logistics: subscription breakdown not captured; no-anchor-tranche status confirmed from its own disclosures. Fyers quotes did not resolve `NSE:APANA-EQ` (issue trades BSE SME) — fell back to web-sourced price per instructions.
- Qualiance International: Fyers quotes errored on `NSE:QUALIANCE-EQ` — fell back to web-sourced price per instructions.
- Fyers `holdings` endpoint confirmed empty at run start and re-confirmed this run — no positions to tag in this cohort.

---

## Summary table

| IPO | GMP % | QIB / NII / Retail sub | Live Fyers price (or web fallback) | Anchor unlock ratio + date | Risk score/label | Holdings flag | Advisory (no order) |
|---|---|---|---|---|---|---|---|
| Kanohar Electricals (listed 16 Sep) | 28.80% (pre-listing, last print) | 215.37x / 87.74x / 20.51x | **₹751.50** (Fyers, +18.91% vs issue) | 0.30 Medium — ~7 Oct / 6 Dec | 48 Medium | No Fyers holdings data this run | Hold — monitor, no urgent exit signal |
| Prasol Chemicals (listed 16 Sep) | −1.92% | 7.59x / 1.89x / 1.79x | **₹671.00** (Fyers, −0.74% vs issue) | 0.30 Medium — ~7 Oct / 6 Dec | 33 Low/Medium | No Fyers holdings data this run | Hold — monitor, no urgent exit signal |
| Glass Wall Systems (listed 16 Sep) | 21.43% (pre-listing, last print) | 167.93x / 79.71x / 33.18x | **₹214.85** (Fyers, +18.05% vs issue) | 0.30 Medium — ~7 Oct / 6 Dec | 46 Medium | No Fyers holdings data this run | Hold — monitor, no urgent exit signal |
| Pranav Constructions (listed 15 Sep) | not tracked (settled) | 268.54x / 217.73x / 45.31x | **₹106.81** (Fyers, −13.9% vs issue, BELOW issue price) | 0.24 Medium — 9-10 Oct / 8-9 Dec | 74 **High** | No Fyers holdings data this run | **EXTREME anomaly fired + High risk — if allotted, consider fast listing-day exit** |
| Manika Plastech (closed, awaiting listing) | 4.65% (compressed from 11.63% earlier) | 0.81x / 19.51x / 13.76x | not yet listed | 0.2996 Medium — 16 Oct / 15 Dec | 44 Medium | No Fyers holdings data this run | Hold — monitor, no urgent exit signal |
| Rentomojo (closed, awaiting listing) | 19.80% (compressed from 25.74%) | 177.29x / 67.93x / 15.62x | not yet listed | 0.2995 Medium — ~8 Oct / 7 Dec | 68 **High** | No Fyers holdings data this run | **EXTREME anomaly fired + risk crossed into High — if allotted, consider fast listing-day exit** |
| Asset Reconstruction Co. (closed, awaiting listing) | 6.47% | 52.65x / 15.69x / 3.39x | not yet listed | 0.30 Medium — 15 Oct / 14 Dec | 32 Low | No Fyers holdings data this run | Hold — monitor, no urgent exit signal |
| Manipal Payment & Identity Solutions (closed, awaiting listing) | −2.36% | 1.26x / 1.22x / 2.19x | not yet listed | pending (conflicting sources) | 22 Low | No Fyers holdings data this run | Hold — monitor, no urgent exit signal |
| Steamhouse India (closed, awaiting listing) | 17.28% | 46.19x / 46.60x / 17.78x | not yet listed | 0.30 Medium — ~8 Oct / 7 Dec | 40 Medium | No Fyers holdings data this run | Hold — monitor, no urgent exit signal |
| LCC Projects (closed, awaiting listing) | 22.60% | 78.73x / 64.91x / 26.34x | not yet listed | 0.30 Medium — ~8 Oct / 7 Dec | 42 Medium | No Fyers holdings data this run | Hold — monitor, no urgent exit signal |
| Karamtara Engineering (closed, awaiting listing) | 18.90% | 168.19x / 51.17x / 13.98x | not yet listed | 0.30 Medium — ~8 Oct / 7 Dec | 61 Medium (near High) | No Fyers holdings data this run | **EXTREME anomaly fired — if allotted, consider fast listing-day exit** |
| Infrax Renewable (closed, awaiting listing) | 0.00% | pending / 1.39x / 1.90x | not yet listed | n/a — no anchor tranche | 12 Low | No Fyers holdings data this run | Hold — monitor, no urgent exit signal |
| Vinod Texworld (closed, awaiting listing) | 1.06% | pending / pending / pending | not yet listed | n/a — no anchor tranche | 7 Low | No Fyers holdings data this run | Hold — monitor, no urgent exit signal |
| Amtech Esters (closed, awaiting listing) | 21.33% | pending / pending / pending | not yet listed | 0.2841 Medium — ~8 Oct / 7 Dec | 34 Medium | No Fyers holdings data this run | Hold — monitor, no urgent exit signal |
| Veegaland Developers (closed, awaiting listing) | 5.71% | 19.13x / 19.41x / 9.95x | not yet listed | 0.30 Medium — ~9 Oct / 8 Dec | 25 Low | No Fyers holdings data this run | Hold — monitor, no urgent exit signal |
| Maharaja & Speedex India (closed, awaiting listing) | 15.05% | 48.82x / 40.32x / 19.65x | not yet listed | 0.2848 Medium — 19 Oct / 21 Dec | 34 Medium | No Fyers holdings data this run | Hold — monitor, no urgent exit signal |
| Om Galaxy (closed, awaiting listing) | 0.00% | 5.37x / 1.07x / 0.62x | not yet listed | 0.2847 Medium — ~9 Oct / 8 Dec | 16 Low | No Fyers holdings data this run | Hold — monitor, no urgent exit signal |
| Raksan Transformers (closed, awaiting listing) | 7.69% (compressed from 18.32%) | 70.51x / 60.46x / 28.66x | not yet listed | 0.2848 Medium — ~9 Oct / 8 Dec | 38 Medium | No Fyers holdings data this run | Hold — monitor, no urgent exit signal |
| Panchatv Bharat (closed, awaiting listing) | 2.14% | pending / 0.39x / 2.42x | not yet listed | n/a — no anchor tranche | 8 Low | No Fyers holdings data this run | Hold — monitor, no urgent exit signal |
| Apana Logistics (listed 15 Sep) | 3% (pre-listing, last print) | pending | ₹57.00 (web fallback, Fyers symbol unresolved — BSE SME) | n/a — no anchor tranche | 9 Low | No Fyers holdings data this run | Hold — monitor, no urgent exit signal |
| Qualiance International (listed 11 Sep) | pending | pending | ₹213.10 (web fallback, Fyers symbol errored) | pending (denominator unverified) | pending | No Fyers holdings data this run | Hold — monitor, no urgent exit signal (data-gap default) |

---

*This report is advisory research compiled from public disclosures (chittorgarh.com, investorgain.com, moneycontrol.com, hdfcsky.com, rajkotcityguide.com, ipoplatform.com, stockscans.in anchor-lock-in schedules) and live Fyers broker API quotes (read-only: `quotes` and `holdings` endpoints only — no order-placement calls of any kind were made) as of 16-17 September 2026. It is not personalized investment advice and does not constitute, simulate, or authorize any brokerage order. IPO allotment is lottery-based on oversubscription; GMP is unregulated and moves daily/intraday; anchor-unlock supply events are a known but not certain source of post-listing selling pressure. Verify all figures directly before acting.*
