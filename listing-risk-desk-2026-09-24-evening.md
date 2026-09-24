# IPO Listing-Day Risk Desk — 24 September 2026, 5:55 PM IST

**ADVISORY / REPORT ONLY.** No brokerage order was placed, simulated, or scripted. Fyers integration used read-only (quotes/holdings). Fyers holdings: **empty — no exposure to flag.**

## Recently listed (last 5 trading days)

### National Stock Exchange of India Ltd. (NSE:NSE, listed 24 Sep 2026)
- GMP pre-listing: ₹15 (0.84%) | Final subscription: 5.68x overall, 13.76x P/BV pure-OFS structure
- Live price: listed ₹1,800 (open), closed day ₹1,817 (+0.94% intraday / +1.79% vs ₹1,785 issue) — sourced web_search cross-check; Fyers symbol unresolved this run (guessed NSE-EQ/NATSTOCKEX-EQ/NSEINDIA-EQ/NSEIL-EQ/544937-EQ, none valid)
- Anchor unlock ratio: 14.94% (Low) — carried from 24 Sep morning run, no new anchor disclosure since
- Anomaly flags: none (sub <75x, GMP <50%)
- **Risk score: 22 (Low)**
- Recommendation: hold — monitor, no urgent exit signal.

### Sonaselection India Ltd. (listed 24 Sep 2026)
- GMP pre-listing: ₹0 (flat) | Final subscription: 0.20x — undersubscribed
- Live price: listed ₹102.21 (open, +3.24% vs discovered price), intraday ₹107.42 (+8.51%) — sourced web_search cross-check; Fyers symbol unresolved this run (guessed SONA/SONASELECT/SONASELECTION/SONASEL/SONO-EQ variants, none confirmed)
- Anchor unlock ratio: 15.0% (Medium) — carried from 24 Sep morning run
- Anomaly flags: none by the numeric thresholds, but flagging a genuine divergence — an undersubscribed 0.20x book produced an +8.51% listing-day pop, the opposite of the usual GMP/subscription-implied direction. Worth manual review for a possible unsustainable rally.
- **Risk score: 38 (Medium)** — divergence-adjusted
- Recommendation: hold — monitor, no urgent exit signal (score below High threshold, no anomaly flag technically fired, but flagged for the subscription/price divergence above).

### SpectraA Technology Solutions Ltd. (SME, closed 21 Sep, listing pending)
- GMP: ₹67 (56.78%) | Subscription: two disagreeing figures on record — press coverage 304.06x vs chittorgarh's reconciled Basis-of-Allotment 212.97x (both clear the anomaly threshold either way; discrepancy unresolved this run, Gemini cross-check unavailable — see below)
- Live Fyers price: not yet listed, no symbol
- Anchor unlock ratio: 14.22% (Low)
- **Anomaly flag: EXTREME** — subscription far exceeds 75x under either figure, GMP 56.78% approaches the 50%-of-issue-price threshold
- **Risk score: 78 (High)**
- Recommendation: **if allotted, consider selling within the first 15 minutes of listing** (High score + EXTREME anomaly).

### Kheria Autocomp Ltd. (SME, closed, listing pending)
- GMP: ₹3 (2.97%) | Subscription: 2.48x final overall
- Anchor unlock ratio: 14.25% (Low)
- Anomaly flags: none
- **Risk score: 18 (Low)**
- Recommendation: hold — monitor, no urgent exit signal.

### Axiom Gas Engineering Ltd. (SME, closed 22 Sep, listing pending)
- GMP: not yet disclosed | Subscription: 1.23x final overall (QIB 1.06x) — corrected in the ledger this run; the card's tags row had been carrying a stale 0.85x undersubscribed figure inconsistent with its own meta-line, fixed to match the meta-line's final 1.23x print
- Anchor unlock ratio: 5.69% (Low)
- Anomaly flags: none
- **Risk score: 24 (Low)**
- Recommendation: hold — monitor, no urgent exit signal.

### Varmora Granito Ltd. (Mainboard, closed bidding today 24 Sep 5 PM, listing 29 Sep)
- GMP: ₹1 (0.68%) | Final subscription: 1.55x overall (QIB 3.10x)
- Anchor unlock ratio: not yet disclosed for this fresh close — pending
- Anomaly flags: none
- **Risk score: 20 (Low)**
- Recommendation: hold — monitor, no urgent exit signal. Too early to call — bidding closed same-day, no listing-day data yet.

### Robokidz Eduventures Ltd. (SME, closed, listing pending)
- GMP: ₹55 (51.89%) | Subscription: 833.56x overall — extreme retail-driven demand
- Anchor unlock ratio: 28.23% of total issue (Medium-High band, computed this run: anchor shares 8,28,000 ÷ total issue shares 29,32,800)
- **Anomaly flag: EXTREME** — subscription and GMP both far exceed thresholds
- **Risk score: 91 (High)**
- Recommendation: **if allotted, consider selling within the first 15 minutes of listing** (High score + EXTREME anomaly — the single highest-risk gap-up signal in the tracked cohort this run).

## Gemini grounded cross-check
Not available this run — `~/.hermes/scripts/gemini_ground_check.py` returned "No GOOGLE_API_KEY or GEMINI_API_KEY set in environment" (recurring known configuration gap, not a quota/billing error this time). Skipped per skill instruction; all figures above rest on primary sources (chittorgarh.com, web_search cross-checks) only. SpectraA's subscription discrepancy (304.06x vs 212.97x) remains unresolved — flagging for manual review since the automated cross-check tool is unavailable.

## Fyers status
Holdings: empty, no exposure across any tracked IPO. Index quotes (Nifty/Sensex) pulled live and correct. Individual-stock symbol resolution failed for NSE, Sonaselection, Kheria Autocomp, and SpectraA this run despite ~20 combined ticker guesses — all five recently-closed/listed names' live prices are sourced from web_search cross-checks instead, not Fyers, this run. Worth a follow-up task to resolve correct NSE_CM_sym_master.json symbol mappings for these five names.
