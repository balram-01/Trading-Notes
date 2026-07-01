# 🎯 Master Strategy & Backtesting Checklist

_Synthesized from Trading-Notes (ICT / Smart Money Concepts framework) — full pass through all lessons_

---

## 1. The Strategy in One Line

> Trade **with** HTF bias, from a **validated premium/discount POI**, only **after** a liquidity sweep + structure shift, during your **kill zone**, with **≥1:2 RR**, using **fixed risk** — or don't trade.

---

## 2. Pre-Trade Checklist (run this before every backtest entry)

### A. Bias (Top-Down, start on H4)

- [ ] HTF (4H/1H) trend marked: HH/HL (bullish) or LH/LL (bearish)
- [ ] LTF trend aligned with HTF — no counter-trend trades while learning
- [ ] **Daily Bias written as one sentence**: _"Today's bias is ___ because ___."_
- [ ] **Invalidation written down**: _"If ___ happens, my bias is wrong."_ (a wick doesn't count — needs a confirmed candle close beyond the level)
- [ ] PDH/PDL, Equal Highs/Lows marked as liquidity reference points

### B. Range & Zone

- [ ] Latest swing high → swing low (or reverse) marked
- [ ] Fib 0–0.5–1 applied → Premium (>50%, look for shorts) / Discount (<50%, look for longs)
- [ ] POI identified inside the correct zone — and it passes its validity test (see §3a)
- [ ] POI is close to the range extreme (stronger) — not mid-range, not sitting in Equilibrium (~50%, chop zone)

### C. Confirmation (never skip)

- [ ] Liquidity swept first (prior high/low, equal highs/lows) — **a sweep alone is not a reversal signal**, it only means orders were collected
- [ ] Not mistaking an **Inducement** (a fake early move designed to trap retail before the real move) for the real signal — wait for the follow-through
- [ ] Market Structure Shift confirmed _after_ the sweep (break of last HL for bearish shift, break of last LH for bullish shift)
- [ ] Entry model chosen: **Aggressive** (right after sweep+shift) or **Conservative** (wait for retrace into the new OB/zone)

### D. Timing (IST)

|Kill Zone|IST Time|Notes|Best Pairs|
|---|---|---|---|
|Asia|5:30 AM – 9:30 AM|Range-bound, sets up the Asia sweep|AUD, NZD, JPY|
|London|11:30 AM – 2:30 PM|Highest quality trends|EUR, GBP|
|New York|4:30 PM – 7:30 PM|High volatility, news-driven|USD pairs, XAUUSD|
|London Close|7:30 PM – 9:30 PM|Lower volume, smaller moves|Majors|

- [ ] Price at POI _during_ your chosen Kill Zone — pick **one** session and master it
- [ ] Not within 15 min before/after high-impact news (CPI, NFP, FOMC, rate decisions)
- [ ] Not Monday open / Friday close / last trading day of month / December, unless truly A+
- [ ] If trading the Asia→London handoff: watch for a sweep of the Asia High/Low as fuel for the London move

### E. Risk & Exit (define BEFORE entry)

- [ ] Stop Loss beyond protected high/low or beyond the POI + a few pips buffer (never on the exact level)
- [ ] SL genuinely invalidates the trade idea (not just "hope it survives")
- [ ] Take Profit = next logical structure (opposing zone / liquidity pool / swing point / PDH-PDL) on the **same timeframe as entry**
- [ ] RR calculated: minimum **1:2**, 1:3 is good, 1:4+ excellent
- [ ] Position size = fixed risk **0.5–1% of account**, no exceptions

### F. Final Gate

- [ ] **Every** box above is checked → Take the trade
- [ ] **Any** box unchecked → No trade, log why and move on

---

## 3. Entry Execution Models

|Model|When|Risk/Reward profile|
|---|---|---|
|**Aggressive**|Right after liquidity sweep + structure shift|Higher reward, higher risk|
|**Conservative**|Wait for retrace into OB/zone formed by the shift|Lower risk, higher confirmation|

---

## 3a. POI Validity Cheat Sheet (use whenever marking a zone)

Not every marked box on your chart is a real POI. Each type has its own pass/fail test:

**Supply / Demand Zone**

- [ ] Formed by a genuine imbalance — strong impulsive move away from the origin
- [ ] Drawn correctly: Range Method (whole consolidation, bigger zone, higher hit-rate) OR Pivot Method (single origin candle, tighter, better RR)
- [ ] Check mitigation status: zone counts as **mitigated once price reaches ≥50% into it** — unmitigated zones are stronger

**Order Block** (a stricter, higher-precision subtype of Supply/Demand)

- [ ] Creates a Fair Value Gap — no FVG = not a valid Order Block, just a regular zone
- [ ] Strong displacement away from it (sharp, V-shaped move)
- [ ] Is the **last opposing candle** before the impulsive move (last bearish candle before a bullish move, or vice versa)
- [ ] Leads to a Break of Structure

**Fair Value Gap (FVG)**

- [ ] Confirmed 3-candle formation with an actual visible gap between candle 1's wick and candle 3's wick — momentum alone without a gap does **not** count
- [ ] Located in the correct Premium/Discount zone for the trade direction

**Flip Zone**

- [ ] Failed Reaction — the original zone failed to do its job (Demand failed to make new HH, or Supply failed to make new LL)
- [ ] Break of Structure occurred after the failure
- [ ] Candle **body** closed beyond the structural level — a wick alone doesn't count
- [ ] Direction: Demand fails → Supply Flip Zone → bias turns bearish; Supply fails → Demand Flip Zone → bias turns bullish
- [ ] HTF zones override LTF Flip Zones — check the higher timeframe narrative first
- [ ] Still needs normal entry confirmation (sweep + MSS) once price returns to mitigate it

If a POI fails its test → it's noise, not a zone. Don't trade it.

---

## 3b. Trade Management (choose one style per plan, decide before entering)

|Style|Rule|
|---|---|
|**Set & Forget**|No SL moves, no partials, let the original plan play out fully|
|**Active Management**|Move SL to break-even after +1R; take 50% profit at +2R; trail remainder below Higher Lows / above Lower Highs|

Pick one per your trading plan and stay consistent across your backtest sample — don't switch mid-series or you can't isolate what's actually working.

---

## 4. Post-Trade / Journal (log every backtested trade)

For each trade record:

- Screenshots: HTF (bias) + MTF (POI) + LTF (entry trigger)
- Setup type (which POI, which model), 2–5 entry confluences
- HTF bias / session / news proximity
- Entry, SL, TP, RR planned vs. RR achieved
- Result (win/loss/BE) in R-multiples
- Trade management used (set & forget / BE / partial / trailing)
- Did I follow the checklist? (Y/N — if N, note which rule broke)
- Emotion before entry / after exit
- **Good Loss or Bad Loss?** Good = followed plan, correct setup, market just didn't cooperate (accept it). Bad = broke a rule, emotional decision (preventable — this is what needs fixing)
- One-line lesson, phrased as an action not a feeling (not _"I'll do better"_ — instead _"Wait for liquidity sweep before entering"_)

**Track in aggregate (weekly):**

- Win rate, Average R-multiple, Profit factor
- **Compliance Score** = (Trades following the plan ÷ Total trades) × 100 — track this alongside win rate; a profitable trade that broke rules is still a bad trade, and a losing trade that followed the plan is still a good one
- Edge score by setup type (which POI/model performs best)

**Guardrail violation log** — every time a rule breaks, record: which rule → why (revenge/greed/boredom/fear) → the specific prevention you'll put in place. ⚠️ Watch for the trap of breaking a rule and still winning — that teaches your brain "breaking rules works" and builds a bad habit that costs you later. Never let an outcome excuse a process failure.

---

## 5. When to Skip / Stop (built-in circuit breakers)

**Skip the setup if:**

- Price is in "middle of nowhere" (no POI reaction) or sitting in Equilibrium (~50% of range)
- Market is choppy/sideways with no clear structure
- Bias not aligned across timeframes
- Outside kill zone or near news
- RR < 1:2
- POI hasn't passed its validity test (§3a)

**Stop trading entirely (even in backtest, note it) if:**

- 5–10 consecutive losses → pause, review journal for rule violations, refine plan before continuing
- You're compromised: stressed, tired, emotional, revenge-trading impulse present

**Emotional Playbook** — recognize the trigger, apply the fixed response, don't improvise:

|Emotion|What it's protecting you from|Fixed response|
|---|---|---|
|Fear (hesitating on a valid setup)|Being wrong|Pre-written If–Then rule: if conditions met → execute, no debate|
|Greed (holding too long, oversizing)|Missing extra profit|Set max daily profit target / trade count _before_ the session; stop when hit|
|FOMO (chasing a move already running)|Missing an opportunity|Abundance mindset — if you weren't prepared, it wasn't your trade; wait for the next one|
|Hope (staying in a loser)|Admitting you're wrong|SL is defined before entry and never moved further away — it's the cost of doing business|
|Revenge (trying to win it back immediately)|Accepting the loss|10-minute rule: step away after every loss before considering the next trade|
|Doubt (second-guessing a valid setup)|— (comes from under-repetition, not logic)|Build evidence through backtesting/journaling; competence creates confidence, not positive thinking|

---

## 6. Key Principles to Hold Yourself To

- **No checklist → No trade.** The checklist decides, not emotion.
- **Waiting is a position.** Missing a trade is never a loss; breaking a rule is.
- **Entries are cheap, exits are the edge.** Plan SL/TP before entry, not after.
- **Fixed risk always** — never scale up size to "recover" or because you feel confident.
- **Process over prediction.** Grade yourself on rule-following (Compliance Score), not on individual trade outcomes.
- **You trade your beliefs, not the market.** Outcome-based beliefs ("I need to make money today") create pressure and forced trades. Identity-based beliefs ("I am the type of trader who follows my process") create consistency. Reinforce the identity daily.

---

## 7. Daily/Weekly Reflection Ritual

**End of every backtest session, ask:**

1. Did I follow my trading plan, or trade on emotion?
2. Did I break any rules? Which ones, and why?
3. Was my execution clean (entry quality, exit quality, patience, timing)?
4. Did I do the "boring work" (markups, journaling, review) — or skip it?

**Then review your best and worst trade of the session:**

- Best trade → what created the win, what did I do right, how do I repeat it (repeat behavior, not profit)?
- Worst trade → root cause, Good Loss or Bad Loss, and one specific improvement for next time

**Close with one sentence:** _"Next session I will ___."_ (one focus at a time — small, compounding improvements, not vague resolutions)

---

## 8. Suggested Backtesting Workflow

1. Pick one pair + one session (e.g., EUR/USD, London KZ) — don't backtest everything at once.
2. Scroll back to a random historical date, mark HTF structure blind (don't peek forward).
3. Run the full pre-trade checklist bar-by-bar as if trading live, including the POI validity test.
4. Log every valid A+ setup found — taken or skipped — and every rule violation you _would_ have made.
5. After 50–100 samples, compute win rate / avg R / profit factor / compliance score from the journal.
6. Run the weekly reflection ritual (§7) on the aggregated results, not just individual trades.
7. Adjust one variable at a time (e.g., kill zone, RR minimum, entry model, trade management style) and re-test — don't change multiple rules simultaneously or you won't know what worked.