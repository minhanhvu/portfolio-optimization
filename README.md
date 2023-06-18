# 🧬Portfolio Optimization

### 🍧 Context
Portfolio optimization is a process of selecting the portfolio that generates the highest possible return given a specific risk level.

Imagine after spending years pursuing 2 Economics degrees, you are finally ready to take some risks and open a micro business of your own with the modest savings you made from your student life. Now you find yourself in a pickle, trying to figure out where to wisely allocate your hard-earned money. You reside in a sunny beach city, so selling ice cream seems tempting. But like every fresh broke graduate, you worry about your loss of income on the rainy days, so why not add umbrella stocks for extra security? Your research shows that while umbrellas promise greater profits, ice cream offers a steadier stream of revenue. Now, a question arises: how much should you invest in ice cream compared to umbrellas so that the monthly return of the entire business at least affords a family vacation twice a year in Maldives while keeping the income fluctuations at minimum.

<p align="center">
  <img src="https://github.com/minhanhvu/portfolio-optimization/assets/87383756/0a46de22-8eb4-43d4-87c2-409155df6492" alt="Description of the GIF">
</p>

Portfolio optimization in financial investment addresses similar questions. Given investor’s risk tolerance, what type of assets should the manager invest in, what is the suitable combination of assets and how much weight should be assigned to each asset so that the portfolio yields the highest possible return. This project focuses on answering the last question by following Modern Portfolio Theory, assumed that the investor has already decided on her assets.

Portfolio includes 2 stock indexes and 1 volatility index. A total of 716 observations for each asset (equivalent to 3 years timeframe) are collected.
- __EXX5.DE__: Dow Jones U.S. Select Dividend Index
- __XVZ__: S&P 500® Dynamic VIX Futures TM Total Return Index
- __IUS3.DE__: S&P Small Cap 600

Specifically, the project will
- Find the minimum-variance portfolio using Monte-Carlo simulation
- Identify tangent portfolio by maximizing Sharpe ratio 
- Validate the assumptions of Modern Portfolio Theory (MPT) on the asset's pricing data
- Suggest alternative optimization approach to MPT

### ❄️ Process
__1. Data preparation__
* Import adjusted closing prices.
* Drop N/A values and convert prices into EUR 
> Library: `yfinance`, `pandas`


__2. Time Series Analysis__
* Depict and analyse price movement
* Calculate average returns and volatilities
* Analyse the correlation between assets
* Visualize return distributions and test their normality
> Library: `matplotlib.pyplot`, `numpy`, `seaborn`


__3. Portfolio Optimization__ 
- Calculate portfolio average return and volatility
- Plot efficient frontier using Monte-carlo simulation
    - Identify minimum variance portfolio using optimization function
    - Identify tangent portfolio by maximizing Sharpe Ratio
> Library: `scipy.optimize`, `scipy.interpolate`
### 👻 Findings
__1. The rates of return of XVZ were negatively correlated to that of EXX5.DE and IUS3.DE__

<p align="center">
<img src="https://github.com/minhanhvu/portfolio-optimization/assets/87383756/121ed7bd-8a74-4d8b-bdb7-a9cbc4d28a5a" width=80% height=80%>
</p>

This is well-explained by the opposite reactions to market uncertainty of the underlying volatility index and stock index. Amid the world economic shutdown, the CBOE Volatility Index rose sharply in March 2020, reflecting the burgeoning demand for options to hedge risk, as opposed to the fall of Down Joins and S&P index, manifested investors’ pessimistic view in future economy.

__2. The efficient market hypothesis did not hold for the examined period__

The efficient market hypothesis (B. Malkiel, 2003) states that in a competitive market, stock prices follow a random walk. In other words, the price changes in one period will be independent of changes in the next. Autocorrelations of returns at all lags are zero.
However, the coefficients of the first lagged price-change (∆_(t-1)) on current price change (∆_t) were found significant at 95% for all three assets, after netting out the effect of other lagged changes and past residuals. Hence, the null hypothesis of zero-correlation between the current price and past prices is rejected. Therefore, we conclude that the efficient market hypothesis did not hold for the examined period. _Test details can be checked at the ARIMA model session in the Jupyter file_

__3. The minimum-variance portfolio__

<p align="center">
<img src="https://github.com/minhanhvu/portfolio-optimization/assets/87383756/eddcd647-28bc-4305-bf5c-7794cff4a5a1" width=80% height=80%>
</p>

The efficient frontier is the set of optimal portfolios that offer the highest expected return for a defined level of risk or the lowest risk for a given level of expected return. The minimum variance portfolio comprises 60.3% EXX5.DE, 11.5% IUS3.DE, and 28.3% XVZ, with an expected return of 11.2% and 17.7% volatility

__4. The tangent portfolio__

<p align="center">
<img src="https://github.com/minhanhvu/portfolio-optimization/assets/87383756/08a972e0-ef1a-477c-bb73-1341164826d5" width=80% height=80%>
</p>

Incorporating risk-free asset in the investment, the tangent portfolio is a portfolio that maximizes the excess return per risk unit, which is also referred to as the Sharpe ratio
The tangent portfolio is identified by using the yield of US 3-month T-bill as risk-free rate 0.05%, comprising of 0% EXX5.DE, 60% IUS3.DE and 40% XVZ, with an expected return of 15.4% and 20.2% volatility

**Bits of discussion**
The Mean-variance portfolio theory implies fixed and predictable returns and volatility of element assets. It also assumes a stable correlation between assets return, and also the normal distribution of return rates. In this case, I found the violations of these assumptions in our assets. 

1. Rates of returns are not normally distributed 
2. Correlation between asset returns can vary through time 
3. Average return and volatility of elements assets are not constant over time

Hence, it's recommended to find an alternative approach that does not require a specific distribution function (Roy's Safety-First Criterion)

### 💡Key learnings
This project is one of the most challenging projects that I have done, concerning the tremendous time to understand Portfolio Theory and learning the optimization tools with Python's `scipy` library. 
However, I found that the concept of diversification and Monte-Carlo methods are incredibly useful in business forecast activities. Diversification brings to our attention the impact of product sales correlation on our revenue when we were to a new product to our business. Meanwhile, Monte-Carlo methods is a great tool to understand possible revenue outcomes given there are random factors in our model. 


- **Statistics**: Gaussian distribution, correlations, stationary property testing
- **Modeling**: ARIMA predictive model for time series data
- **Optimization**: Mean-variance technique using Monte-Carlo simulation
  
Programing language: Python
- **Data visualization** with `matplotlib`,`seaborn`
- **Data cleaning** and analysis with `pandas`,`numpy`, 
- **Modelling** with `scipy`

### Reference & Appreciation
* Hilpisch, Yves. (2018): Python for Finance, 2nd ed., O'Reilly Media
* Big thanks to my friend Ilham Salahov for giving me feedback on this project 💗
