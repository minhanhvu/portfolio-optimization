# 🧬Portfolio Optimization

### 🪶Context
Imagine after spending years pursuing 2 Economics degrees, you finally come to a point of "This is it! Enough preaching, I am ready to put my life at risk". Armed with the modest savings the internship in Berlin, you open a micro business. Now you find yourself in a pickle, trying to figure out where to wisely allocate your hard-earned money. You reside in a sunny beach city, so selling icecream seems tempting. But like every fresh broke graduate, you worry about your loss of income on the rainy days, so why not add umbrella stocks for extra security? But how much should you invest in icecream as opposed to umbrellas so that the return can at least afford your rent and some extra coffee for your dates. And if you are confident in your business discernment 

Portfolio optimization in financial investment is process that answer similar questions as above, how to best allocate your assets given a set of constraints (


While the focus of portfolio optimization is to find the best allocation given a set of constraints, what may be considered the best portfolio can go beyond traditional risk-return tradeoffs. Quantitative researchers and portfolio managers might also want to add diversification techniques, perform an optimization that minimizes tracking error, or find a portfolio that equalizes the risk contribution of the assets in the portfolio.
### Process


###


### Key learnings

### 💡Findings
__1. Time series analysis__
>The rates of return of XVZ were negatively corelated to EXX5.DE and IUS3.DE and the negativity were three times intensified during the pandemic period.

<img align="right" width="100%" height="100%" src="https://github.com/minhanhvu/portfolio-optimization/assets/87383756/221381c8-bcaa-413c-b1ce-578106004762">

This is explained by the opposite reactions to market uncertainty of the underlying volatility index and stock index. Amid the world economic shutdown, the CBOE Volatility Index rose sharply in March 2020, reflecting the burgeoning demand for options to hedge risk, as opposed to the fall of Down Joins and S&P index, manifested investors’ pessimistic view in future economy.


> There was a serial correlation in price changes for the sub-period before Covid-19.

Efficient market hypothesis states that stock prices follow a random walk. In other words, the price changes in one period will be independent of changes in the next. Therefore, we cannot forecast future returns based on the past since autocorrelations at all lags are zero. 

This hypothesis is rejected for the coefficients of the first lagged price-change ∆<sub>t-1</sub> on current price change ∆<sub>t</sub> were found significant at 95% for all three assets, after netting out the effect of other lagged changes and past residuals

__2. Optimal portfolio__

The tangent portfolio is identified by using the yield of US 3-month T-bill as risk-free rate 0.05%. The tangent portfolio comprises 0% EXX5.DE, 60% IUS3.DE and 40% XVZ, with an expected return of 15.4% and 20.2% volatility. Minimum variance portfolio comprises 60.3% EXX5.DE, 11.5% IUS3.DE, and 28.3% XVZ, with an expected return of 11.2% and 17.7% volatility.

Nevertheless, identifying optimal portfolio by maximizing Sharpe ratio is only valid if asset returns are normally distributed. The Shapiro-Wilk test for the log returns of our assets reveals that the return rates do not follow normal distribution. Here I suggest Roy’s Safety-First criterion as one of the alternatives that do not require a statistical distribution. Roy’s Safety-First criterion suggests that investors will choose the optimal portfolio that minimizing the probability which portfolio’s return fall below a safety rate called floor return (Francis & Kim, 2013)

<p align="center">
Minimize Prob (r<sub>P</sub>< r<sub>floor</sub>)
</p>


If the portfolio returns follow normal distribution, and the risk-free rate is taken as the floor return, minimizing the probability of underperform the safety rate is equivalent to maximize Sharpe ratio. 


