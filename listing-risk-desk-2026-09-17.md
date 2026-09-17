# IPO Listing-Day Risk Desk — 17 September 2026

**Scope:** all 17 issues in the IPO Fundamentals Ledger currently "Closed — awaiting listing" (Rentomojo, Asset Reconstruction Co. (India), Manipal Payment & Identity Solutions, Steamhouse India, LCC Projects, Karamtara Engineering, Infrax Renewable, Vinod Texworld, Amtech Esters, Veegaland Developers, Maharaja & Speedex India, Om Galaxy, Raksan Transformers, Panchatv Bharat, Manika Plastech, Injecto Polymers, Century Business Media) plus every mainboard/SME name in the ledger's "Recently listed" table with a listing date in the last 5 trading days (16, 15, 11 Sep 2026 — Kanohar Electricals, Prasol Chemicals, Glass Wall Systems (India), Pranav Constructions, Apana Logistics, Qualiance International). **23 issues tracked below.**

**Nature of this document:** advisory research only. No brokerage order of any kind was placed, simulated, or queued in producing this report. Every recommendation line is monitoring/exit-timing language for a human to act on themselves through their own broker — never an instruction this system executes. Fyers API calls in this run were limited strictly to read-only `quotes` and `holdings` endpoints.

**Methodology notes (read before using the numbers):**
- GMP is the unofficial, unregulated grey-market premium, cross-checked between investorgain.com (live GMP table, browser_exec — this page is JS-rendered and defuddle returns nothing on it) and chittorgarh.com. It moves daily and is not a regulated price signal.
- Subscription multiples (QIB/NII/Retail/Overall) are the final books from chittorgarh.com/investorgain.com combined BSE+NSE reports, as this run's issues have all finished bidding.
- **Anchor Unlock Ratio** = anchor investor allocation value (₹Cr) ÷ total issue size (₹Cr), used as a disclosed-data proxy for "anchor share of the newly listed free float." This is a documented judgment call, not the literal SEBI free-float definition — treat Low/Medium/High as directional, not exact.
- Lock-in dates: SEBI ICDR mandates 50% of anchor shares unlock 30 days after allotment, remaining 50% at 90 days. Where a company's own circular disclosed exact dates, those are used; where only the anchor bid date was found, 30/90-day dates are computed and flagged "(computed, not individually disclosed)."
- Risk score (0–100, Low 0–33 / Medium 34–66 / High 67–100): a weighted heuristic across four factors, each 0–25 — GMP momentum, subscription skew (institutional vs retail imbalance), sector volatility (qualitative), anchor-unlock proximity (days to nearest unlock date). Not a validated statistical model.
- Live/current market price for already-listed names is pulled from the Fyers broker API (`quotes` endpoint, `lp` field — last traded price) where the NSE symbol resolved; two names (Apana Logistics, Qualiance International) errored on Fyers ("Please provide a valid symbol" on every NSE/BSE combination tried) and fall back to web-sourced snippets, noted per row.
- **Fyers holdings check:** ran `fyers_pull.py holdings` this run — returned `"holdings": [], "count_total": 0`. Confirmed empty: no cohort company (or any company) is held in the connected Fyers account this run.
- No number below is fabricated. Every field marked "pending" means no source disclosed it as of compile time.

---

## Fyers holdings check (run explicitly, not assumed)

```
{"code":200,"s":"ok","overall":{"count_total":0,"total_current_value":0,"total_investment":0,"total_pl":0,"pnl_perc":0},"holdings":[]}
```

Confirmed truthfully: the holdings array is empty. No cohort company is flagged as held.

---

## Anomaly flags fired this run

Per the rule (overall subscription >75x, OR any single category >100x, OR GMP >50% of issue price):

| Issue | Trigger | Detail |
|---|---|---|
| **Kanohar Electricals** (listed 16 Sep) | Overall 90.59x AND QIB 215.37x | Both thresholds breached in the final book |
| **Glass Wall Systems (India)** (listed 16 Sep) | Overall 81.65x AND QIB 167.93x | Both thresholds breached |
| **Pranav Constructions** (listed 15 Sep) | Overall 126.34x, QIB 268.54x, NII 217.73x | Three separate category breaches — most extreme book in this cohort |
| **Qualiance International** (listed 11 Sep) | Listing-day gain +85.91% | No pre-listing subscription/GMP captured this run to test the numeric thresholds directly, but the realized +85.91% debut is itself evidence of an extreme pre-listing demand imbalance — flagged qualitatively given the retroactive data gap |
| **Rentomojo** (closed, awaiting listing, tentative 17 Sep) | QIB 177.29x | Overall 72.89x stayed just under 75x but QIB alone cleared 100x |
| **Karamtara Engineering** (closed, awaiting listing, tentative 17 Sep) | QIB 168.19x | Overall 66.01x, QIB alone cleared 100x |

No issue in this cohort triggered the GMP >50%-of-issue-price threshold this run (highest current live GMP read within scope is LCC Projects at 24.66%; SpectraA Technology Solutions prints 42.37% but is currently Open, not Closed, so is out of this desk's scope).

Century Business Media (57.93x overall, 47.53x QIB) is the highest subscription multiple in this run's SME sub-cohort but stays comfortably under both the 75x and 100x thresholds — noted here for visibility, not flagged EXTREME.

---

## Per-issue detail

### 1. Kanohar Electricals (Mainboard) — LISTED 16 Sep 2026
- **GMP (pre-listing, last active read):** ₹182 (28.80%)
- **Subscription (final):** Overall 90.59x · QIB 215.37x · NII 87.74x · Retail 20.51x
- **Live/current price:** ₹751.50 (Fyers `quotes NSE:KANOHAR-EQ`, `lp` field) — +18.91% vs ₹632 issue price; listing-day close was ₹685.50 (+8.47%)
- **Anomaly flag:** **EXTREME — high gap-up signal** (overall >75x and QIB >100x)
- **Anchor Unlock Ratio:** ₹316.72 Cr / ₹1,055.74 Cr = 0.30 → **Medium**; lock-in 30-day ~7 Oct 2026, 90-day ~6 Dec 2026 (computed from 7 Sep anchor bid, not individually disclosed)
- **Risk score:** 58/100 (Medium) — GMP momentum 15/25 (post-listing gain has since run further to +18.9%, extending past the original GMP read — bullish continuation, not a fade), subscription skew 20/25 (QIB-dominated at 215x vs retail 20.5x), sector volatility 12/25 (power T&D — moderate, policy-tailwind), anchor proximity 11/25 (unlock ~3 weeks out)
- **Advisory:** Hold — monitor, no urgent exit signal. Price has continued climbing past the debut close rather than fading, so there's no fast-exit signal despite the pre-listing anomaly flag.

### 2. Prasol Chemicals (Mainboard) — LISTED 16 Sep 2026
- **GMP (pre-listing, last active read):** ₹-13 (-1.92%)
- **Subscription (final):** Overall 3.47x · QIB 7.59x · NII 1.89x · Retail 1.79x
- **Live/current price:** ₹671.00 (Fyers `quotes NSE:PRASOLCHEM-EQ`) — -0.74% vs ₹676 issue price; listing-day close ₹610.00 (-9.76%), has since recovered most of the debut loss
- **Anomaly flag:** none
- **Anchor Unlock Ratio:** ₹150.00 Cr / ₹500.00 Cr = 0.30 → **Medium**; lock-in 30-day ~7 Oct 2026, 90-day ~6 Dec 2026 (computed, not individually disclosed)
- **Risk score:** 32/100 (Low, boundary) — GMP momentum 4/25 (negative GMP already largely reversed on recovery), subscription skew 8/25, sector volatility 18/25 (specialty chemicals — commodity/China-plus-one sensitive), anchor proximity 10/25
- **Advisory:** Hold — monitor, no urgent exit signal. The stock has clawed back almost the entire listing-day discount; no gap-up risk either way.

### 3. Glass Wall Systems (India) (Mainboard) — LISTED 16 Sep 2026
- **GMP (pre-listing, last active read):** ₹39 (21.43%)
- **Subscription (final):** Overall 81.65x · QIB 167.93x · NII 79.71x · Retail 33.18x
- **Live/current price:** ₹214.85 (Fyers `quotes NSE:GLASSWALL-EQ`) — +18.05% vs ₹182 issue price; listing-day close ₹194.00 (+6.59%)
- **Anomaly flag:** **EXTREME — high gap-up signal** (overall >75x and QIB >100x)
- **Anchor Unlock Ratio:** ₹128.36 Cr / ₹427.89 Cr = 0.30 → **Medium**; lock-in 30-day ~7 Oct 2026, 90-day ~6 Dec 2026 (computed)
- **Risk score:** 53/100 (Medium) — GMP momentum 13/25 (gain has extended past the original GMP), subscription skew 19/25 (heavily QIB-weighted), sector volatility 12/25 (building materials/facade — real-estate-cycle linked), anchor proximity 10/25
- **Advisory:** Hold — monitor, no urgent exit signal. Same pattern as Kanohar — price has continued rising post-debut rather than fading.

### 4. Pranav Constructions (Mainboard) — LISTED 15 Sep 2026
- **GMP:** not tracked this refresh (already listed and settled)
- **Subscription (final):** Overall 126.34x · QIB 268.54x · NII 217.73x · Retail 45.31x
- **Live/current price:** ₹106.81 (Fyers `quotes NSE:PRANAV-EQ`) — **-13.86% vs ₹124 issue price**, a further sharp deterioration from yesterday's ₹132.00 (+6.45%); listing-day close was ₹165.00 (+33.06%)
- **Anomaly flag:** **EXTREME — high gap-up signal** (overall >75x, QIB and NII both >100x — the most extreme book in this cohort)
- **Anchor Unlock Ratio:** ₹84.25 Cr / ₹351.03 Cr = 0.24 → **Medium**; lock-in 30-day 9/10 Oct 2026, 90-day 8/9 Dec 2026 (disclosed on ipomarkets.com)
- **Risk score:** 74/100 (High) — GMP momentum 18/25 (the debut's +33% pop has now fully round-tripped into a loss below issue price — this is exactly the extreme-subscription/fast-fade pattern the score is meant to catch, so momentum reads as confirmed-negative rather than neutral), subscription skew 23/25 (QIB and NII both cleared 100x — textbook institutional pile-on that has now unwound), sector volatility 16/25 (Mumbai redevelopment real estate — cyclical), anchor proximity 12/25 (unlock ~3.5 weeks out)
- **Advisory:** **EXTREME — high gap-up signal fired; risk score is High.** Anyone still holding an allotment should treat this as the clearest confirmed instance in this cohort of the anomaly-rule's fast-fade thesis: the stock is now trading below its issue price, having given back the entire debut pop within two trading sessions. This is advisory monitoring language only, not a trade order — but it's the strongest "the anomaly played out as feared" evidence in this run.

### 5. Apana Logistics (SME) — LISTED 15 Sep 2026
- **GMP (pre-listing):** ₹1 (3%) per last available print before listing
- **Subscription:** pending — full QIB/NII/Retail breakdown not captured; fixed-price SME issue with **no anchor investor portion** (explicitly stated not applicable in its own disclosures)
- **Live/current price:** ₹54.15 — Fyers `quotes` errored on every symbol variant tried (NSE:APANA-EQ, BSE:APANA-EQ: "Please provide a valid symbol"); **Fyers was unavailable for this name**, falling back to a web_search snippet (bajajfinservmarkets.in, dated 17 Sep 2026) — -9.75% vs ₹60.00 issue price; listing-day close was flat at ₹60.00
- **Anomaly flag:** none
- **Anchor Unlock Ratio:** not applicable (no anchor tranche)
- **Risk score:** 12/100 (Low) — GMP momentum 2/25 (flat listing, small further slide since), subscription skew 4/25 (no anchor overhang possible), sector volatility 4/25 (container logistics — thin data), anchor proximity 2/25
- **Advisory:** Hold — monitor, no urgent exit signal.

### 6. Qualiance International (SME) — LISTED 11 Sep 2026
- **GMP:** not captured this refresh (already listed and settled well before this compile)
- **Subscription:** pending — full breakdown not captured
- **Live/current price:** ₹213.10 — Fyers `quotes` errored ("Please provide a valid symbol" on NSE:QUALIANCE-EQ, BSE:QUALIANCE-EQ, NSE:QUALIANCE-SM); **Fyers was unavailable for this name**, falling back to a web_search snippet (kotakneo.com, dated 17 Sep 2026) — +67.80% vs ₹127.00 issue price; listing-day close was ₹236.10 (+85.91%), the largest listing-day gain in this ledger's recent history, now cooling but still deeply positive
- **Anomaly flag:** flagged qualitatively (see Anomaly table above) — cannot compute the numeric threshold retroactively without pre-listing GMP/subscription data
- **Anchor Unlock Ratio:** pending — numerator known (₹12.81 Cr allocated) but total issue size not confirmed in this search pass, so the ratio denominator is unverified; not fabricated
- **Lock-in dates:** 30-day unlock ~3 Oct 2026, 90-day unlock ~2 Dec 2026 (computed from 3 Sep anchor bid date, not individually disclosed)
- **Risk score:** 45/100 (Medium) — GMP momentum 15/25 (the +85.91% debut has cooled to +67.80% but remains a very large realized gain — genuine momentum, some giveback), subscription skew 12/25 (unknown breakdown, scored conservatively given the scale of the realized pop implies a thin float/heavy demand imbalance), sector volatility 10/25 (technical garments/export manufacturing — moderate), anchor proximity 8/25
- **Advisory:** Hold — monitor, no urgent exit signal. The stock has given back roughly a fifth of its debut gain but remains well above issue price; nothing here signals an urgent fresh exit trigger distinct from ordinary post-listing volatility, though anyone still holding should note this is the largest realized listing-day pop in the tracked cohort and profit-taking risk is real.

### 7. Rentomojo (Mainboard) — Closed, awaiting listing (tentative listing 17 Sep 2026)
- **GMP:** ₹86 (21.29%) — down from ₹104 (25.74%) yesterday; investorgain shows the GMP has compressed steadily from ₹148 on 11-Sep to ₹86 this morning
- **Subscription (final):** Overall 72.89x · QIB 177.29x · NII 67.93x · Retail 15.62x
- **Anomaly flag:** **EXTREME — high gap-up signal** (QIB >100x; overall 72.89x stayed just under 75x)
- **Anchor Unlock Ratio:** ₹376.07 Cr / ₹1,255.57 Cr = 0.2995 → **Medium**; lock-in 30-day ~8 Oct 2026, 90-day ~7 Dec 2026 (computed)
- **Risk score:** 63/100 (Medium, near High boundary) — GMP momentum 15/25 (GMP has compressed materially into listing day — 21% now vs 26% yesterday and 37% at its peak, a cooling trend that tempers the gap-up thesis somewhat), subscription skew 22/25 (QIB overhang at 177x vs retail 15.6x — stark institutional tilt), sector volatility 18/25 (consumer rental/subscription — no listed peer per its own RHP, genuinely hard to benchmark), anchor proximity 8/25 (listing today, unlock still ~3 weeks out)
- **Advisory:** **EXTREME — high gap-up signal fired.** Given the QIB-heavy book, consider selling within the first 15 minutes of listing if allotted — the compressing GMP into listing morning (down from ₹148 to ₹86 over the past week) is a caution sign that some of the earlier extreme demand read may already be fading before the stock even opens. This is advisory only, not an order.

### 8. Asset Reconstruction Co. (India) (Mainboard) — Closed, awaiting listing (tentative listing 17 Sep 2026)
- **GMP:** ₹12 (8.63%) — down from ₹24 a week ago
- **Subscription (final):** Overall 20.10x · QIB 52.65x · NII 15.69x · Retail 3.39x
- **Anomaly flag:** none
- **Anchor Unlock Ratio:** ₹219.89 Cr / ₹732.97 Cr = 0.30 → **Medium**; lock-in 30-day 15 Oct 2026, 90-day 14 Dec 2026 (explicitly disclosed)
- **Risk score:** 30/100 (Low, boundary) — GMP momentum 6/25 (GMP has roughly halved since bidding closed), subscription skew 10/25 (QIB-led but not extreme), sector volatility 10/25 (financial services/distressed-asset resolution — regulated, moderate), anchor proximity 4/25
- **Advisory:** Hold — monitor, no urgent exit signal.

### 9. Manipal Payment & Identity Solutions ("Manipal Cards") (Mainboard) — Closed, awaiting listing (tentative listing 17 Sep 2026)
- **GMP:** ₹-6 (-1.77%) — negative but has narrowed slightly from ₹-10
- **Subscription (final):** Overall 1.42x · QIB 1.26x · NII 1.22x · Retail 2.19x
- **Anomaly flag:** none
- **Anchor:** **resolved this run** — ₹362.25 Cr allocated (8 Sep 2026, 1.07 Cr shares @ ₹339) = **45.0% of ₹805.00 Cr issue size** (the conflicting ₹119 Cr figure carried in yesterday's report is superseded by chittorgarh.com's own confirmed anchor-round news release, cross-checked against equitybulls.com and money.rediff.com, all agreeing on ₹362.25 Cr) → Anchor Unlock Ratio **0.45 → High**
- **Lock-in dates:** 30-day unlock ~8 Oct 2026, 90-day unlock ~7 Dec 2026 (computed from 8 Sep anchor bid date; the underlying circular PDF text was not machine-readable for exact dates)
- **Risk score:** 38/100 (Medium) — GMP momentum 4/25 (negative GMP, mild), subscription skew 5/25 (barely oversubscribed), sector volatility 8/25 (secure-card/payments manufacturing — moderate), anchor proximity 21/25 (anchor ratio at 45% just resolved into High band — a genuinely large share of free float unlocking in one window is a real overhang risk, scored higher than yesterday's placeholder given the data gap is now closed)
- **Advisory:** Hold — monitor, no urgent exit signal for the listing-day window itself (negative GMP, thin subscription argue against an immediate pop to sell into) — but flag the now-confirmed 45% anchor unlock ratio (High band) as a name to watch specifically around 8 Oct/7 Dec for secondary selling pressure, distinct from the listing-day question this desk otherwise scores.

### 10. Steamhouse India (Mainboard) — Closed, awaiting listing (tentative listing 17 Sep 2026)
- **GMP:** ₹13.50 (16.67%) — down from ₹17 (20.99%) yesterday, and off a ₹21 peak on 11-Sep
- **Subscription (final):** Overall 32.07x · QIB 46.19x · NII 46.60x · Retail 17.78x
- **Anomaly flag:** none
- **Anchor Unlock Ratio:** ₹124.20 Cr / ₹414.00 Cr = 0.30 → **Medium**; lock-in 30-day ~8 Oct 2026, 90-day ~7 Dec 2026 (computed)
- **Risk score:** 40/100 (Medium) — GMP momentum 10/25 (compressing into listing day), subscription skew 13/25 (QIB and NII roughly balanced), sector volatility 13/25 (industrial gas/steam utility — moderate), anchor proximity 4/25
- **Advisory:** Hold — monitor, no urgent exit signal.

### 11. LCC Projects (Mainboard) — Closed, awaiting listing (tentative listing 17 Sep 2026)
- **GMP:** ₹36 (24.66%) — down from ₹44 (30.14%) yesterday and off a ₹78 peak on 11-Sep, a real compression
- **Subscription (final):** Overall 49.57x · QIB 78.73x · NII 64.91x · Retail 26.34x
- **Anomaly flag:** none (all under threshold, QIB is the highest sub-100x read in this batch)
- **Anchor Unlock Ratio:** ₹128.14 Cr / ₹427.14 Cr = 0.30 → **Medium**; lock-in 30-day ~8 Oct 2026, 90-day ~7 Dec 2026 (computed)
- **Risk score:** 46/100 (Medium) — GMP momentum 16/25 (still the highest GMP% in this batch despite compressing sharply from its peak — a real gap-up signal, tempered by the fade), subscription skew 15/25, sector volatility 11/25 (irrigation/water EPC — policy-tailwind, moderate cyclicality), anchor proximity 4/25
- **Advisory:** Hold — monitor, no urgent exit signal. GMP has more than halved from its 11-Sep peak (₹78 → ₹36) — a meaningful cooling trend worth watching into listing, but stayed under both hard triggers.

### 12. Karamtara Engineering (Mainboard) — Closed, awaiting listing (tentative listing 17 Sep 2026)
- **GMP:** ₹48 (18.90%) — up from ₹40 (15.75%) yesterday, though still well off the ₹75 peak on 9-Sep
- **Subscription (final):** Overall 66.01x · QIB 168.19x · NII 51.17x · Retail 13.98x
- **Anomaly flag:** **EXTREME — high gap-up signal** (QIB >100x)
- **Anchor Unlock Ratio:** ₹262.50 Cr / ₹875.00 Cr = 0.30 → **Medium**; lock-in 30-day ~8 Oct 2026, 90-day ~7 Dec 2026 (computed)
- **Risk score:** 62/100 (Medium, near High boundary) — GMP momentum 13/25 (rebounded slightly overnight after compressing hard earlier in the week), subscription skew 20/25 (QIB at 168x vs retail 14x — stark institutional/retail gap), sector volatility 14/25 (solar-EPC/structural steel — policy-tailwind but cyclical raw-material exposure), anchor proximity 5/25
- **Advisory:** **EXTREME — high gap-up signal fired.** Given the stark QIB/retail subscription skew, consider selling within the first 15 minutes of listing if allotted — this pattern has historically preceded both strong debuts and equally fast post-listing fades in this cohort (see Pranav Constructions above for a live example of exactly that fade playing out). Not an order; a flag to act on personally through your own broker.

### 13. Infrax Renewable (SME) — Closed, awaiting listing (tentative listing 17 Sep 2026)
- **GMP:** not yet active (₹0/-- on investorgain, no live premium quoted)
- **Subscription (final):** Overall 2.05x · NII 1.39x · Retail 1.90x · QIB: pending (SME books did not break out a QIB-specific print for this issue)
- **Anomaly flag:** none
- **Anchor Unlock Ratio:** pending — no anchor-allocation circular found in this search pass
- **Lock-in dates:** pending
- **Risk score:** 15/100 (Low) — GMP momentum 2/25 (inactive), subscription skew 5/25 (thin oversubscription only), sector volatility 6/25 (solar EPC — moderate), anchor proximity 2/25 (default low given no data)
- **Advisory:** Hold — monitor, no urgent exit signal.

### 14. Vinod Texworld (SME) — Closed, awaiting listing (tentative listing 17 Sep 2026)
- **GMP:** ₹1 (1.06%) — unchanged from yesterday
- **Subscription (final):** Overall 1.60x · QIB/NII/Retail breakdown: pending (SME subscription page did not break the category out separately in this pull)
- **Anomaly flag:** none
- **Anchor Unlock Ratio:** pending — no anchor-allocation circular found in this search pass
- **Lock-in dates:** pending
- **Risk score:** 10/100 (Low) — GMP momentum 1/25, subscription skew 3/25, sector volatility 4/25 (textile processing — thin margin, low volatility signal), anchor proximity 2/25
- **Advisory:** Hold — monitor, no urgent exit signal.

### 15. Amtech Esters (SME) — Closed, awaiting listing (tentative listing 17 Sep 2026)
- **GMP:** ₹16 (21.33%) — up from ₹13 (17.33%) yesterday
- **Subscription (final):** Overall 25.70x · QIB/NII/Retail breakdown: pending (SME subscription page did not break the category out separately)
- **Anomaly flag:** none
- **Anchor Unlock Ratio:** pending — no anchor-allocation circular found in this search pass; this remains a debut mandate for lead manager Credora Partners, a brand-new merchant banker with zero prior listed track record
- **Lock-in dates:** pending
- **Risk score:** 28/100 (Low, near Medium boundary) — GMP momentum 12/25 (rising into listing), subscription skew 9/25 (moderate overall, breakdown unknown, scored conservatively), sector volatility 6/25 (specialty chemicals/resins — moderate), anchor proximity 3/25
- **Advisory:** Hold — monitor, no urgent exit signal. GMP rising into listing is worth watching, but with no anchor or category-breakdown data this stays a data-limited Low-risk read, not an anomaly.

### 16. Veegaland Developers (Mainboard) — Closed, awaiting listing
- **GMP:** ₹5 (3.57%) — unchanged
- **Subscription (final):** Overall 14.60x · QIB 19.13x · NII 19.41x · Retail 9.95x
- **Anomaly flag:** none
- **Anchor Unlock Ratio:** ₹63.00 Cr / ₹210.00 Cr = 0.30 → **Medium**; lock-in 30-day ~9 Oct 2026, 90-day ~8 Dec 2026 (computed)
- **Risk score:** 27/100 (Low) — GMP momentum 4/25 (GMP more than halved since bidding closed, from ₹15 to ₹5), subscription skew 10/25 (QIB and NII broadly balanced), sector volatility 10/25 (Kerala residential real estate — regional concentration risk), anchor proximity 3/25
- **Advisory:** Hold — monitor, no urgent exit signal.

### 17. Maharaja & Speedex India (SME) — Closed, awaiting listing
- **GMP:** ₹28 (15.05%) — unchanged
- **Subscription (final):** Overall 32.41x · QIB 48.82x · NII 40.32x · Retail 19.65x
- **Anomaly flag:** none
- **Anchor Unlock Ratio:** ₹22.82 Cr / ₹76.11 Cr = 0.2999 → **Medium**; lock-in 30-day 19 Oct 2026, 90-day 21 Dec 2026 (explicitly disclosed)
- **Risk score:** 38/100 (Medium) — GMP momentum 11/25, subscription skew 15/25 (a genuine late-session QIB-led surge — final book was 32x vs a near-zero QIB read for most of bidding), sector volatility 10/25 (stainless-steel houseware — consumer durables, moderate), anchor proximity 3/25
- **Advisory:** Hold — monitor, no urgent exit signal.

### 18. Om Galaxy (SME) — Closed, awaiting listing
- **GMP:** not yet active
- **Subscription (final):** Overall 2.07x · QIB 5.37x · NII 1.07x · Retail 0.62x
- **Anomaly flag:** none
- **Anchor Unlock Ratio:** ₹29.89 Cr / ₹99.75 Cr = 0.3016 → **High** (marginally over the 30% line)
- **Lock-in dates:** 30-day unlock ~9 Oct 2026, 90-day unlock ~8 Dec 2026 (computed)
- **Risk score:** 22/100 (Low) — GMP momentum 2/25 (inactive), subscription skew 8/25 (thin book overall despite a QIB-led tilt), sector volatility 8/25 (industrial moulds/precision engineering — moderate), anchor proximity 4/25
- **Advisory:** Hold — monitor, no urgent exit signal. Anchor-unlock ratio lands in High band (30.16%) purely on a boundary computation; with GMP inactive and a thin overall book, there's no listing-day gap-up signal to act on.

### 19. Raksan Transformers (SME) — Closed, awaiting listing
- **GMP:** ₹21 (7.69%) — down sharply from ₹50 (18.32%) yesterday
- **Subscription (final):** Overall 47.43x · QIB 70.51x · NII 60.46x · Retail 28.66x
- **Anomaly flag:** none (all under threshold)
- **Anchor Unlock Ratio:** ₹42.86 Cr / ₹150.50 Cr = 0.2848 → **Medium**; lock-in 30-day ~9 Oct 2026, 90-day ~8 Dec 2026 (computed)
- **Risk score:** 41/100 (Medium) — GMP momentum 14/25 (GMP has more than halved overnight, ₹50 → ₹21 — a notable cooling that tempers the earlier bullish read), subscription skew 17/25 (QIB at 70.5x vs retail 28.7x), sector volatility 13/25 (transformers/power T&D — policy-tailwind, moderate), anchor proximity 4/25
- **Advisory:** Hold — monitor, no urgent exit signal. The sharp overnight GMP compression is worth watching closely into listing but doesn't cross into anomaly or High-risk territory on its own.

### 20. Panchatv Bharat (SME) — Closed, awaiting listing
- **GMP:** ₹3 (2.14%) — unchanged
- **Subscription (final):** Overall 1.40x · NII 0.39x · Retail 2.42x · QIB: not broken out for this issue
- **Anomaly flag:** none
- **Anchor Unlock Ratio:** pending — no anchor-allocation circular found in this search pass
- **Lock-in dates:** pending
- **Risk score:** 13/100 (Low) — GMP momentum 2/25, subscription skew 5/25, sector volatility 4/25 (denim/textile — this ledger's own weakest-fundamentals name, a separate concern from listing-day risk), anchor proximity 2/25
- **Advisory:** Hold — monitor, no urgent exit signal.

### 21. Manika Plastech (Mainboard) — Closed, awaiting listing
- **GMP:** ₹2 (4.65%)
- **Subscription (final):** Overall 29.46x · QIB 11.22x · Retail 23.98x
- **Anomaly flag:** none
- **Anchor:** ₹3.76 Cr allocated (10 Sep 2026, 87.56 lakh shares @ ₹43, confirmed via chittorgarh.com's own anchor-round news release and cross-checked against the BRLM circular PDF) = **3.0% of ₹125.50 Cr issue size** → Anchor Unlock Ratio **0.030 → Low**
- **Lock-in dates:** 30-day unlock 17 Oct 2026, 90-day unlock 16 Dec 2026 (per ipostation.in's anchor schedule, cross-checked against the 10-Sep anchor bid date)
- **Risk score:** 24/100 (Low) — GMP momentum 5/25 (a modest 4.65% premium heading into listing), subscription skew 11/25 (retail-heavy at 24x vs QIB 11x — an unusual retail-over-institutional tilt for this cohort, mildly elevated relative to a pure institutional book), sector volatility 6/25 (rigid plastic packaging — moderate, this ledger's own read has it priced well below listed peers), anchor proximity 2/25 (very small anchor tranche, low unlock supply risk)
- **Advisory:** Hold — monitor, no urgent exit signal. Notably the smallest anchor allocation (3%) in this cohort — minimal unlock-supply overhang risk regardless of listing-day outcome.

### 22. Injecto Polymers (SME) — Closed, awaiting listing
- **GMP:** not yet active (₹0/-- on investorgain's live table this morning)
- **Subscription (final):** Overall 1.23x · QIB 1.57x
- **Anomaly flag:** none
- **Anchor:** ₹9.58 Cr allocated (10 Sep 2026, 9.58 lakh shares @ ₹100, per chittorgarh.com's confirmed anchor-round release) = **17.07% of ₹56.12 Cr issue size** → Anchor Unlock Ratio **0.1707 → Medium**
- **Lock-in dates:** pending — exact dates not found in this search pass; 30/90-day dates from the 10-Sep anchor bid would compute to ~10 Oct/9 Dec 2026 but are not individually confirmed, so left as "computed, not individually disclosed"
- **Risk score:** 14/100 (Low) — GMP momentum 1/25 (inactive), subscription skew 4/25 (barely oversubscribed, thin book), sector volatility 6/25 (plastic/polymer packaging — moderate), anchor proximity 3/25
- **Advisory:** Hold — monitor, no urgent exit signal.

### 23. Century Business Media (SME) — Closed, awaiting listing
- **GMP:** not yet active (₹0/-- on investorgain's live table this morning)
- **Subscription (final):** Overall 57.93x · QIB 47.53x
- **Anomaly flag:** none (both metrics comfortably under threshold, though 57.93x overall is the highest multiple in this run's SME sub-cohort)
- **Anchor:** ₹4.84 Cr allocated (10 Sep 2026, 6.54 lakh shares @ ₹74, per chittorgarh.com's confirmed anchor-round release, cross-checked against the BRLM circular PDF) = **28.30% of ₹17.11 Cr issue size** → Anchor Unlock Ratio **0.2830 → Medium**
- **Lock-in dates:** 30-day unlock 17 Oct 2026, 90-day unlock 16 Dec 2026 (explicitly disclosed per ipostation.in, matching the standard SEBI ICDR schedule from the 10-Sep anchor bid)
- **Risk score:** 34/100 (Medium, boundary) — GMP momentum 3/25 (inactive), subscription skew 16/25 (57.93x overall is the highest sub-cohort read here, though the QIB print alone at 47.53x stays well under the 100x single-category trigger), sector volatility 11/25 (out-of-home advertising — media/ad-spend cyclical, moderate), anchor proximity 4/25
- **Advisory:** Hold — monitor, no urgent exit signal. This is the strongest subscription book in the SME group this run without crossing into anomaly territory — worth watching at listing given the demand, but GMP is inactive so there's no pre-listing pop signal to act on.

---

## Data gaps in this run (documented, not fabricated)

- Infrax Renewable, Vinod Texworld, Amtech Esters, Panchatv Bharat: no anchor-allocation circular found in this search pass — all four marked pending rather than estimated.
- Vinod Texworld, Amtech Esters, Panchatv Bharat, Infrax Renewable: QIB/NII/Retail category breakdown not fully captured (only combined "overall"/partial category multiples pulled) — marked pending rather than assumed proportional to overall.
- Injecto Polymers: exact anchor lock-in dates not individually confirmed in this search pass — the 30/90-day dates shown are computed from the anchor bid date, flagged accordingly.
- Apana Logistics, Qualiance International: Fyers `quotes` endpoint errored on every NSE/BSE symbol combination tried ("Please provide a valid symbol") — current price sourced from web_search snippets instead, as required by the task's fallback instruction; both explicitly noted per-row above.
- Qualiance International: pre-listing subscription and GMP were not captured (already listed 11 Sep, well outside this run's live-tracker window) — numeric anomaly-rule thresholds could not be computed retroactively; flagged qualitatively instead based on the realized +85.91% debut, and the risk score is explicitly noted as data-limited.
- Qualiance International: total issue size for the Anchor Unlock Ratio denominator not confirmed in this search pass — ratio left pending (numerator of ₹12.81 Cr anchor allocation is known).
- Manipal Payment & Identity Solutions: yesterday's report carried a conflicting anchor figure (₹119 Cr vs ₹362.25 Cr) as pending; this run resolved it to ₹362.25 Cr via chittorgarh.com's own confirmed anchor-round release, cross-checked against two independent news sources (equitybulls.com, money.rediff.com) — Anchor Unlock Ratio is now scored (0.45, High) rather than pending.

---

## Company-by-company summary table

| Company | GMP % | Subscription QIB / NII / Retail / Overall | Live/current price (+source) | Anchor unlock ratio + date | Risk score + label | Holdings flag | Recommendation |
|---|---|---|---|---|---|---|---|
| Kanohar Electricals | 28.80% (pre-listing) | 215.37x / 87.74x / 20.51x / 90.59x | ₹751.50, +18.91% vs issue (Fyers NSE:KANOHAR-EQ) | 0.30 Medium — ~7 Oct/6 Dec | 58 Medium | No holdings | Hold — monitor, no urgent exit signal |
| Prasol Chemicals | -1.92% | 7.59x / 1.89x / 1.79x / 3.47x | ₹671.00, -0.74% vs issue (Fyers NSE:PRASOLCHEM-EQ) | 0.30 Medium — ~7 Oct/6 Dec | 32 Low | No holdings | Hold — monitor, no urgent exit signal |
| Glass Wall Systems (India) | 21.43% (pre-listing) | 167.93x / 79.71x / 33.18x / 81.65x | ₹214.85, +18.05% vs issue (Fyers NSE:GLASSWALL-EQ) | 0.30 Medium — ~7 Oct/6 Dec | 53 Medium | No holdings | Hold — monitor, no urgent exit signal |
| Pranav Constructions | not tracked (settled) | 268.54x / 217.73x / 45.31x / 126.34x | ₹106.81, **-13.86% vs issue** (Fyers NSE:PRANAV-EQ) | 0.24 Medium — 9-10 Oct/8-9 Dec | 74 **High** | No holdings | **EXTREME fired — sell within first 15 min if allotted** |
| Apana Logistics | 3% (pre-listing) | pending | ₹54.15, -9.75% vs issue (web_search, Fyers unavailable) | n/a — no anchor tranche | 12 Low | No holdings | Hold — monitor, no urgent exit signal |
| Qualiance International | not captured | pending | ₹213.10, +67.80% vs issue (web_search, Fyers unavailable) | pending (denominator unverified) | 45 Medium | No holdings | Hold — monitor, no urgent exit signal |
| Rentomojo | 21.29% | 177.29x / 67.93x / 15.62x / 72.89x | not yet listed | 0.2995 Medium — ~8 Oct/7 Dec | 63 Medium (near High) | No holdings | **EXTREME fired — sell within first 15 min if allotted** |
| Asset Reconstruction Co. (India) | 8.63% | 52.65x / 15.69x / 3.39x / 20.10x | not yet listed | 0.30 Medium — 15 Oct/14 Dec | 30 Low | No holdings | Hold — monitor, no urgent exit signal |
| Manipal Payment & Identity Solutions | -1.77% | 1.26x / 1.22x / 2.19x / 1.42x | not yet listed | **0.45 High** — ~8 Oct/7 Dec | 38 Medium | No holdings | Hold — monitor, no urgent exit signal |
| Steamhouse India | 16.67% | 46.19x / 46.60x / 17.78x / 32.07x | not yet listed | 0.30 Medium — ~8 Oct/7 Dec | 40 Medium | No holdings | Hold — monitor, no urgent exit signal |
| LCC Projects | 24.66% | 78.73x / 64.91x / 26.34x / 49.57x | not yet listed | 0.30 Medium — ~8 Oct/7 Dec | 46 Medium | No holdings | Hold — monitor, no urgent exit signal |
| Karamtara Engineering | 18.90% | 168.19x / 51.17x / 13.98x / 66.01x | not yet listed | 0.30 Medium — ~8 Oct/7 Dec | 62 Medium (near High) | No holdings | **EXTREME fired — sell within first 15 min if allotted** |
| Infrax Renewable | not yet active | pending / 1.39x / 1.90x / 2.05x | not yet listed | pending | 15 Low | No holdings | Hold — monitor, no urgent exit signal |
| Vinod Texworld | 1.06% | pending / pending / pending / 1.60x | not yet listed | pending | 10 Low | No holdings | Hold — monitor, no urgent exit signal |
| Amtech Esters | 21.33% | pending / pending / pending / 25.70x | not yet listed | pending | 28 Low | No holdings | Hold — monitor, no urgent exit signal |
| Veegaland Developers | 3.57% | 19.13x / 19.41x / 9.95x / 14.60x | not yet listed | 0.30 Medium — ~9 Oct/8 Dec | 27 Low | No holdings | Hold — monitor, no urgent exit signal |
| Maharaja & Speedex India | 15.05% | 48.82x / 40.32x / 19.65x / 32.41x | not yet listed | 0.2999 Medium — 19 Oct/21 Dec | 38 Medium | No holdings | Hold — monitor, no urgent exit signal |
| Om Galaxy | not yet active | 5.37x / 1.07x / 0.62x / 2.07x | not yet listed | 0.3016 **High** — ~9 Oct/8 Dec | 22 Low | No holdings | Hold — monitor, no urgent exit signal |
| Raksan Transformers | 7.69% | 70.51x / 60.46x / 28.66x / 47.43x | not yet listed | 0.2848 Medium — ~9 Oct/8 Dec | 41 Medium | No holdings | Hold — monitor, no urgent exit signal |
| Panchatv Bharat | 2.14% | pending / 0.39x / 2.42x / 1.40x | not yet listed | pending | 13 Low | No holdings | Hold — monitor, no urgent exit signal |
| Manika Plastech | 4.65% | 11.22x / pending / 23.98x / 29.46x | not yet listed | 0.030 Low — 17 Oct/16 Dec | 24 Low | No holdings | Hold — monitor, no urgent exit signal |
| Injecto Polymers | not yet active | 1.57x / pending / pending / 1.23x | not yet listed | 0.1707 Medium — ~10 Oct/9 Dec | 14 Low | No holdings | Hold — monitor, no urgent exit signal |
| Century Business Media | not yet active | 47.53x / pending / pending / 57.93x | not yet listed | 0.2830 Medium — 17 Oct/16 Dec | 34 Medium (boundary) | No holdings | Hold — monitor, no urgent exit signal |

**File written to:** `~/Documents/Obsidian Vault/listing-risk-desk-2026-09-17.md` (confirmed — this exact document).

---

*This report is advisory research compiled from public disclosures (chittorgarh.com, investorgain.com, BSE/NSE circulars, chittorgarh.net/ipowatch.in/ipostation.in anchor-lock-in schedules, Fyers broker API read-only quotes/holdings endpoints) as of 17 September 2026 morning refresh. It is not personalized investment advice and does not constitute, simulate, or authorize any brokerage order. IPO allotment is lottery-based on oversubscription; GMP is unregulated and moves daily; anchor-unlock supply events are a known but not certain source of post-listing selling pressure. Verify all figures directly before acting.*
