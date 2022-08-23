# RTG---Trading-Algorithm 

This algorithm was implemented in line with Optiver's 'Ready Trader Go' competition where students were tasked with building a autotrader that ran in a simulated exchange.

This autotrader implements the 'Ichimoku Cloud' strategy implementing four indicators of behaviour of the market simulation:
1. Kijun-sen ([highest high + lowest low]/2 for the last 26 records)
2. Tenkan-sen ([highest high + lowest low]/2 for the last 9 records)
3. Senkou (span A [(Tenkan-sen + Kijun-sen)/2] and span B [(highest high + lowest low)/2] for the last 52 records)
4. Chikou (price compared to the price 26 records ago)

The autotrader behaves as follows:
Buy:
- Whenever the Tenkan-sen crosses the Kijun-sen from below to above while the market price is above the Ichimoku cloud.
- And finally, the Chikou span’s last value must be higher than the corresponding market price in the same point in time.

Sell:
- Whenever the Tenkan-sen crosses the Kijun-sen from above to below while the market price is below the Ichimoku cloud.
- And finally, the Chikou span’s last value must be lower than the corresponding market price in the same point in time.

Additional indicators were considered:
- If current prices are above kijun, this signals an oncoming increase in price
- If current prices are below kijun, this signals an oncoming decreasing in price

- If current prices cross tekan from below, this signals price increase
- If current prices cross tenkan from above, this signals a price decrease

- If span A > span B, this signals a price increase
- If span A < span B, this signals a price decrease

- When Chikou-span increases above the current price, this signals a price increase.
- When Chikou-span decreases below the current price, this signals a price decrease.

- Steeper angles = confirmation of trends
- Volatility is shown by larger clouds (difference between span A and span B), which also signals a trend reversal
