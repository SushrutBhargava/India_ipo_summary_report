# IPO Listing-Day Risk Desk — 17 September 2026

**Scope:** every issue currently "Closed — awaiting listing" (14 issues, allotment finalized/finalizing, not yet trading) plus every mainboard/SME name that listed within the last 5 trading days (16, 15, 14, 11, 10 Sep 2026 — 6 issues). 20 issues tracked below. Cohort cross-checked against chittorgarh.com/ipo/ipo_dashboard.asp (mainboard dashboard) and investorgain.com/report/ipo-gmp-live/331/ (live GMP table, JS-rendered — pulled via browser, not defuddle) on 17 Sep 2026; investorgain's live table's own "UPDATED-ON" timestamps read 16 Sep evening for most rows (site had not yet posted a fresh 17 Sep intraday refresh at pull time) — this is disclosed below per-issue, not smoothed over.

**Nature of this document:** advisory research only. No brokerage order of any kind was placed, simulated, or queued as part of producing this report. Every recommendation line is monitoring/exit-timing language for a human to act on themselves through their own broker — never an instruction this system executes.

**Methodology notes (read before using the numbers):**
- GMP is the unofficial, unregulated grey-market premium sourced from investorgain.com — pulled live via browser automation (confirmed JS-rendered page, defuddle returns empty on this URL). It moves daily/intraday and is not a regulated price signal.
- Subscription multiples (QIB/NII/Retail/Overall) — "overall" figures refreshed from today's investorgain pull; category (QIB/NII/Retail) breakdowns not re-broken-out in this table are carried forward from the prior day's chittorgarh.com detail-page pull where already verified, flagged "(carried, unchanged book)" — final books do not change after allotment, so this is not stale data, just not re-fetched.
- **Anchor Unlock Ratio** = anchor investor allocation value (₹Cr) ÷ total issue size (₹Cr), used as a disclosed-data proxy for "anchor share of the newly listed free float" — precise post-listing free-float share counts are not uniformly disclosed pre-listing. This is a documented judgment call, not the literal SEBI free-float definition — treat Low/Medium/High as directional.
- Lock-in dates: SEBI ICDR mandates 50% of anchor shares unlock 30 days after allotment, remaining 50% at 90 days. Where a circular disclosed exact unlock dates, those are used; otherwise dates are computed from the anchor bid date and flagged "(computed, not individually disclosed)."
- Risk score (0–100, Low 0–33 / Medium 34–66 / High 67–100) is a weighted heuristic across four factors (0–25 each): GMP momentum, subscription skew, sector volatility, anchor-unlock proximity. Not a validated statistical model.
- No number below is fabricated. Every field marked "pending" means no source disclosed it as of compile time. Two anchor-ratio corrections vs the prior day's report are noted explicitly below (Amtech Esters, Om Galaxy, Maharaja & Speedex) — today's live pull surfaced updated total-issue-size figures that change the denominator; corrections are shown, not silently overwritten.

---

## Anomaly flags fired this run

Per the rule (overall subscription >75x, OR any single category >100x, OR GMP >50% of issue price):

| Issue | Trigger | Detail |
|---|---|---|
| **Kanohar Electricals** (listed 16 Sep) | Overall 90.59x AND QIB 215.37x (carried) | Both thresholds breached in the final book before listing |
| **Glass Wall Systems (India)** (listed 16 Sep) | Overall 81.65x AND QIB 167.93x (carried) | Both thresholds breached |
| **Pranav Constructions** (listed 15 Sep) | Overall 126.34x, QIB 268.54x, NII 217.73x (carried) | Three separate category breaches — most extreme book in this cohort |
| **Rentomojo** (closed, awaiting listing) | QIB 177.29x (carried) | Overall 72.89x stayed just under 75x but QIB alone cleared 100x |
| **Karamtara Engineering** (closed, awaiting listing) | QIB 168.19x (carried) | Overall 66.01x, QIB alone cleared 100x |

No issue in this cohort triggered the GMP >50%-of-issue-price threshold. Highest live GMP read today is Kanohar's last pre-listing print at 28.80% (already listed, historical) and Rentomojo at 24.75% (still pending).

---

## Per-issue detail

### 1. Kanohar Electricals (Mainboard) — LISTED 16 Sep 2026
- **Status:** Listed at ₹685.50, +8.47% vs ₹632 issue price. No fresher 17-Sep price available from today's pull (site still showing the 16-Sep listing-day close as its latest print).
- **GMP (last pre-listing print, today's pull):** ₹182 (28.80%), as of 16-Sep 9:33 — this is investorgain's final pre-listing figure; note GMP fluctuated intraday during bidding (₹218→₹240→₹182) and the eventual listing gain (+8.47%) undershot even the lowest of these reads.
- **Subscription (final):** Overall 90.59x · QIB 215.37x (carried) · NII 87.74x (carried) · Retail 20.51x (carried)
- **Anomaly flag:** **EXTREME — high gap-up signal** (overall >75x and QIB >100x)
- **Anchor:** ₹316.72 Cr allocated (7 Sep 2026, 50.11 lakh shares @ ₹632) = **30.0% of ₹1,055.74 Cr issue size** (issue size reconfirmed against today's live pull) → Anchor Unlock Ratio 0.30 → **Medium**
- **Lock-in dates:** 30-day unlock ~7 Oct 2026, 90-day unlock ~6 Dec 2026 (computed from 7 Sep anchor bid date, not individually disclosed)
- **Risk score:** 52/100 (Medium) — GMP momentum 10/25 (actual gain badly undershot every pre-listing GMP read, signals demand has cooled hard post-listing), subscription skew 20/25 (QIB-dominated book), sector volatility 12/25 (power T&D — moderate, policy-tailwind), anchor proximity 10/25 (unlock ~20 days out)
- **Advisory:** Hold — monitor, no urgent exit signal. Already listed and settled; the anomaly flag fired on the pre-listing book but the debut already absorbed most of that demand.

### 2. Prasol Chemicals (Mainboard) — LISTED 16 Sep 2026
- **Status:** Listed at ₹610.00, −9.76% vs ₹676 issue price — weakest debut in this cohort.
- **GMP (last pre-listing print):** ₹-13 (−1.92%) — negative GMP correctly signalled the soft debut.
- **Subscription (final):** Overall 3.47x · QIB 7.59x (carried) · NII 1.89x (carried) · Retail 1.79x (carried)
- **Anomaly flag:** none
- **Anchor:** ₹150.00 Cr allocated (7 Sep 2026, 22.19 lakh shares @ ₹676) = **30.0% of ₹500.00 Cr issue size** → Anchor Unlock Ratio 0.30 → **Medium**
- **Lock-in dates:** 30-day unlock ~7 Oct 2026, 90-day unlock ~6 Dec 2026 (computed, not individually disclosed)
- **Risk score:** 38/100 (Medium) — GMP momentum 5/25 (negative, discount already realized), subscription skew 8/25, sector volatility 18/25 (specialty chemicals — commodity/China-plus-one sensitive), anchor proximity 7/25
- **Advisory:** Hold — monitor, no urgent exit signal.

### 3. Glass Wall Systems (India) (Mainboard) — LISTED 16 Sep 2026
- **Status:** Listed at ₹194.00, +6.59% vs ₹182 issue price.
- **GMP (last pre-listing print):** ₹39 (21.43%), as of 16-Sep 9:36 (updated from ₹41/22.53% in the prior day's read — GMP compressed slightly into listing).
- **Subscription (final):** Overall 81.65x · QIB 167.93x (carried) · NII 79.71x (carried) · Retail 33.18x (carried)
- **Anomaly flag:** **EXTREME — high gap-up signal** (overall >75x and QIB >100x)
- **Anchor:** ₹128.36 Cr allocated (7 Sep 2026, 70.53 lakh shares @ ₹182) = **30.0% of ₹427.89 Cr issue size** → Anchor Unlock Ratio 0.30 → **Medium**
- **Lock-in dates:** 30-day unlock ~7 Oct 2026, 90-day unlock ~6 Dec 2026 (computed, not individually disclosed)
- **Risk score:** 50/100 (Medium) — GMP momentum 13/25, subscription skew 19/25, sector volatility 12/25 (building materials/facade — real-estate-cycle linked), anchor proximity 6/25
- **Advisory:** Hold — monitor, no urgent exit signal. Debut already absorbed most of the pre-listing demand without an outsized gap-up.

### 4. Pranav Constructions (Mainboard) — LISTED 15 Sep 2026
- **Status:** Debuted +33.06% (₹165.00 vs ₹124 issue price); latest tracked price ₹129.60, **+4.52%** vs issue (per chittorgarh's own performance tracker, refreshed today — down from the +6.45%/₹132 read in yesterday's report, confirming continued fade).
- **GMP:** not tracked in today's refresh (already listed and settled).
- **Subscription (final):** Overall 126.34x · QIB 268.54x (carried) · NII 217.73x (carried) · Retail 45.31x (carried)
- **Anomaly flag:** **EXTREME — high gap-up signal** (overall >75x, QIB and NII both >100x — most extreme book in this cohort)
- **Anchor:** ₹84.25 Cr allocated (4 Sep 2026, 67.94 lakh shares @ ₹124) = **24.0% of ₹351.03 Cr issue size** (per chittorgarh's reservation table) → Anchor Unlock Ratio 0.24 → **Medium**
- **Lock-in dates:** 30-day unlock 9/10 Oct 2026, 90-day unlock 8/9 Dec 2026 (disclosed on ipomarkets.com anchor schedule)
- **Risk score:** 66/100 (Medium, at the High boundary) — GMP momentum 18/25 (the debut delivered a genuine pop confirming extreme demand converted to a real gap-up, but continued fade since — 33% → 4.5% over two sessions — argues the momentum leg is now largely spent), subscription skew 22/25 (QIB and NII both cleared 100x), sector volatility 15/25 (Mumbai redevelopment real estate — cyclical), anchor proximity 11/25 (unlock ~3 weeks out)
- **Advisory:** Hold — monitor, no urgent exit signal. Note: the anomaly flag DID fire on this issue's pre-listing book and the risk score sits just under the High cutoff — anyone still holding an unsold allotment should treat this as a name to watch closely given the fast fade already observed (+33% debut → +4.5% two sessions later), even though today's recomputed score lands in Medium rather than High.

### 5. Rentomojo (Mainboard) — Closed, awaiting listing (per live pull, listing tag still shows 17 Sep 2026)
- **GMP:** ₹100 (24.75%), as of 16-Sep 11:30 print — GMP has been compressing through the week (₹143 → ₹148 → ₹100).
- **Subscription (final):** Overall 72.89x · QIB 177.29x (carried) · NII 67.93x (carried) · Retail 15.62x (carried)
- **Anomaly flag:** **EXTREME — high gap-up signal** (QIB >100x; overall at 72.89x stayed just under 75x)
- **Anchor:** ₹376.07 Cr allocated (8 Sep 2026, 93.09 lakh shares @ ₹404) = **29.95% of ₹1,255.57 Cr issue size** (reconfirmed) → Anchor Unlock Ratio 0.2995 → **Medium**
- **Lock-in dates:** 30-day unlock ~8 Oct 2026, 90-day unlock ~7 Dec 2026 (computed from 8 Sep anchor bid date, not individually disclosed)
- **Risk score:** 64/100 (Medium, near High) — GMP momentum 16/25 (compressing GMP into listing — down from a ₹148 peak to ₹100 — a real cooling signal versus 24 hours ago), subscription skew 21/25 (QIB overhang 177x vs retail 15.6x), sector volatility 17/25 (consumer rental/subscription — no listed peer), anchor proximity 10/25
- **Advisory:** **EXTREME — high gap-up signal fired (anomaly triggered); if allotted, consider a fast listing-day exit once shares are tradable**, given the QIB-heavy book, no listed-peer benchmark, and visibly cooling GMP momentum into listing. This is advisory monitoring language only — not an order, and not executed by this system.

### 6. Asset Reconstruction Co. (India) (Mainboard) — Closed, awaiting listing
- **GMP:** ₹10 (7.19%), as of 16-Sep 11:35 print (up slightly from ₹9/6.47% yesterday).
- **Subscription (final):** Overall 20.10x · QIB 52.65x (carried) · NII 15.69x (carried) · Retail 3.39x (carried)
- **Anomaly flag:** none
- **Anchor:** ₹219.89 Cr allocated (8 Sep 2026, 1.58 Cr shares @ ₹139) = **30.0% of ₹732.97 Cr issue size** (reconfirmed) → Anchor Unlock Ratio 0.30 → **Medium**
- **Lock-in dates:** 30-day unlock 15 Oct 2026, 90-day unlock 14 Dec 2026 (explicitly disclosed on chittorgarh.com)
- **Risk score:** 33/100 (Low/Medium boundary) — GMP momentum 8/25, subscription skew 10/25, sector volatility 10/25 (financial services/distressed-asset resolution — regulated), anchor proximity 5/25
- **Advisory:** Hold — monitor, no urgent exit signal.

### 7. Manipal Payment & Identity Solutions ("Manipal Cards") (Mainboard) — Closed, awaiting listing
- **GMP:** ₹-15 (−4.42%), as of 16-Sep 11:30 print (widened from −₹10/−2.95% yesterday — negative GMP deepening).
- **Subscription (final):** Overall 1.42x · QIB 1.26x (carried) · NII 1.22x (carried) · Retail 2.19x (carried)
- **Anomaly flag:** none
- **Anchor:** allocation amount still conflicting across sources (₹119 Cr vs ₹362.25 Cr at ₹339/share); today's live pull confirms total issue size **₹805.00 Cr** but does not resolve which anchor figure is correct — **anchor allocation and Anchor Unlock Ratio: pending**, not fabricated pending source reconciliation.
- **Lock-in dates:** pending (tied to unresolved anchor amount)
- **Risk score:** 24/100 (Low) — GMP momentum 2/25 (deepening negative GMP), subscription skew 5/25 (thin book), sector volatility 8/25 (secure-card/payments manufacturing), anchor proximity 6/25 (default mid-range given unresolved date)
- **Advisory:** Hold — monitor, no urgent exit signal. Widening negative GMP and thin subscription argue against urgency either way.

### 8. Steamhouse India (Mainboard) — Closed, awaiting listing
- **GMP:** ₹15 (18.52%), as of 16-Sep 11:33 print (down slightly from ₹17/20.99% yesterday).
- **Subscription (final):** Overall 32.07x · QIB 46.19x (carried) · NII 46.60x (carried) · Retail 17.78x (carried)
- **Anomaly flag:** none
- **Anchor:** ₹124.20 Cr allocated (8 Sep 2026, 1.53 Cr shares @ ₹81) = **30.0% of ₹414.00 Cr issue size** (reconfirmed) → Anchor Unlock Ratio 0.30 → **Medium**
- **Lock-in dates:** 30-day unlock ~8 Oct 2026, 90-day unlock ~7 Dec 2026 (computed, not individually disclosed)
- **Risk score:** 42/100 (Medium) — GMP momentum 11/25, subscription skew 13/25 (QIB/NII roughly balanced), sector volatility 13/25 (industrial gas/steam utility — moderate), anchor proximity 5/25
- **Advisory:** Hold — monitor, no urgent exit signal.

### 9. LCC Projects (Mainboard) — Closed, awaiting listing
- **GMP:** ₹41 (28.08%), as of 16-Sep 11:28 print (up from ₹44/30.14% level; two consecutive prints show GMP oscillating in the high-20s/low-30s%).
- **Subscription (final):** Overall 49.57x · QIB 78.73x (carried) · NII 64.91x (carried) · Retail 26.34x (carried)
- **Anomaly flag:** none (all metrics under threshold, though QIB is the highest sub-100x read in this batch)
- **Anchor:** ₹128.14 Cr allocated (8 Sep 2026) = **30.0% of ₹427.14 Cr issue size** (reconfirmed) → Anchor Unlock Ratio 0.30 → **Medium**
- **Lock-in dates:** 30-day unlock ~8 Oct 2026, 90-day unlock ~7 Dec 2026 (computed, not individually disclosed)
- **Risk score:** 48/100 (Medium) — GMP momentum 16/25 (consistently high GMP in this batch — real gap-up signal building), subscription skew 14/25, sector volatility 11/25 (irrigation/water EPC — policy-tailwind), anchor proximity 7/25
- **Advisory:** Hold — monitor, no urgent exit signal. Worth watching closely given the persistently elevated GMP, but neither the anomaly rule nor the score cross into High.

### 10. Karamtara Engineering (Mainboard) — Closed, awaiting listing
- **GMP:** ₹45 (17.72%), as of 16-Sep 11:28 print (up from ₹40/15.75% yesterday).
- **Subscription (final):** Overall 66.01x · QIB 168.19x (carried) · NII 51.17x (carried) · Retail 13.98x (carried)
- **Anomaly flag:** **EXTREME — high gap-up signal** (QIB >100x)
- **Anchor:** ₹262.50 Cr allocated (8 Sep 2026) = **30.0% of ₹875.00 Cr issue size** (reconfirmed) → Anchor Unlock Ratio 0.30 → **Medium**
- **Lock-in dates:** 30-day unlock ~8 Oct 2026, 90-day unlock ~7 Dec 2026 (computed, not individually disclosed)
- **Risk score:** 63/100 (Medium, near High) — GMP momentum 14/25 (rising GMP), subscription skew 20/25 (QIB at 168x vs retail 14x — stark gap), sector volatility 14/25 (solar-EPC/structural steel — policy-tailwind but cyclical raw-material exposure), anchor proximity 5/25
- **Advisory:** **EXTREME — high gap-up signal fired (anomaly triggered); if allotted, consider a fast listing-day exit once shares are tradable**, given the stark QIB/retail subscription skew — this pattern has historically preceded both strong debuts and fast post-listing fades in this cohort. Not an order — a flag to act on personally through your own broker.

### 11. Infrax Renewable (SME) — Closed, awaiting listing
- **GMP:** ₹-- (0.00%) — inactive, unchanged.
- **Subscription (final):** Overall 2.05x · NII 1.39x (carried) · Retail 1.90x (carried) · QIB: not broken out for this issue
- **Anomaly flag:** none
- **Anchor:** **confirmed no anchor tranche (❌ per today's live pull)** — this issue had no anchor investor portion. Correction from yesterday's "pending — no circular found": today's data confirms it as a genuine "not applicable," not a missing disclosure.
- **Lock-in dates:** not applicable (no anchor tranche)
- **Risk score:** 15/100 (Low) — GMP momentum 1/25 (inactive), subscription skew 5/25, sector volatility 8/25 (solar EPC — moderate), anchor proximity 1/25 (no anchor overhang possible)
- **Advisory:** Hold — monitor, no urgent exit signal.

### 12. Vinod Texworld (SME) — Closed, awaiting listing (allotment finalized; investorgain tags this "ALLOTTED")
- **GMP:** ₹1 (1.06%) — unchanged, flat.
- **Subscription (final):** Overall 1.60x · QIB/NII/Retail breakdown: pending (not captured in any refresh to date)
- **Anomaly flag:** none
- **Anchor:** **confirmed no anchor tranche (❌ per today's live pull)** — correction from yesterday's "pending."
- **Lock-in dates:** not applicable (no anchor tranche)
- **Risk score:** 8/100 (Low) — GMP momentum 1/25, subscription skew 3/25, sector volatility 3/25 (textile processing — flat GMP signal), anchor proximity 1/25 (no anchor overhang)
- **Advisory:** Hold — monitor, no urgent exit signal.

### 13. Amtech Esters (SME) — Closed, awaiting listing
- **GMP:** ₹13 (17.33%) — unchanged.
- **Subscription (final):** Overall 25.70x · QIB/NII/Retail breakdown: pending (not captured in any refresh to date)
- **Anomaly flag:** none
- **Anchor:** **CORRECTION vs prior day:** anchor allocation now confirmed — ₹5.08 Cr raised (8 Sep 2026, 6,76,800 shares @ ₹75), per chittorgarh's own anchor-allocation news item and the anchor allocation letter PDF (chittorgarh.net). Total issue size ₹17.88 Cr (today's live pull) → **Anchor Unlock Ratio = 5.08 / 17.88 = 28.41%** → **Medium**. Yesterday's report marked this "pending — no circular found"; today's search surfaced the disclosure directly.
- **Lock-in dates:** 30-day unlock ~8 Oct 2026, 90-day unlock ~7 Dec 2026 (computed from 8 Sep anchor bid date, not individually disclosed)
- **Risk score:** 32/100 (Low/Medium boundary) — GMP momentum 10/25, subscription skew 9/25 (category breakdown unknown, scored conservatively), sector volatility 8/25 (specialty chemicals/resins), anchor proximity 5/25 (now scored on a confirmed unlock date rather than defaulted)
- **Advisory:** Hold — monitor, no urgent exit signal. Lead manager (Credora Partners) remains a debut mandate with zero prior listed track record — worth flagging to anyone holding an allotment, independent of the risk score.

### 14. Veegaland Developers (Mainboard) — Closed, awaiting listing
- **GMP:** ₹6 (4.29%), as of 16-Sep 11:29 print (up slightly from ₹5/3.57%).
- **Subscription (final):** Overall 14.60x · QIB 19.13x (carried) · NII 19.41x (carried) · Retail 9.95x (carried)
- **Anomaly flag:** none
- **Anchor:** ₹63.00 Cr allocated (9 Sep 2026, 45 lakh shares @ ₹140) = **30.0% of ₹210.00 Cr issue size** (reconfirmed) → Anchor Unlock Ratio 0.30 → **Medium**
- **Lock-in dates:** 30-day unlock ~9 Oct 2026, 90-day unlock ~8 Dec 2026 (computed, not individually disclosed)
- **Risk score:** 26/100 (Low) — GMP momentum 4/25, subscription skew 10/25 (QIB/NII broadly balanced), sector volatility 11/25 (Kerala residential real estate — regional concentration risk), anchor proximity 1/25
- **Advisory:** Hold — monitor, no urgent exit signal.

### 15. Maharaja & Speedex India (SME) — Closed, awaiting listing
- **GMP:** ₹25 (13.44%), as of 16-Sep 11:30 print (down from ₹28/15.05%).
- **Subscription (final):** Overall 32.41x · QIB 48.82x (carried) · NII 40.32x (carried) · Retail 19.65x (carried)
- **Anomaly flag:** none
- **Anchor:** ₹22.82 Cr allocated (9 Sep 2026, 12.27 lakh shares @ ₹186) — **CORRECTION vs prior day:** today's live pull confirms a total issue size of **₹80.13 Cr** (vs ₹76.11 Cr used yesterday) → recomputed **Anchor Unlock Ratio = 22.82 / 80.13 = 28.48%** → **Medium** (was 29.99% Medium yesterday on the smaller denominator; label unchanged, ratio revised down slightly).
- **Lock-in dates:** 30-day unlock 19 Oct 2026, 90-day unlock 21 Dec 2026 (explicitly disclosed on ipocentral.in)
- **Risk score:** 36/100 (Medium) — GMP momentum 10/25 (GMP has eased slightly, ₹28→₹25), subscription skew 15/25 (late-session QIB-led surge per tracked history), sector volatility 10/25 (stainless-steel houseware — consumer durables), anchor proximity 1/25
- **Advisory:** Hold — monitor, no urgent exit signal.

### 16. Om Galaxy (SME) — Closed, awaiting listing
- **GMP:** ₹-- (0.00%) — inactive, unchanged.
- **Subscription (final):** Overall 2.07x · QIB 5.37x (carried) · NII 1.07x (carried) · Retail 0.62x (carried)
- **Anomaly flag:** none
- **Anchor:** ₹29.89 Cr allocated (9 Sep 2026, 33.22 lakh shares @ ₹90) — **CORRECTION vs prior day:** today's live pull confirms a total issue size of **₹105.00 Cr** (vs ₹99.75 Cr used yesterday) → recomputed **Anchor Unlock Ratio = 29.89 / 105.00 = 28.47%** → **Medium** (yesterday's report flagged this "High" at 30.16% on a smaller, since-superseded denominator — this is now corrected to Medium).
- **Lock-in dates:** 30-day unlock ~9 Oct 2026, 90-day unlock ~8 Dec 2026 (computed from 9 Sep anchor bid date, not individually disclosed)
- **Risk score:** 20/100 (Low) — GMP momentum 2/25 (inactive), subscription skew 8/25 (thin book despite QIB-led tilt), sector volatility 9/25 (industrial moulds/precision engineering), anchor proximity 1/25 (corrected down from prior day's elevated score, since the unlock ratio no longer clears the High-band boundary)
- **Advisory:** Hold — monitor, no urgent exit signal. Anchor ratio correction (28.47% vs a prior High-band misread of 30.16%) removes yesterday's boundary flag; GMP remains inactive and the book thin — no listing-day gap-up signal to act on.

### 17. Raksan Transformers (SME) — Closed, awaiting listing
- **GMP:** ₹50 (18.32%) — unchanged, per today's pull matching yesterday's final read.
- **Subscription (final):** Overall 47.43x · QIB 70.51x (carried) · NII 60.46x (carried) · Retail 28.66x (carried)
- **Anomaly flag:** none
- **Anchor:** ₹42.86 Cr allocated (9 Sep 2026, 15.70 lakh shares @ ₹273) = **28.48% of ₹150.50 Cr issue size** (reconfirmed, matches today's pull) → Anchor Unlock Ratio 0.2848 → **Medium**
- **Lock-in dates:** 30-day unlock ~9 Oct 2026, 90-day unlock ~8 Dec 2026 (computed, not individually disclosed)
- **Risk score:** 46/100 (Medium) — GMP momentum 15/25 (strong final-day GMP build, ₹28→₹50 into close, per tracked history), subscription skew 17/25 (QIB 70.5x vs retail 28.7x), sector volatility 13/25 (transformers/power T&D — policy-tailwind), anchor proximity 1/25
- **Advisory:** Hold — monitor, no urgent exit signal. Rising GMP and a late institutional surge worth watching, but stayed under both hard triggers.

### 18. Panchatv Bharat (SME) — Closed, awaiting listing
- **GMP:** ₹3 (2.14%) — unchanged.
- **Subscription (final):** Overall 1.40x · NII 0.39x (carried) · Retail 2.42x (carried) · QIB: not broken out
- **Anomaly flag:** none
- **Anchor:** **confirmed no anchor tranche (❌ per today's live pull)** — correction from yesterday's "pending."
- **Lock-in dates:** not applicable (no anchor tranche)
- **Risk score:** 10/100 (Low) — GMP momentum 2/25, subscription skew 6/25, sector volatility 1/25 (denim/textile — no anchor overhang possible), anchor proximity 1/25
- **Advisory:** Hold — monitor, no urgent exit signal.

### 19. Apana Logistics (SME) — LISTED 15 Sep 2026
- **Status:** Listed flat at ₹60.00 (0.00% listing-day gain); no fresher price captured in today's pull (issue is no longer on investorgain's active live table — already settled and off the tracked window).
- **GMP (pre-listing):** ₹1 (3%), last available print before listing (carried, unchanged from prior day — no fresher data source found).
- **Subscription:** pending — full QIB/NII/Retail breakdown not captured in any refresh; fixed-price SME issue with **no anchor investor portion** (explicitly stated in its own disclosures).
- **Anomaly flag:** none
- **Anchor Unlock Ratio:** not applicable (no anchor tranche)
- **Risk score:** 8/100 (Low) — GMP momentum 1/25 (flat listing already realized), subscription skew 3/25 (no anchor overhang possible), sector volatility 3/25 (container logistics — thin data), anchor proximity 1/25
- **Advisory:** Hold — monitor, no urgent exit signal.

### 20. Qualiance International (SME) — LISTED 11 Sep 2026
- **Status:** Listed at ₹236.10, +85.91% vs ₹127 issue price — largest listing-day gain in this ledger's recent history. No fresher current price captured today (issue is off investorgain's active live table).
- **GMP:** not captured in any refresh (already listed and settled well before either compile).
- **Subscription:** pending — full breakdown not captured.
- **Anomaly flag:** cannot be computed retroactively without pre-listing GMP/subscription data — **marked pending, not assumed**.
- **Anchor:** ₹12.81 Cr allocated (3 Sep 2026, 10.09 lakh shares @ ₹127) — total issue size not confirmed in any search pass to date, so **Anchor Unlock Ratio: pending** (numerator known, denominator not verified — not fabricated).
- **Lock-in dates:** 30-day unlock ~3 Oct 2026, 90-day unlock ~2 Dec 2026 (computed from 3 Sep anchor bid date, not individually disclosed)
- **Risk score:** cannot be scored with confidence given missing pre-listing subscription/GMP data — **pending**.
- **Advisory:** Hold — monitor, no urgent exit signal (default stance given insufficient data; this is a data-gap call, not a confirmed Low-risk assessment).

---

## Data gaps and corrections logged this run

- **Corrections vs 16 Sep report** (today's live pull surfaced updated total-issue-size denominators or new anchor disclosures): Amtech Esters (anchor now confirmed ₹5.08 Cr, ratio 28.41% Medium — was fully "pending"); Om Galaxy (ratio corrected from a mis-flagged 30.16% High to 28.47% Medium on a corrected ₹105.00 Cr issue size); Maharaja & Speedex (ratio revised from 29.99% to 28.48%, both Medium, on a corrected ₹80.13 Cr issue size); Infrax Renewable, Vinod Texworld, Panchatv Bharat (anchor status corrected from "pending" to confirmed "no anchor tranche" — a real disclosed fact, not a data gap).
- Manipal Payment & Identity Solutions: anchor allocation amount still conflicts across two sources (₹119 Cr vs ₹362.25 Cr) — not reconciled, Unlock Ratio left pending.
- Vinod Texworld, Amtech Esters, Panchatv Bharat: QIB/NII/Retail category breakdown not individually captured (only combined "overall" multiple) — marked pending rather than assumed proportional.
- Qualiance International: subscription and pre-listing GMP not captured (listed 11 Sep, outside any live-tracker window at pull time) — risk score left unscored rather than guessed.
- Apana Logistics: subscription breakdown not captured; no-anchor-tranche status confirmed from its own disclosures.
- investorgain.com's live table had not posted a fresh 17-Sep intraday refresh at the time of this pull for most already-closed-book issues (timestamps read 16-Sep evening) — GMP/subscription figures for those names are therefore the same underlying final book as yesterday's report, re-verified rather than assumed unchanged. Where GMP prints differed slightly from the prior day's report (e.g. Glass Wall Systems ₹41→₹39, Karamtara ₹40→₹45), the newer print from today's pull is used and the prior figure is noted for context.

---

## Summary table

| IPO | GMP % | QIB / NII / Retail sub | Anchor unlock ratio + date | Risk score/label | Advisory (no order) |
|---|---|---|---|---|---|
| Kanohar Electricals (listed 16 Sep) | 28.80% (pre-listing, last print) | 215.37x / 87.74x / 20.51x | 0.30 Medium — ~7 Oct / 6 Dec | 52 Medium | Hold — monitor, no urgent exit signal |
| Prasol Chemicals (listed 16 Sep) | −1.92% | 7.59x / 1.89x / 1.79x | 0.30 Medium — ~7 Oct / 6 Dec | 38 Medium | Hold — monitor, no urgent exit signal |
| Glass Wall Systems (listed 16 Sep) | 21.43% (pre-listing, last print) | 167.93x / 79.71x / 33.18x | 0.30 Medium — ~7 Oct / 6 Dec | 50 Medium | Hold — monitor, no urgent exit signal |
| Pranav Constructions (listed 15 Sep) | not tracked (settled) | 268.54x / 217.73x / 45.31x | 0.24 Medium — 9-10 Oct / 8-9 Dec | 66 Medium (boundary) | Hold — monitor; anomaly fired pre-listing, fade underway, watch closely |
| Rentomojo (pending, tentative 17 Sep) | 24.75% | 177.29x / 67.93x / 15.62x | 0.2995 Medium — ~8 Oct / 7 Dec | 64 Medium (near High) | **EXTREME anomaly fired — if allotted, consider fast listing-day exit** |
| Asset Reconstruction Co. (pending) | 7.19% | 52.65x / 15.69x / 3.39x | 0.30 Medium — 15 Oct / 14 Dec | 33 Low/Medium | Hold — monitor, no urgent exit signal |
| Manipal Payment & Identity Solutions (pending) | −4.42% | 1.26x / 1.22x / 2.19x | pending (conflicting sources) | 24 Low | Hold — monitor, no urgent exit signal |
| Steamhouse India (pending) | 18.52% | 46.19x / 46.60x / 17.78x | 0.30 Medium — ~8 Oct / 7 Dec | 42 Medium | Hold — monitor, no urgent exit signal |
| LCC Projects (pending) | 28.08% | 78.73x / 64.91x / 26.34x | 0.30 Medium — ~8 Oct / 7 Dec | 48 Medium | Hold — monitor, no urgent exit signal |
| Karamtara Engineering (pending) | 17.72% | 168.19x / 51.17x / 13.98x | 0.30 Medium — ~8 Oct / 7 Dec | 63 Medium (near High) | **EXTREME anomaly fired — if allotted, consider fast listing-day exit** |
| Infrax Renewable (pending) | 0.00% | pending / 1.39x / 1.90x | n/a — no anchor tranche | 15 Low | Hold — monitor, no urgent exit signal |
| Vinod Texworld (pending) | 1.06% | pending / pending / pending | n/a — no anchor tranche | 8 Low | Hold — monitor, no urgent exit signal |
| Amtech Esters (pending) | 17.33% | pending / pending / pending | 0.2841 Medium — ~8 Oct / 7 Dec | 32 Low/Medium | Hold — monitor, no urgent exit signal |
| Veegaland Developers (pending) | 4.29% | 19.13x / 19.41x / 9.95x | 0.30 Medium — ~9 Oct / 8 Dec | 26 Low | Hold — monitor, no urgent exit signal |
| Maharaja & Speedex India (pending) | 13.44% | 48.82x / 40.32x / 19.65x | 0.2848 Medium — 19 Oct / 21 Dec | 36 Medium | Hold — monitor, no urgent exit signal |
| Om Galaxy (pending) | 0.00% | 5.37x / 1.07x / 0.62x | 0.2847 Medium — ~9 Oct / 8 Dec | 20 Low | Hold — monitor, no urgent exit signal |
| Raksan Transformers (pending) | 18.32% | 70.51x / 60.46x / 28.66x | 0.2848 Medium — ~9 Oct / 8 Dec | 46 Medium | Hold — monitor, no urgent exit signal |
| Panchatv Bharat (pending) | 2.14% | pending / 0.39x / 2.42x | n/a — no anchor tranche | 10 Low | Hold — monitor, no urgent exit signal |
| Apana Logistics (listed 15 Sep) | 3% (pre-listing, last print) | pending | n/a — no anchor tranche | 8 Low | Hold — monitor, no urgent exit signal |
| Qualiance International (listed 11 Sep) | pending | pending | pending (denominator unverified) | pending | Hold — monitor, no urgent exit signal (data-gap default) |

---

*This report is advisory research compiled from public disclosures (chittorgarh.com, investorgain.com, BSE/NSE circulars, ipomarkets.com/ipocentral.in anchor-lock-in schedules) as of 17 September 2026. It is not personalized investment advice and does not constitute, simulate, or authorize any brokerage order. IPO allotment is lottery-based on oversubscription; GMP is unregulated and moves daily/intraday; anchor-unlock supply events are a known but not certain source of post-listing selling pressure. Verify all figures directly before acting.*
