---
layout: post
title:  "Security Analysis Part 2 - Alaska Airlines Group"
date:   2018-10-12 20:08:21 -0700
categories: finance
tags: finance
---
## This post examines Alaska Air Groups's FY2018 financial statements.

Today I'm going to examine the financials of Alaska Air Group with a particular intention of forecasting future earnings through a pro-forma model. This is the second post in a series on security analysis: see also the previous note on [Western Digital](https://utopiancapitalist.github.io/finance/2018/09/13/Security-Analysis.html).

The post is composed of three sections:
1) Comparison of balances, which will allow us to easily see trends from 2017 to 2018.
2) Pro-forma model developed from historical financial statements. For the purposes of this post, these will be rough estimates.
3) Concluding observations.

Note that I'm interested in performing this analysis in Python as opposed to Excel. The model shown here is a simplified edition of that which can be performed in Excel. Future models will be advanced from this point. Of note, the type of valuation I'm performing is *absolute*, that we are looking at the fundamental qualities of Alaska Air Group and deciphering a value of the company in the future based on these. This is distinct from  a relative valuation, which is a comparison against other similar stocks (i.e. the P/E ratio of Alaska Air Group as compared against American Airlines, Delta, and United - the competitor United States airlines).

### Comparing Balances

Comparing prior year and current year balances is standard practice within the financial industry. This allows one to easily decipher balances in increase and balances in decline.



<style  type="text/css" >
</style>  
<table id="T_f7b42fa8_286b_11e9_b189_c82a140053b3" >
<thead>    <tr>
        <th class="blank level0" ></th>
        <th class="col_heading level0 col0" >9-30-18</th>
        <th class="col_heading level0 col1" >9-30-17</th>
        <th class="col_heading level0 col2" >Difference 18v17</th>
        <th class="col_heading level0 col3" >Difference as %</th>
    </tr>    <tr>
        <th class="index_name level0" >Consolidated Income Statement In Millions</th>
        <th class="blank" ></th>
        <th class="blank" ></th>
        <th class="blank" ></th>
        <th class="blank" ></th>
    </tr></thead>
<tbody>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row0" class="row_heading level0 row0" >0</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row0_col0" class="data row0 col0" >0.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row0_col1" class="data row0 col1" >0.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row0_col2" class="data row0 col2" >0.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row0_col3" class="data row0 col3" >0.00%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row1" class="row_heading level0 row1" >Passenger revenue</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row1_col0" class="data row1 col0" >2,043.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row1_col1" class="data row1 col1" >1,958.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row1_col2" class="data row1 col2" >85.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row1_col3" class="data row1 col3" >4.34%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row2" class="row_heading level0 row2" >Mileage Plan other revenue</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row2_col0" class="data row2 col0" >114.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row2_col1" class="data row2 col1" >105.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row2_col2" class="data row2 col2" >9.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row2_col3" class="data row2 col3" >8.57%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row3" class="row_heading level0 row3" >Cargo and other</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row3_col0" class="data row3 col0" >55.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row3_col1" class="data row3 col1" >47.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row3_col2" class="data row3 col2" >8.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row3_col3" class="data row3 col3" >17.02%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row4" class="row_heading level0 row4" >Total Operating Revenues</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row4_col0" class="data row4 col0" >2,212.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row4_col1" class="data row4 col1" >2,110.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row4_col2" class="data row4 col2" >102.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row4_col3" class="data row4 col3" >4.83%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row5" class="row_heading level0 row5" >Operating Expenses</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row5_col0" class="data row5 col0" >0.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row5_col1" class="data row5 col1" >0.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row5_col2" class="data row5 col2" >0.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row5_col3" class="data row5 col3" >0.00%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row6" class="row_heading level0 row6" >Wages and benefits</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row6_col0" class="data row6 col0" >549.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row6_col1" class="data row6 col1" >477.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row6_col2" class="data row6 col2" >72.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row6_col3" class="data row6 col3" >15.09%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row7" class="row_heading level0 row7" >Variable incentive pay</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row7_col0" class="data row7 col0" >27.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row7_col1" class="data row7 col1" >40.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row7_col2" class="data row7 col2" >-13.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row7_col3" class="data row7 col3" >-32.50%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row8" class="row_heading level0 row8" >Aircraft fuel, including hedging gains</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row8_col0" class="data row8 col0" >513.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row8_col1" class="data row8 col1" >368.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row8_col2" class="data row8 col2" >145.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row8_col3" class="data row8 col3" >39.40%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row9" class="row_heading level0 row9" >and losses</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row9_col0" class="data row9 col0" >0.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row9_col1" class="data row9 col1" >0.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row9_col2" class="data row9 col2" >0.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row9_col3" class="data row9 col3" >0.00%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row10" class="row_heading level0 row10" >Aircraft maintenance</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row10_col0" class="data row10 col0" >107.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row10_col1" class="data row10 col1" >88.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row10_col2" class="data row10 col2" >19.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row10_col3" class="data row10 col3" >21.59%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row11" class="row_heading level0 row11" >Aircraft rent</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row11_col0" class="data row11 col0" >82.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row11_col1" class="data row11 col1" >70.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row11_col2" class="data row11 col2" >12.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row11_col3" class="data row11 col3" >17.14%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row12" class="row_heading level0 row12" >Landing fees and other rentals</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row12_col0" class="data row12 col0" >135.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row12_col1" class="data row12 col1" >124.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row12_col2" class="data row12 col2" >11.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row12_col3" class="data row12 col3" >8.87%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row13" class="row_heading level0 row13" >Contracted services</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row13_col0" class="data row13 col0" >70.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row13_col1" class="data row13 col1" >76.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row13_col2" class="data row13 col2" >-6.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row13_col3" class="data row13 col3" >-7.89%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row14" class="row_heading level0 row14" >Selling expenses</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row14_col0" class="data row14 col0" >79.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row14_col1" class="data row14 col1" >92.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row14_col2" class="data row14 col2" >-13.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row14_col3" class="data row14 col3" >-14.13%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row15" class="row_heading level0 row15" >Depreciation and amortization</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row15_col0" class="data row15 col0" >99.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row15_col1" class="data row15 col1" >95.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row15_col2" class="data row15 col2" >4.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row15_col3" class="data row15 col3" >4.21%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row16" class="row_heading level0 row16" >Food and beverage service</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row16_col0" class="data row16 col0" >53.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row16_col1" class="data row16 col1" >50.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row16_col2" class="data row16 col2" >3.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row16_col3" class="data row16 col3" >6.00%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row17" class="row_heading level0 row17" >Third-party regional carrier expense</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row17_col0" class="data row17 col0" >38.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row17_col1" class="data row17 col1" >30.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row17_col2" class="data row17 col2" >8.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row17_col3" class="data row17 col3" >26.67%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row18" class="row_heading level0 row18" >Other</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row18_col0" class="data row18 col0" >141.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row18_col1" class="data row18 col1" >150.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row18_col2" class="data row18 col2" >-9.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row18_col3" class="data row18 col3" >-6.00%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row19" class="row_heading level0 row19" >Special items-merger-related costs</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row19_col0" class="data row19 col0" >22.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row19_col1" class="data row19 col1" >23.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row19_col2" class="data row19 col2" >-1.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row19_col3" class="data row19 col3" >-4.35%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row20" class="row_heading level0 row20" >Special items-other</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row20_col0" class="data row20 col0" >0.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row20_col1" class="data row20 col1" >0.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row20_col2" class="data row20 col2" >0.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row20_col3" class="data row20 col3" >0.00%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row21" class="row_heading level0 row21" >Total Operating Expenses</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row21_col0" class="data row21 col0" >1,915.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row21_col1" class="data row21 col1" >1,683.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row21_col2" class="data row21 col2" >232.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row21_col3" class="data row21 col3" >13.78%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row22" class="row_heading level0 row22" >Operating Income</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row22_col0" class="data row22 col0" >297.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row22_col1" class="data row22 col1" >427.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row22_col2" class="data row22 col2" >-130.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row22_col3" class="data row22 col3" >-30.44%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row23" class="row_heading level0 row23" >Nonoperating Income (Expense)</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row23_col0" class="data row23 col0" >0.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row23_col1" class="data row23 col1" >0.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row23_col2" class="data row23 col2" >0.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row23_col3" class="data row23 col3" >0.00%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row24" class="row_heading level0 row24" >Interest income</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row24_col0" class="data row24 col0" >11.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row24_col1" class="data row24 col1" >9.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row24_col2" class="data row24 col2" >2.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row24_col3" class="data row24 col3" >22.22%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row25" class="row_heading level0 row25" >Interest expense</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row25_col0" class="data row25 col0" >-22.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row25_col1" class="data row25 col1" >-26.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row25_col2" class="data row25 col2" >4.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row25_col3" class="data row25 col3" >-15.38%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row26" class="row_heading level0 row26" >Interest capitalized</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row26_col0" class="data row26 col0" >5.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row26_col1" class="data row26 col1" >5.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row26_col2" class="data row26 col2" >0.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row26_col3" class="data row26 col3" >0.00%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row27" class="row_heading level0 row27" >Other-net</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row27_col0" class="data row27 col0" >-7.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row27_col1" class="data row27 col1" >2.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row27_col2" class="data row27 col2" >-9.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row27_col3" class="data row27 col3" >-450.00%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row28" class="row_heading level0 row28" >Total Nonoperating Income (Expense)</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row28_col0" class="data row28 col0" >-13.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row28_col1" class="data row28 col1" >-10.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row28_col2" class="data row28 col2" >-3.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row28_col3" class="data row28 col3" >30.00%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row29" class="row_heading level0 row29" >Income Before Income Tax</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row29_col0" class="data row29 col0" >284.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row29_col1" class="data row29 col1" >417.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row29_col2" class="data row29 col2" >-133.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row29_col3" class="data row29 col3" >-31.89%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row30" class="row_heading level0 row30" >Income tax expense</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row30_col0" class="data row30 col0" >67.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row30_col1" class="data row30 col1" >158.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row30_col2" class="data row30 col2" >-91.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row30_col3" class="data row30 col3" >-57.59%</td>
    </tr>    <tr>
        <th id="T_f7b42fa8_286b_11e9_b189_c82a140053b3level0_row31" class="row_heading level0 row31" >Net Income</th>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row31_col0" class="data row31 col0" >217.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row31_col1" class="data row31 col1" >259.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row31_col2" class="data row31 col2" >-42.0</td>
        <td id="T_f7b42fa8_286b_11e9_b189_c82a140053b3row31_col3" class="data row31 col3" >-16.22%</td>
    </tr></tbody>
</table>
