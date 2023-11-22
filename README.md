### 🍉Summary
This project aims to find a portfolio structure that yields the highest profit given a specific level of risk tolerance of the investor. If you're interested in technical knowledge in investment, this project will show you how to:
* Find the minimum-variance portfolio using the Monte-Carlo simulation
* Identify tangent portfolio by maximizing Sharpe ratio
* Validate the assumptions of Modern Portfolio Theory (MPT) on the asset's pricing data
* Suggest an alternative optimization approach to MPT

If you're not a finance-savvy but still want to understand what I am doing here, let me try to explain the git of it. 

This analysis is based on the concept of diversification and Monte-Carlo methods, which can be quite useful in business forecast activities in my opinion. Let's say we open an ice cream business. If we were to add a new item to the business, what would you choose? A waffle may help to triple the sales of ice cream on a sunny day (great combination!) but _umbrellas would help to save the business during the rainy _days. **That's the beauty of diversification - to minimize the external risks to your business (like weather)**. In economic terms, we say waffle and ice cream has a positive correlation in sales while umbrella and ice cream sales are negatively correlated. If you are high-risk tolerant, you're more likely to add more products that have a positive correlation with the sales of ice cream like waffles rather than umbrellas. If you're risk-averse, you choose the other way around. Also, the number of rainy days per year also plays a role in your decision and it's one of the random factors that cause fluctuation to your revenue. **At the end of the day, you need the decide on an optimal proportion of each product that helps to reach your revenue goal with the least sales uncertainty**.

Monte Carlo simulation is one of the tools that help you do that. **It gives you insights into the probability of the outcomes given there are random factors in your model** by simulating a large number of possible scenarios.

This is undoubtedly one of the most challenging projects that I have done, concerning the tremendous time to grasp the idea of Portfolio Theory and learn optimization tools in Python's scipy library, but thank God, I made it.
