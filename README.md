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
- Caculate portfolio average return and volatility
- Plot efficient frontier using Monte-carlo simulation
    - Identify minimum variance portfolio
    - Identify tangent portfolio by maximizing Sharpe Ratio
> Library: `scipy.optimize`, `scipy.interpolate`
### 👻 Findings


### 💡Key learnings

