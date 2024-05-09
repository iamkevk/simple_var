# Simplified Market Risk Analysis Using Value at Risk for an Equities-only Portfolio of a Retail Stock Investor

## Introduction

The overview work here is a class group project for `Team 001` in the Georgia Tech MGT 6203 Data Analytics Business, an advanced core subject offered as part of the [Online Master of Science in Analytics - OMSA](https://pe.gatech.edu/degrees/analytics). The MGT 6203 class, formerly taught by Prof. Frederic Bien in the Summer of 2023, covers basic methodologies, algorithms, and challenges related to analyzing business data. The class also covers applications of data analysis in:
1)	Finance & Investments
2)	Marketing & Advertising
3)	Operations & Logistics

***Disclaimer***: The views and opinions expressed in this project are those of the authors and do not necessarily reflect the views or positions of Georgia Tech.

## VAR Overview

> [Value at Risk (VaR)](https://www.investopedia.com/terms/v/var.asp) is a statistical measure that quantifies the extent of possible financial losses within a firm, portfolio, or position over a specific time frame. It's commonly used by investment and commercial banks to assess risk exposure.
> For example, a financial firm may determine an asset has a 3% one-month VaR of 2%, representing a 3% chance of the asset declining in value by 2% during the one-month time frame. The conversion of the 3% chance of occurrence to a daily ratio places the odds of a 2% loss at one day per month. 
> There are three main ways to compute VaR:

> - **Historical Method**: This approach looks at past returns history and orders them from worst losses to greatest gains. It assumes that past returns experience will inform future outcomes.
> - **Variance-Covariance Method (Parametric Method)**: This method assumes that gains and losses are normally distributed and frames potential losses in terms of standard deviation events from the mean.
> - **Monte Carlo Method**: This method uses random simulations to model potential portfolio returns. It's more flexible but computationally intensive.
> 
> By assessing firm-wide VaR, institutions can aggregate risks from different trading desks and departments to ensure adequate capital reserves. [^1]

## Project Motivation

VaR is an important risk management tool and metric that can be used by retail investors to assess and manage their portfolios. The VaR risk management model can be integrated into investment applications, providing investors with a comprehensive risk management tool. However, VaR poses challenges for retail investors due to its complexity, limited data accessibility, and potential modeling errors, hindering its effective use as a risk management tool. This exploratory group project aimed to democratize VaR and empower retail investors to make informed investment decisions.

## Our approach

We proposed a robust multi-factor analysis[^2] investigating the relationship between VaR and variables including market indicators such as GDP, VIX, S&P 500 and 10-year US government treasury yields and portfolio metrics such as portfolio beta, Sharpe ratio, Treynor ratio, and Jensen’s Alpha. Using logistic regression analysis, tree-based models, and variable selection techniques3, we aimed to help retail investors measure and address portfolio risk to navigate potential pitfalls and avoid succumbing to psychological biases that could lead to suboptimal decision-making.

## Implementation Overview
1. Extracted relevant data from [FRED API](https://fred.stlouisfed.org/docs/api/fred/) and Yahoo Finance.
2. Computed 1-month monthly VAR values over 130 months using the three main ways - Historical, Monte Carlo Simulation, and Parametric
3. Prepared the dataset and executed the logistic regression model.
4. Select the relevant variables based on the p-values.
5. Variable selection and run the logistic regression model again.
6. Evaluated the model on the test data set.
7. Run a random forest classifier on the training and test results of the logistic regression model.
8. Identified feature importance

## Performance metrics
- Historical S&P 500 index data
- Beta and Alpha
- Sharpe Ratio
- Treyner Ratio
- Jensen's Alpha

## Project Presentation

In the final [video presentation](https://www.youtube.com/watch?v=Caw6UfeNikM), we seek to answer the following question: 
- Given the relationship between specific economic indicators and portfolio performance, can we accurately forecast whether a specified VaR threshold for a particular portfolio will be breached?




## References
[^1]: [Investopedia](https://www.investopedia.com/terms/v/var.asp)
[^2]: Agarwal, V., & Naik, N. Y. (2004). Risks and portfolio decisions involving hedge funds. The Review of Financial Studies, 17(1), 63-98.




