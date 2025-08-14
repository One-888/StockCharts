# Trading Strategy Overview

This trading strategy leverages stockcharts.com for comprehensive market analysis. The strategy is designed to address two pivotal questions: the optimal timing for purchasing stocks and the appropriate purchase price.

## Step 1: Initial Scan
An initial scan of the S&P 500 is conducted to identify volume spikes that are at least 1.25 times the volume of the previous period (weekly or monthly). This scan generates a list of potential stocks for acquisition.

Utilizing weekly or monthly data mitigates the noise associated with rapid daily volume fluctuations, thereby providing a clearer indication of significant volume spikes. The default setting is on a monthly basis, which smooths out short-term volatility and highlights more substantial trends.

### Scan Code
```
///////////// Monthly ///////////////////////
[group is SP500]
and [2 months ago Monthly Volume * 1.55 < 1 month ago Monthly Volume]  // Volume up 55%

///////////// Weekly ////////////////////////
[group is SP500]
and [2 weeks ago Weekly Volume * 1.55 < 1 week ago Weekly Volume]  // Volume up 5% last week
```

## Step 2: Position Opening

In the Thinkorswim web application, a conditional order is executed at or above the mark price when it reaches the peak price. The mark price is set within a range of 2-5% from the Volume by Price (VOP) peak. The focus is on stocks that are in an uptrend. The 2-5% range is used to confirm momentum in the stock, thereby avoiding the risk of market exhaustion and potential investor exit.

**Tip**: The strategy aims to purchase stocks when the current price is below the peak VOP, providing room for upward movement. If an entry is not made at this time, there are plenty of other stocks to choose from. Avoid falling into the trap of FOMO (Fear of Missing Out).

## Exit Strategy

The strategy adheres to a risk management rule of never risking more than 7% of the investment. A trailing stop order is set by default at 3%. For high-risk stocks, such as PLTR, the trailing stop is set at 3%, while for stocks like the Magnificent Seven, it is set at 4%.

## Additional Notes

The strategy does not place significant emphasis on moving averages (MA) since past performance cannot predict future outcomes. For example, if a dice is tossed three times and the numbers 6, 6, and 6 are obtained, the probability of getting another 6 on the fourth toss is the same as getting any other random number, such as 2, 3, or 5. This illustrates that past results do not influence future probabilities.

**Tip**: The strategy avoids purchasing large quantities of cheap or poor-quality stocks. It is preferable to hold on to cash. Warren Buffet serves as an exemplary model in this regard. Think of investing like fishing: set up the correct bait and check the weather. It might take a few days to catch any fish. Investing is inherently boring. For excitement, consider visiting a casino.
