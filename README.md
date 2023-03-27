# Pair-Trading-Algorithm
Gives pairs to trade EOD

This algorithm identifies stationary pairs for end-of-day trading. It imports data for the last 200 days, which is approximately 137 trading days. It checks for 98C97 pairs, i.e., 9,506 pairs in total. If the ratio is found to be stationary, it looks for pairs that are more than 2.5 standard deviations away from the mean.

The stationarity test used here is the Augmented Dickey-Fuller (ADF) test. The algorithm looks for pairs with a p-value equal to or less than 0.05. If this condition is met, we buy/sell the pair and hold it until the ratio drops to 1 standard deviation or goes to 3 standard deviations, at which point we cuts our losses.


This algorithm was backtested from 2021-12-1:

| Number of Trades  | 40 |
| ------------- | ------------- |
| Winners  | 22  |
| Losers | 18  |


Google Sheet with list of trades:
https://docs.google.com/spreadsheets/d/1BBCJHp44MGGH2PgFx3vRA63sjMSCglosOiS7CyjJrWY/edit#gid=0
