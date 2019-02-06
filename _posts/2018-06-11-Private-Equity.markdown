---
layout: post
title:  "Revolver"
date:   2018-07-11 20:08:21 -0700
categories: finance
tags: finance, economics, philosophy, public policy
---
### What is a revolver?

A revolver (revolving credit line) is a debt tool used by banks to withdraw cash as necessary, similar to a credit card in personal finance. The credit withdrawn with a bank might often be $0 so as to avoid interest penalties, but this tool allows a company to remain liquid without having to exchange illiquid assets (i.e. long term investments).

Note that companies have limits on how much they can withdraw. For a $200M loan, $40M of this may be a revolving credit line. How much a company can withdraw depends on its "borrowing base," which refers to the liquid assets (AR, Inventory, etc.) that secure the revolver. Typically, inventory can be liquidated at 80% of its value while AR is 90%.

### How is a revolver modeled?

The revolver should work in tandem with the cash balance. In essence, a revolver balance should grow if there is a deficit, while cash should grow if there is a surplus (unless there is first a deficit, in which case the revolver should be reduced). The deficit/surplus can be calculated from the cash flow statement.

--> The MIN function can be used for this calculation
--> Note that circularity may occur, resulting in an Excel error. To account for this, simply enter the Excel options, go to the formulas tab, and click the "enable iterative calculation" button.

See [Here](https://www.wallstreetprep.com/knowledge/modeling-revolving-credit-line-excel-free-template/) for an excellent template for learning to use the Revolver in practice.

Another helpful website in working through the [modeling of a revolver.](http://www.streetofwalls.com/finance-training-courses/investment-banking-technical-training/three-statement-financial-modeling/)
