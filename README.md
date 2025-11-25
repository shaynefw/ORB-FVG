# ORB-FVG STRATEGY
## 1-Minute NQ Futures Day Trading System

---

## TOOLS REQUIRED

- Chart Timeframe: 1-Minute
- [ORB Indicator](https://www.tradingview.com/script/uJsja4dX-ORB-Opening-Range-Breakout/)
  - Settings: ORB total time = 5min, Session Time = NY open first 5 minutes
- [FVG Indicator](https://www.tradingview.com/script/jWY4Uiez-Fair-Value-Gap-LuxAlgo/)
- [Trim Calculator](https://docs.google.com/spreadsheets/d/1-H46rJP_invFPwYxf4mOFRkO-fWFtciJfmAgRy6On9U/edit?usp=sharing)
- [NQ Position Size Indicator](https://www.tradingview.com/script/pr4yuvXG-NQ-Position-Size-and-Risk-Reward-Calculator-V2/)
   - Settings: Disable "Show Distance Lines" (Optional but recommended)

---

## ENTRY CRITERIA

1. Price must CLOSE outside the 5-minute ORB range
   - LONG: Close above ORB high
   - SHORT: Close below ORB low

2. Fair Value Gap (FVG) must form in the breakout direction
   - Use LuxAlgo FVG indicator to detect

3. Wait for the FVG candle to complete

4. ENTER on the CLOSE of the confirmation candle
   - Confirmation candle = the candle immediately after the FVG candle

---

## STOP LOSS PLACEMENT

- LONG: Stop at the LOW of the candle BEFORE the FVG candle
- SHORT: Stop at the HIGH of the candle BEFORE the FVG candle

---

## PROFIT TAKING (TRIM SCHEDULE)

Target    | Action                          | After Trim
----------|--------------------------------|------------------
1.5R      | Trim 60% of position           | Move stop to BREAKEVEN
2R        | Trim 50% of remaining          | Stay at breakeven or Trail
3R        | Trim 50% of remaining          | Stay at breakeven or Trail
4R        | Trim 50% of remaining          | Stay at breakeven or Trail
5R        | Close remaining or trail stop  | Done

Use the Trim Calculator spreadsheet to determine exact contract numbers.

---

## EXAMPLE (10 Contracts)

- Entry: 10 contracts
- At 1.5R: Sell 6 → Move stop to BE → Remaining: 4
- At 2R: Sell 2 → Remaining: 2
- At 3R: Sell 1 → Remaining: 1
- At 4R: Sell 1 or hold → Remaining: 0-1
- At 5R: Close any remaining

---

## DAILY RULES

- Maximum 2 trades per day
- If Trade 1 wins: DONE for the day
- If Trade 1 is BE or loss: Take Trade 2, then DONE regardless of outcome

---

## QUICK CHECKLIST

[ ] Price closed outside 5-min ORB range
[ ] FVG formed in breakout direction
[ ] FVG candle completed
[ ] Entered on close of confirmation candle
[ ] Stop placed at high/low of candle BEFORE FVG
[ ] First trim at 1.5R → Stop moved to breakeven
[ ] Continue trimming per schedule
[ ] Max 2 trades today

---
