# Trading Strategy Overview

This trading strategy utilizes stockcharts.com for market analysis. The strategy is designed to answer two critical questions: when to buy and at what price to buy.

## Step 1: Initial Scan
We perform an initial scan of the S&P 500 to identify volume spikes of at least 1.25 times the previous period (weekly or monthly). This scan generates a list of potential stocks for purchase.

## Step 2: Position Opening

In the Thinkorswim web application, we execute a conditional order at or above the mark price when it reaches the peak price. The mark price is set within a range of $2 - 5% from the Volume by Price (VOP) peak. Our focus is on stocks that are in an uptrend. We wait for the 2-5% range to confirm momentum in the stock, avoiding the risk of market exhaustion and potential investor exit.

**Tip**: We aim to purchase stocks when the current price is below the peak VOP, providing room for upward movement. If we do not enter this time, we have plenty of other stocks to choose from. Do not fall into the trap of FOMO (Fear of Missing Out).

## Exit Strategy

We adhere to a risk management rule of never risking more than 7% of the investment. A trailing stop order is set by default at 3%. For high-risk stocks, such as PLTR, the trailing stop is set at 3%, while for stocks like the Magnificent Seven, it is set at 4%.

## Additional Notes

We do not place much emphasis on moving averages (MA) since past performance cannot predict future outcomes. For example, if you toss a dice three times and get the numbers 6, 6, and 6, the probability of getting another 6 on the fourth toss is the same as getting any other random number, such as 2, 3, or 5. This illustrates that past results do not influence future probabilities.

**Tip**: We do not want to buy large quantities of cheap or poor-quality stocks. It is better to hold on to cash. Look at Warren Buffet as an example. Think of investing like fishing: you set up the correct bait and check the weather. You might not catch any fish for a few days. Investing is boring. If you want something exciting, go to a casino.
