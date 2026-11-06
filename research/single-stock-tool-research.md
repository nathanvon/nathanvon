# Single-Stock Intelligence System — Research & Build Plan

**Date:** 2026-11-06 · **Pilot stock:** Micron (MU) · **Status:** Research complete, build not started

This document synthesizes research into how best-in-class investors analyze and trade a single stock, what signals have real evidence behind them, what tools and data exist, and how to build a personal system that covers: fundamentals, entry/exit discipline, proactive event monitoring, options P/L scenarios, and backtesting. Everything here is educational research for building a decision-support tool — not financial advice.

---

## 1. The diagnosis: what happened with MU, and why it was foreseeable

The trigger for this project: bought MU above $900, then watched it drop ~20% with no warning and no plan.

**What actually happened (Nov 2026):**
- MU ran ~900% from its lows to a June 25, 2026 closing high of **$1,213.56** (~$1.35T market cap) on the HBM/AI memory supercycle.
- **Nov 2:** Kioxia's cautious outlook hit memory names (MU −4%). MU was already −22% over the trailing month.
- **Nov 4:** MU −7% to $795 as scrutiny grew on how long AI capex and memory price increases can last.
- **Nov 5:** MU −17.5% to **$656.39** — inside a market-wide crash (Nasdaq −5.5%, worst since Apr 2025) triggered by midterm-election AI-regulation fears, Qualcomm's weak forecast, and debt-financed AI-buildout worries. AMD −17%, NVDA −9%.
- Cumulative: MU is down ~40–46% from the June peak. A buyer above $900 is down ~27% at $656.

**The two key lessons:**

1. **The low-P/E trap.** MU looked "cheap" at $900+ (single-digit P/E). For memory stocks, a low P/E on peak earnings is historically a *sell signal, not a bargain* — the multiple contracts as earnings peak and expands into the trough. Memory stocks peak months before their earnings do. Every disciplined memory framework (Morgan Stanley's "Winter" series, UBS's book-value anchoring) prices the *cycle*, not the multiple.
2. **Every catalyst was on a knowable calendar.** Kioxia/competitor earnings, hyperscaler capex scrutiny, the US midterms, Qualcomm's report — all were scheduled or category-predictable events. A pre-mortem written in October ("assume this position blew up — why?") would have listed competitor guidance cuts, AI-capex sentiment reversal, and regulatory shock. All three fired within one week. Proactivity = maintaining the catalyst calendar *before* events, not reacting after.

**Historical context for what comes next:** MU's memory-downcycle drawdowns: −77% (2008–09), −73% (2014–16), −55% (2018), −49/−51% (2021–22), −36% (2024). Average across 15 major shocks: −34%; >50% is common. The current ~40–46% drawdown is within historical norms — and troughs have produced multi-bagger recoveries. **Price alone cannot tell a mid-cycle shakeout from a cycle top.** The monitorable tells: DRAM/NAND contract-price direction (TrendForce), HBM contract integrity, hyperscaler capex revisions, competitor guidance.

---

## 2. How best-in-class investors actually do it (5 pillars)

### Pillar 1 — Read what's priced in, don't predict price (Expectations Investing)
Mauboussin & Rappaport's reverse-DCF: instead of forecasting cash flows to get a "fair value," extract the **price-implied expectations** (revenue growth, margins, value-creating years) needed to justify today's price, then judge whether those expectations are too high or low. Returns come from anticipating *revisions in expectations*. This is the single most tool-friendly professional framework.

### Pillar 2 — For cyclicals, cycle stage dominates the multiple
Memory analysts anchor trough valuation to **P/B** (MU troughed ~0.7x in 2011, ~0.85–1x in 2016, ~1x in 2018 — rising floor each cycle) and track **cycle signposts**: supplier inventory days, industry capex/wafer-capacity adds, spot-vs-contract DRAM price spread, HBM wafer crowding-out, hyperscaler capex revisions. Whether the HBM era preserves the old P/B floor is contested (some now use SOTP with premium HBM multiples) — so the tool should present *where in the cycle we are*, not a naive multiple screen.

### Pillar 3 — Pre-committed plans beat in-the-moment decisions
- **Uncertainty-scaled buy bands** (Morningstar architecture): fair-value range ± a band that *widens with uncertainty* — a high-uncertainty name like MU demands a much larger discount before buying than a staple.
- **Tranche ladders:** split planned allocation into 2–4 descending pre-set entries decided *before* the first buy; re-verify the thesis before averaging down.
- **Exits matched to entry type:** price stops (~15%/ATR-based) have evidence *for momentum entries* (Han/Zhou/Zhu 1926–2013); valuation entries need **thesis-milestone exits** (assumption tracker with dated reviews), because fixed stops whipsaw in mean-reverting names.
- **Sizing:** volatility-scaled, capped at ¼–½ Kelly (full Kelly is never used in practice; half-Kelly captures ~75% of growth at ~50% of the volatility).
- **Process alpha:** pre-mortem at entry (Klein/Mauboussin) + decision journal (what you decided, why, how you felt) + 200-day MA as a displayed regime flag (Faber: vol ~30% higher below it).

### Pillar 4 — The catalyst calendar IS the proactive tool
Event-driven desks maintain, for each position: earnings dates + guidance history, conferences/analyst days, lockups, index rebalances, macro dates (FOMC/CPI/elections) — plus sector-specific feeds. For MU: **Samsung/SK Hynix/Kioxia earnings, TSMC monthly revenue (~10th of each month — the closest real-time read on AI capex), TrendForce DRAM/NAND contract-price releases, hyperscaler (MSFT/GOOGL/AMZN/META) capex guidance each earnings season, export-control/China policy (CXMT scaling toward ~350k wafers/month by end-2026 vs. Micron's ~375–385k).** Monitoring = polling a known list on a schedule, with pre-event briefs, not reacting to headlines.

### Pillar 5 — Options decisions are made on scenario grids, not predictions
The professional standard (thinkorswim Risk Profile, OptionStrat): **P/L across price × date × IV**, with greeks, probability of profit AND expected value, expected move from straddle prices vs. the stock's *historical* realized earnings moves, and an explicit post-event IV-crush scenario. tastytrade-style mechanics with study support: enter ~45 DTE, manage at 21 DTE or 50% max profit; buying premium into earnings historically loses (IV crush ~15–45% typical post-event); size by max loss at 1–2% of account per trade, ~25–30% portfolio-wide cap.

---

## 3. Signal scorecard — what the evidence actually says

| Signal | Verdict | Evidence summary |
|---|---|---|
| Twitter/X & StockTwits sentiment | **IGNORE** (as buy signal) | Predictive power lives at minutes-to-hours; fades by the day level. One exception: pre-earnings retail *hype spikes* predict weaker returns — useful only as a contrarian crowding gauge. |
| News-NLP sentiment | **SKIP** (can't exploit) | Real but fast-decaying; needs institutional data (RavenPack). Tetlock: pessimism → pressure then reversion. Use LLM news *triage* for comprehension, not speed alpha. |
| Post-earnings-announcement drift | **DEAD** for MU | Non-existent in large caps since ~2006. Earnings day IS the event; prices react fully near the announcement. |
| Analyst estimate revisions | **BUILD** | Among the best surviving fundamental signals. Track direction + breadth of EPS estimate revisions. Estimate revisions >> recommendation levels (which are dead). |
| Insider buying | **BUILD** (filtered) | Strongest surviving signal: *opportunistic* (non-routine) buys ~82bp/mo abnormal; **cluster buys** (multiple insiders within days) ~3.8% over 21 days. Ignore routine/10b5-1 trades and most selling. |
| Options flow / UOA feeds | **IGNORE** | Edge is short-lived and mostly invisible publicly; publicized UOA trades *reverse* after airing. High volume often = disagreement, not information. |
| Retail crowding (contrarian) | **BUILD** (flag only) | Robinhood herding: top-bought names −3 to −6% over 5 days (small caps mostly). AAII extreme pessimism mildly bullish for the index. Use at extremes as a caution flag. |
| DRAM spot vs. contract price | **BUILD** | Spot leads contract ("contract is the magnet"); spot crossing above contract = classic bullish trigger; TrendForce DXI marketed as a leading indicator of memory stocks. Caveat: spot is ~10% of volume; lead time varies. |
| Hyperscaler capex revisions | **BUILD** | The dominant demand driver (~$700B+ guided for 2026). The *revision direction* each quarter is the signal, not the level. Debt-funded capex + FCF strain = cycle-top warning. |
| Korea semiconductor exports | **BUILD** (confirming) | Fastest-published macro proxy (1st of month + flash prints); Samsung+Hynix ≈ 50% of global memory. Confirming/diverging indicator, not a lead on the stock. |
| 200-day MA regime | **BUILD** (display) | Faber: below the 10-month SMA, returns lower and vol ~30% higher. Regime flag, not a trade signal. |
| Low P/E on a cyclical | **INVERT** | For memory: low P/E at peak margins = warning. The tool should flag "cheap on peak earnings" as risk. |

---

## 4. The analysis framework (6 layers)

**Layer 1 — Business & cycle state.** Quality scorecard (ROIC vs WACC, financial health, moat durability — Morningstar architecture) + memory-cycle dashboard: P/B vs. historical trough band (0.7–1.5x), inventory days (company + industry), industry capex growth, HBM mix %, spot-vs-contract spread, cycle-stage classification (early/mid/late up-cycle, rollover, downcycle, trough).

**Layer 2 — Valuation & expectations.** Reverse DCF: what revenue growth/margins/duration does the current price imply? Compare vs. base/bull/bear cases. Output: fair-value *range* (never a point), with explicit uncertainty rating.

**Layer 3 — Entry/exit plan (pre-committed).** Uncertainty-scaled buy bands → 2–4 tranche ladder with sizes; averaging-down gate (thesis must re-verify); exit rules matched to entry type; volatility-scaled sizing with fractional-Kelly cap; every position carries a pre-mortem + 3–5 tracked assumptions with dated review triggers.

**Layer 4 — Options overlay.** For any contemplated structure: P/L matrix across price × date × per-expiry IV override; greeks now & projected; PoP and EV; expected move (state the convention) vs. historical realized earnings moves; post-event IV-crush toggle; suggested size from max-loss rule. Strategy menu mapped to situations:
- Accumulate lower → cash-secured puts at ladder prices (the wheel if assigned)
- Underwater long → covered calls, collar, or stock-repair spread (buy 1 ATM call, sell 2 OTM calls ≈ zero cost; doubles upside to short strike, lowers breakeven, caps recovery, no downside protection)
- Defined-risk recovery bet → call debit spreads (relatively IV-neutral — matters when post-crash IV is elevated)
- Event volatility → show implied vs. historical move; default stance: do NOT buy premium into earnings (IV crush).

**Layer 5 — Catalyst calendar & monitoring.** Scored event list (probability × expected impact) over a rolling 90 days; pre-event briefs at T-10 and T-2 days; daily poll of: EDGAR 8-K/Form 4 (minutes-level via data.sec.gov), TrendForce press center, TSMC monthly revenue, competitor earnings dates, macro calendar; LLM triage of news into relevant/material/why with a daily digest; quarterly 10-Q diff (the "Lazy Prices" result: language *changes* carry signal).

**Layer 6 — Evidence grading (backtesting with honesty).** Event-study methodology for rules like "buy after X% drop": enumerate ALL historical instances, measure forward *excess* returns vs. SOXX/SPY at multiple horizons, de-cluster overlapping events, benchmark vs. random entry, test above/below 200-dma regimes, cross-validate on peers (WDC, STX, SOXX members). Apply deflated-Sharpe thinking: count every parameter tried; halve the backtest edge for live expectations. **Single-stock statistical reality: ~30–80 non-overlapping drop events in 25 years; ~75 earnings cycles of options history (2007+). Outputs are evidence grades, not proof.** Options backtests additionally need point-in-time chains (expired contracts included), fill modeling at 60–75% of spread width, and acknowledge unmodeled assignment risk.

---

## 5. Tool requirements & architecture

**Outputs (what the tool produces):**
1. **Morning brief** (daily): price/regime state, cycle dashboard deltas, news triage digest, any new filings/insider activity, upcoming 10-day catalyst list.
2. **Pre-event brief** (T-10 and T-2 before each scored catalyst): what's expected, implied move, positioning (IV rank/skew), scenario impacts, recommended pre-event actions from the plan.
3. **Position risk report:** current P/L, distance to tranche/exit levels, assumption-tracker status, options-position greeks and scenario matrix.
4. **Trade ticket generator:** for any contemplated trade — EV, PoP, max loss, suggested size, scenario grid, and the pre-mortem prompt.
5. **Decision journal:** append-only log of every decision with reasoning; reviewed quarterly.

**Architecture (Python, local-first):**
- Ingestion layer (OpenBB as unified fetch layer where convenient) → **point-in-time DuckDB/SQLite store** (snapshot everything on ingest; never overwrite history)
- Engines: cycle dashboard · reverse-DCF/valuation · entry-exit planner · options scenario engine (py_vollib/QuantLib greeks) · catalyst calendar + alerting · LLM layer (Claude API: news triage, transcript summaries, 10-Q diffs, pre-event briefs)
- Backtest module: vectorbt or backtesting.py for equity rules; custom pandas engine over EOD option chains for options rules
- UI: start with generated daily markdown/HTML briefs + a lightweight dashboard; alerts via email/Telegram

**Data stack:**

| Need | Hobbyist (<$100/mo) | Serious ($100–500/mo) |
|---|---|---|
| Prices EOD/intraday | Tiingo Power $30 or Polygon/Massive Starter ~$29 | Polygon Developer ~$79–99 or Alpaca Algo Trader Plus $99 (real-time SIP) |
| Fundamentals, analyst estimates, earnings calendar, transcripts | FMP Starter/Premium $22–59 | FMP Premium + Koyfin Premium ~$79–110 (human screen) |
| Options chains + IV/greeks history | ThetaData Value $40 (4yr history) or Alpha Vantage Premium $50 (daily chains w/ IV, 15+ yrs) | ORATS Delayed API $199 (smoothed IV surfaces to 2007; or one-time $399 historical bulk) + ThetaData Standard $80 |
| Live chains for order decisions | Free via Tradier or Alpaca brokerage account | same |
| Filings, macro | SEC EDGAR + FRED (free) | same |
| **Total** | **≈ $92/mo** (Tiingo + FMP + ThetaData) | **≈ $340–480/mo** |

Notes: yfinance is prototype-only (unofficial scraper, breaks several times a year — cache everything). Polygon.io rebranded to Massive.com (Oct 2025); keys/endpoints unchanged. Skip: Bloomberg/FactSet (cost), NewsAPI Business ($449 for headlines), UOA alert services, backtrader/zipline (unmaintained/wrong fit).

---

## 6. Build plan (phased; expand to stock #2 only after one full earnings cycle on MU)

**Phase 0 — Decision discipline on paper (this week, zero code).**
Write the MU position document: current thesis in 3–5 falsifiable assumptions with confidence levels; pre-mortem ("it's 6 months later and this position failed — why?"); pre-committed action plan (tranche ladder prices for adds, trim/exit triggers, max position size); options-structure menu to evaluate (covered call / collar / repair spread / CSP ladder) with the decision deferred until Phase 4 can model them. This captures 40% of the system's value for free.

**Phase 1 — Data foundation + morning brief (week 1–2).**
Repo scaffolding; DuckDB point-in-time store; ingest: Tiingo/cached-yfinance EOD prices, FMP fundamentals + estimates + earnings calendar, EDGAR submissions (8-K/Form 4/10-Q), FRED macro. Generate the daily MU morning brief (price/regime, estimate-revision tracker, insider activity, filings, next catalysts).

**Phase 2 — Catalyst calendar + proactive alerting (week 2–4).**
Event registry (earnings, Samsung/SK Hynix/Kioxia dates, TSMC monthly ~10th, TrendForce poller, hyperscaler earnings, FOMC/CPI/elections, lockups/rebalances) scored by probability × impact; T-10/T-2 pre-event briefs; EDGAR minutes-level polling for 8-K/Form 4 with push alerts; LLM news triage digest. **This phase solves "I had no idea it was coming."**

**Phase 3 — Valuation, cycle & entry/exit engine (week 4–6).**
Reverse-DCF module; memory-cycle dashboard (P/B band, spot-vs-contract, inventory days, capex, HBM mix, hyperscaler capex revisions, Korea exports); uncertainty-scaled fair-value band; tranche-ladder generator; sizing calculator (vol-scaled, Kelly-capped); assumption tracker with scheduled reviews.

**Phase 4 — Options scenario engine (week 6–9).**
Chain ingestion (ThetaData/Alpha Vantage + free live via Tradier); P/L matrix price × date × IV with per-expiry overrides; expected-move vs. historical-earnings-move comparison; IV-crush scenario toggle; EV + PoP + max-loss sizing on every ticket; strategy comparison report for the live MU position (hold vs. covered call vs. collar vs. repair spread vs. CSP ladder for adds).

**Phase 5 — Evidence grading / backtests (week 9–12).**
Event-study runner with guardrails (excess-vs-SOXX, de-clustering, random-entry baseline, regime splits, peer cross-validation, trial counting + deflated-Sharpe report); options-rule backtests on EOD chains with realistic fills; grade every rule the tool uses (A/B/C evidence).

**Phase 6 — Harden & expand.** Run the full loop through one MU earnings cycle (Dec 2026 report), journal everything, then add stock #2.

---

## 7. MU snapshot the tool would show today (Nov 6, 2026)

- Price $656 (Nov 5 close) · −46% from June peak $1,213 · cost basis $900+ → −27% · beta 2.4 · below 200-dma territory after a 2-day −23%.
- Cycle tells currently MIXED: TrendForce 4Q26 contract prices still *rising* (bullish); HBM4 sold out through 2026, >75% of FY27 HBM reportedly committed at higher prices (bullish); Kioxia cautious guide + CXMT capacity scaling + post-midterm AI-regulation risk + debt-financed capex scrutiny (bearish). Classic late-cycle ambiguity.
- Valuation optics: trailing P/E ~8.8x, forward ~3.7x (lowest among US chips) — the tool would flag this as **"cheap on peak earnings" — a cycle warning, not a value signal.** GuruFocus GF-value style estimates sit ~$824 vs $656; analyst averages $1,400–1,560 largely pre-date the crash.
- Catalyst list: TSMC October revenue ~Nov 10 · Samsung/SK Hynix results · TrendForce 1Q27 price forecast (date unannounced — poll) · **MU FQ1-27 earnings mid-to-late Dec (vendors conflict: Dec 15/16/23 — confirm on IR)** · hyperscaler Q4 capex guides late Jan · AI-regulation legislative calendar.
- Options context: IV elevated post-crash → structurally favors premium-selling/financed structures (covered calls, collars, CSPs at ladder prices) over buying calls; repair spread is the canonical "underwater long" structure to model in Phase 4.
- Unverified figures to confirm before relying on them: FQ1-27 guidance ($61.5B rev / $38.15 EPS per one Yahoo summary — looks anomalously large), current P/B, exact earnings date.

---

## 8. Honest limitations

- Single-stock backtests are low-power; every rule gets an evidence grade, not a verdict.
- Earnings-day moves will remain partly unpredictable; the tool's job is to ensure they're never *unanticipated* and always pre-sized.
- Sentiment/flow feeds are deliberately excluded as buy signals — evidence says they don't pay at retail horizons.
- Several 2026 figures above came from secondary aggregators during research; items flagged "verify" need confirmation against primary sources (Micron IR, TrendForce) in Phase 1.

## 9. Key sources (abridged)

Mauboussin & Rappaport, *Expectations Investing*; Morningstar Equity Research Methodology; Cohen, Malloy & Pomorski (insider trading, NBER w16454); Martineau "Rest in Peace PEAD"; Barber, Huang, Odean & Schwarz (Robinhood herding); Tetlock (JF 2007); Han/Zhou/Zhu + Kaminski & Lo (stop-losses); Faber (2007) 10-month SMA; Bailey & López de Prado (Deflated Sharpe); S&P Global "Buying the Dip"; CBOE PUT/BXM studies + Bondarenko (2016); tastylive strangle-management studies; Morgan Stanley "Winter" memory-cycle series; TrendForce memory bulletins (2026); Trefis/GuruFocus/Motley Fool/CNN/AP (Nov 2026 MU crash coverage); OpenBB/ThetaData/ORATS/FMP/Tiingo documentation and pricing pages. Full source lists live in the three research-agent reports from the 2026-11-06 session.
