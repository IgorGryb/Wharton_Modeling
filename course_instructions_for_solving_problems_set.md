Those files are:

(i) historical daily prices for ten individual stocks (AAPL, MSFT, WFC, DIS, COP, XOM, GOOG, BIDU, TSLA, and TTM) and for the Dow Jones market index, DJI (sample window: June 30th 2010 – June 30th 2016); and

(ii) monthly prices for AAPL (sample window: August 2015 - July 2016)
Step 2.

Using the historical data downloaded:

2.1 Calculate the daily return for each security and DJI using both the “Close price” and “Adjusted Close” price. Compare the difference between these two return series and think about what causes the difference (if there’s any).

(You will be provided with a sample return to verify whether your calculations are correct.)

2.2 Using the results you get from Step 2.1, calculate the following summary statistics of the return series for the “Adjusted Close” prices:

1. mean

2. standard deviation

3. min max

4. Sharpe Ratio*

*The Sharpe Ratio is a widely used tool for measuring the riskiness of investments. For more information on this concept, see the materials presented with Module 2.  Assume the “risk free asset” rate = 0.

In the assessment for this week, you’ll be asked to verify some of your calculations and answer questions based on a comparison of the summary statistics of the index DJI against the individual stocks.

Step 3.

Now imagine you are a portfolio manager at an equity quant fund with the option to invest your portfolio in the stocks listed above. Using your knowledge of portfolio variance and the efficient frontier (see Module 3 for more information on these concepts), complete the following:

3.1 If you are only allowed to invest in two stocks, MSFT and WFC, how would you allocate your investment to arrive at a portfolio with the minimum variance (as well as the lowest standard deviation)? You are not allowed to hold cash, so 100% of your portfolio has to be devoted to these two stocks.

First, calculate the approximate weights. Hint: Use a 5% increment in weights (e.g. 0%, 5%, …, 95%, 100%) in each stock, calculate the corresponding portfolio return and standard deviation. Plot the efficient frontier using the portfolio characteristics for each weight.

How much weight, approximated to the nearest whole percentage, would you assign to MSFT and WFC respectively to achieve the lowest portfolio variance?

3.2 Using the Solver function in Excel, next calculate the exact weight in WFC and MSFT for the minimum variance portfolio, rounded to the nearest tenth decimal point. Verify your answer with the approximation you obtained from Step 3.1 - they should be close.

Hint: You can assign your initial portfolio as an equal weighted portfolio before using the Solver function in Excel.
Next, using the same technique, please work out the weights for the “optimal risky portfolio” on the efficient frontier consisting of WFC and MSFT.  The “optimal risky portfolio” is also known as the “tangent portfolio” because it is where the
meets the efficient frontier (the tangency point).  See Module 3 for more information on these concepts.

Hint: Your goal now is to find the maximum value of the Sharpe Ratio of the portfolio. For simplicity, always assume the risk free rate = 0.

In the assessment for this week, you’ll be asked to compare your "optimal risky portfolio" characteristics to those of the two individual stocks used in the portfolio.

3.3 After your client reviews your proposal from the exercise involving two stocks, she really likes the idea of risk diversification. As a portfolio manager, you are given the right to invest in all 10 of the securities listed in the pool (note, this does not include DJI).

Can you work out your “optimal risky portfolio” (a.k.a. tangent portfolio) on the efficient frontier using all 10 securities?

Hint: You can use the same logic and Solver built from Step 3.2.

Calculate your final portfolio weights in each stock and the portfolio characteristics (mean, std dev, and sharpe ratio).

You should find that some of your weights come out negative.  This means that the optimal risky portfolio contemplates “short selling.”  See Module 3 for more information on short selling (if your minimum weight = 0 instead of being negative, please make sure to uncheck the “Make Unconstrained Variables Non-Negative” option in the Solver Parameters window).

What if your mandate does not allow you to participate in short selling activity? In other words, the lowest weight you can impose on the stocks in your portfolio is zero. What is your portfolio composition under this ‘constrained’ or ‘long-only’ regime?

Hint: You can repeat the same exercise as in the short selling case. You only need to check “Make Unconstrained Variables Non-Negative” this time.

Step 4.

For this optional, non-credit exercise, you will be working with the Capital Asset Pricing Model (CAPM).  See Module 4 for more on this concept.

Using Excel, calculate the Alpha and Beta loadings of the 10 securities on the market index DJI.

Hint: You can use the regression function in Excel under the “Data Analysis” add-on.

In the optional assessment for this Step, you’ll be asked to use the CAPM model results to determine which stock is the riskiest investment and which one is the least risky.

Step 5.

You have just applied the knowledge of efficient frontier and portfolio optimization in managing a pure equity portfolio in Steps 3 and 4. In real life, many investment strategies utilize other assets or a mix of several, including fixed income, money market funds, commodities, foreign currencies, and even real estates. For instance, among the
close to half invest in assets other than equity.

Using the same set of knowledge on portfolio diversification, you are now required to plan for an investment portfolio of $5 million. Your mandate allows you to invest in the following investment vehicles: Vanguard Total Bond Market Index Fund (ticker: VBTLX) and Vanguard 500 Index (ticker: VFIAX). These two funds represent investment vehicles in fixed income and equity, respectively.

Your data set for this part of the project includes the monthly prices for AAPL provided in the "Historical Stock Data" link in Module 1, as well as the historical monthly returns data for VBTLX and VFIAX from January 2012 to July 2016.

You are encouraged to practice retrieving and inputting the VBTLX and VFIAX returns data by:
b.  Searching in the “Quote” box for fund performances using the ticker given, then click on the “Performance” tab to find the monthly total returns at the bottom of the page.

c.  Copying historical monthly returns data from January 2012 to July 2016 in a spreadsheet (NOTE: The returns are percentages but are presented without a percentage sign, so make sure that when entering them into your spreadsheet they are treated as percentages).  
/Users/igorgrybek/Cursor/Wharton_Modeling/_b01664a045fe7720c1bf143fe3fef7a9_VBTLX-and-VFIAX-Monthly-Returns.xlsx

5.1 Your goal is to again design a portfolio allocation that represents a "optimal risky portfolio" on the efficient frontier. How much of the $5 million would you invest in each of the two funds as of the end of December 2015?

5.2 Assume you keep the portfolio weights fixed as of the end of the December 2015. Calculate your portfolio monthly return for the period January 2016 through the end of July 2016.

5.3 In light of the calculations in Steps 5.1 and 5.2, as well as what you’ve learned more generally about portfolio diversification and risk, consider this question: how does the monthly performance of your portfolio of a mixed asset class of funds compare to the single security AAPL?

Present your findings and discuss the importance of portfolio diversification in a short power point presentation to your potential clients (see Module 5 for more information on this assignment).

Good luck!
