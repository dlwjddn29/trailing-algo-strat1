# Trailing-algo-strat1: Momentum 
Automating how I want to trade/invest in stocks for my own portfolio for more emotionless decisions. 
### W Brain W ChatGPT ^_^ 

{S&P 500 Mid-Cap} Trailing Stop Strategy
==============================================================

Universe Selection
------------------
1. Select companies ranked 100th–119th by market capitalization in the S&P 500.
2. Re-rank and update the universe monthly.
3. Optional filters:
   - Exclude high-volatility stocks (prefer lower 6-month volatility).
   - Optionally, prioritize positive 6-month momentum or stable earnings.

Portfolio Allocation
--------------------
4. Allocate capital equally among selected stocks.
   - Example: $100,000 ÷ 20 = $5,000 per stock.
5. Cash from stopped-out positions remains idle (no re-entry until next rebalance).

Entry Rules
------------
6. Buy each selected stock at market open on the rebalance day.
7. (Optional) Adjust position sizes by volatility — smaller for high-vol stocks.

Stop-Loss & Trailing Rules
--------------------------
8. Initial stop-loss: 7% below entry price.
9. Dynamic trailing stop:
   - When price ≥ +3% from entry → move stop to 4% below current price.
   - For each additional +1% gain → recalc stop = 4% below current price.
   - Alternatively, use volatility-adjusted trailing stop (e.g., 2×ATR below price).
10. Update stop-loss levels daily (or intraday if using real-time data).

Exit Rules
----------
11. If price hits stop-loss → sell immediately and mark position as exited.
12. Do not re-enter exited stocks until next monthly rebalance.
13. Open positions remain active (Good-til-cancelled) until stop triggers or rebalance.

Risk Management (Optional Enhancements)
---------------------------------------
14. Cap max portfolio drawdown (e.g., 10–15%) — move all to cash if breached.
15. Limit max sector exposure (e.g., ≤25% in any sector).
16. Track slippage and transaction costs for realistic backtesting.

Rebalancing
------------
17. Rebalance monthly to refresh the 100–119 universe and reallocate idle cash.
18. Update all open positions’ stop-loss levels and portfolio weights at rebalance.
