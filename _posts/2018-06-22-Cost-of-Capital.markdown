---
layout: post
title:  "Cost of Capital"
date:   2018-07-22 20:08:21 -0700
categories: finance
tags: finance
---
### What is the Cost of Capital?

The question of Cost of Capital is a common [IBD Interview Question](https://utopiancapitalist.github.io/finance/2018/06/22/interview-questions-3.html) and essential to any financial analyst. A financial model is dependent on many variables, but the key drivers of the terminal value (1) are revenue and invested capital. Invested capital can come in the form of equity or debt, and neither of these sources come without a _cost of capital_. Note that Cost of Capital is often use synonymously with _Weighted Average Cost of Capital_, or _WACC_.

This is easy to conceptualize for debt. Say Company X (a $10M EV company) desires to build a capital project for $1 million. Given it only has $100K of cash on hand, it will need to draw debt to construct the project. Given its $10M enterprise value, the bank loans the money at a 10% interest rate to the company. This, multiplied by the outstanding debt balance, is the cost of debt capital.

As for equity, the calculation is more onerous. For a public company, this can be taken as: [Risk-free rate + (Beta * the Equity risk premium)]. Recall that Beta refers to how closely the company's stock price correlates to its market peers. Although Beta information can easily be found for public companies on finances sites such as Nasdaq or Yahoo Finance, they can also be derived by use of regression analysis on the company's stock price. The Risk-free rate is often represented by the 10-year U.S. Treasury bond rate for North American companies. Finally, the [equity risk premium is a prediction of how the stock market will outperform risk-free debt instruments.](https://www.investopedia.com/investing/calculating-equity-risk-premium/) This is calculated be (1) estimating the expected return on stocks, (2) estimating the expected return on risk-free bonds, and (3) subtracting the difference to obtain the equity risk premium.

Thus, Company X's overall cost of capital becomes evident when the cost of debt capital is weighted against the cost of equity capital.

### Why is it important to correctly estimate WACC?
WACC is highly influential in arriving at the terminal valuation of a company. A WACC that is obtusely high will result in an overly optimistic terminal valuation, while a WACC disproportionally low will result in an pessimistic terminal valuation.

### How is WACC modeled?

There are three calculations to a WACC model.

1. Calculate Cost of Equity by multiplying the Risk Free Rate by (Beta * Equity Risk Premium).
2. Calculate Cost of Debt by multiplying the Cost of Debt by (1-Tax Rate)
3. Multiple the Cost of Equity (i.e 8.5%) and Cost of Debt (i.e 3.9%) by their respective % in the Debt to Equity Ratio.

![Example WACC Calculation]({{ utopiancapitalist.github.io }}/assets/WACC1.png)
<img src="/assets/WACC1.png" alt="drawing" width="200"/>

(1) Terminal value will be discussed in a future post.
