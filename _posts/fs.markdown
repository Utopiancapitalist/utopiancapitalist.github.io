layout: post
title:  "Sensitivity Analysis"
date:   2018-06-28 20:08:21 -0700
categories: finance
tags: finance
---
### A Detailed Description of Sensitivity Analysis is Coming Soon


```python
import pandas as pd
import numpy as np
```


```python
df = pd.read_excel("wdc_K.xlsx")
df.dropna(how='all', inplace=True)
```


```python
df = df.replace(r'^\s+$', np.nan, regex=True)
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Consolidated Balance Sheets - USD ($) $ in Millions</th>
      <th>Jun. 29, 2018</th>
      <th>Jun. 30, 2017</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Current assets:</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Cash and cash equivalents</td>
      <td>5005.0</td>
      <td>6354.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Accounts receivable, net</td>
      <td>2197.0</td>
      <td>1948.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Inventories</td>
      <td>2944.0</td>
      <td>2341.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Other current assets</td>
      <td>492.0</td>
      <td>413.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Total current assets</td>
      <td>10638.0</td>
      <td>11056.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Non-current assets:</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Property, plant and equipment, net</td>
      <td>3095.0</td>
      <td>3033.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Notes receivable and investments in Flash Vent...</td>
      <td>2105.0</td>
      <td>1340.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Goodwill</td>
      <td>10075.0</td>
      <td>10014.0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Other intangible assets, net</td>
      <td>2680.0</td>
      <td>3823.0</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Other non-current assets</td>
      <td>642.0</td>
      <td>594.0</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Total assets</td>
      <td>29235.0</td>
      <td>29860.0</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Current liabilities:</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Accounts payable</td>
      <td>2265.0</td>
      <td>2144.0</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Accounts payable to related parties</td>
      <td>259.0</td>
      <td>206.0</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Accrued expenses</td>
      <td>1274.0</td>
      <td>1255.0</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Accrued compensation</td>
      <td>479.0</td>
      <td>506.0</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Current portion of long-term debt</td>
      <td>179.0</td>
      <td>233.0</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Total current liabilities</td>
      <td>4456.0</td>
      <td>4344.0</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Non-current liabilities:</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Long-term debt</td>
      <td>10993.0</td>
      <td>12918.0</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Other liabilities</td>
      <td>2255.0</td>
      <td>1180.0</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Total liabilities</td>
      <td>17704.0</td>
      <td>18442.0</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Commitments and contingencies (Notes 6, 9, 13 ...</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Shareholders’ equity:</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Preferred stock, $0.01 par value; authorized —...</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Common stock, $0.01 par value; authorized — 45...</td>
      <td>3.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Additional paid-in capital</td>
      <td>4254.0</td>
      <td>4506.0</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Accumulated other comprehensive loss</td>
      <td>-39.0</td>
      <td>-58.0</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Retained earnings</td>
      <td>8757.0</td>
      <td>8633.0</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Treasury stock — common shares at cost; 16 sha...</td>
      <td>-1444.0</td>
      <td>-1666.0</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Total shareholders’ equity</td>
      <td>11531.0</td>
      <td>11418.0</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Total liabilities and shareholders’ equity</td>
      <td>29235.0</td>
      <td>29860.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.fillna(0, inplace=True)
```


```python
df = df.rename({'Consolidated Balance Sheets - USD ($) $ in Millions':'Consolidated Balance Sheet In Millions'}, axis=1)
```


```python
print df
```

                   Consolidated Balance Sheet In Millions  Jun. 29, 2018  \
    0                                     Current assets:            0.0   
    1                           Cash and cash equivalents         5005.0   
    2                            Accounts receivable, net         2197.0   
    3                                         Inventories         2944.0   
    4                                Other current assets          492.0   
    5                                Total current assets        10638.0   
    6                                 Non-current assets:            0.0   
    7                  Property, plant and equipment, net         3095.0   
    8   Notes receivable and investments in Flash Vent...         2105.0   
    9                                            Goodwill        10075.0   
    10                       Other intangible assets, net         2680.0   
    11                           Other non-current assets          642.0   
    12                                       Total assets        29235.0   
    13                               Current liabilities:            0.0   
    14                                   Accounts payable         2265.0   
    15                Accounts payable to related parties          259.0   
    16                                   Accrued expenses         1274.0   
    17                               Accrued compensation          479.0   
    18                  Current portion of long-term debt          179.0   
    19                          Total current liabilities         4456.0   
    20                           Non-current liabilities:            0.0   
    21                                     Long-term debt        10993.0   
    22                                  Other liabilities         2255.0   
    23                                  Total liabilities        17704.0   
    24  Commitments and contingencies (Notes 6, 9, 13 ...            0.0   
    25                              Shareholders’ equity:            0.0   
    26  Preferred stock, $0.01 par value; authorized —...            0.0   
    27  Common stock, $0.01 par value; authorized — 45...            3.0   
    28                         Additional paid-in capital         4254.0   
    29               Accumulated other comprehensive loss          -39.0   
    30                                  Retained earnings         8757.0   
    31  Treasury stock — common shares at cost; 16 sha...        -1444.0   
    32                         Total shareholders’ equity        11531.0   
    33         Total liabilities and shareholders’ equity        29235.0   

        Jun. 30, 2017  
    0             0.0  
    1          6354.0  
    2          1948.0  
    3          2341.0  
    4           413.0  
    5         11056.0  
    6             0.0  
    7          3033.0  
    8          1340.0  
    9         10014.0  
    10         3823.0  
    11          594.0  
    12        29860.0  
    13            0.0  
    14         2144.0  
    15          206.0  
    16         1255.0  
    17          506.0  
    18          233.0  
    19         4344.0  
    20            0.0  
    21        12918.0  
    22         1180.0  
    23        18442.0  
    24            0.0  
    25            0.0  
    26            0.0  
    27            3.0  
    28         4506.0  
    29          -58.0  
    30         8633.0  
    31        -1666.0  
    32        11418.0  
    33        29860.0  



```python
df['Jun. 29, 2018']=df.apply(lambda x: "{:,}".format(x['Jun. 29, 2018']), axis=1)
```


```python
df['Jun. 30, 2017']=df.apply(lambda x: "{:,}".format(x['Jun. 30, 2017']), axis=1)
```


```python
print df
```

                   Consolidated Balance Sheet In Millions Jun. 29, 2018  \
    0                                     Current assets:           0.0   
    1                           Cash and cash equivalents       5,005.0   
    2                            Accounts receivable, net       2,197.0   
    3                                         Inventories       2,944.0   
    4                                Other current assets         492.0   
    5                                Total current assets      10,638.0   
    6                                 Non-current assets:           0.0   
    7                  Property, plant and equipment, net       3,095.0   
    8   Notes receivable and investments in Flash Vent...       2,105.0   
    9                                            Goodwill      10,075.0   
    10                       Other intangible assets, net       2,680.0   
    11                           Other non-current assets         642.0   
    12                                       Total assets      29,235.0   
    13                               Current liabilities:           0.0   
    14                                   Accounts payable       2,265.0   
    15                Accounts payable to related parties         259.0   
    16                                   Accrued expenses       1,274.0   
    17                               Accrued compensation         479.0   
    18                  Current portion of long-term debt         179.0   
    19                          Total current liabilities       4,456.0   
    20                           Non-current liabilities:           0.0   
    21                                     Long-term debt      10,993.0   
    22                                  Other liabilities       2,255.0   
    23                                  Total liabilities      17,704.0   
    24  Commitments and contingencies (Notes 6, 9, 13 ...           0.0   
    25                              Shareholders’ equity:           0.0   
    26  Preferred stock, $0.01 par value; authorized —...           0.0   
    27  Common stock, $0.01 par value; authorized — 45...           3.0   
    28                         Additional paid-in capital       4,254.0   
    29               Accumulated other comprehensive loss         -39.0   
    30                                  Retained earnings       8,757.0   
    31  Treasury stock — common shares at cost; 16 sha...      -1,444.0   
    32                         Total shareholders’ equity      11,531.0   
    33         Total liabilities and shareholders’ equity      29,235.0   

       Jun. 30, 2017  
    0            0.0  
    1        6,354.0  
    2        1,948.0  
    3        2,341.0  
    4          413.0  
    5       11,056.0  
    6            0.0  
    7        3,033.0  
    8        1,340.0  
    9       10,014.0  
    10       3,823.0  
    11         594.0  
    12      29,860.0  
    13           0.0  
    14       2,144.0  
    15         206.0  
    16       1,255.0  
    17         506.0  
    18         233.0  
    19       4,344.0  
    20           0.0  
    21      12,918.0  
    22       1,180.0  
    23      18,442.0  
    24           0.0  
    25           0.0  
    26           0.0  
    27           3.0  
    28       4,506.0  
    29         -58.0  
    30       8,633.0  
    31      -1,666.0  
    32      11,418.0  
    33      29,860.0  



```python
df = df.set_index("Consolidated Balance Sheet In Millions")
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Jun. 29, 2018</th>
      <th>Jun. 30, 2017</th>
    </tr>
    <tr>
      <th>Consolidated Balance Sheet In Millions</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Current assets:</th>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>Cash and cash equivalents</th>
      <td>5,005.0</td>
      <td>6,354.0</td>
    </tr>
    <tr>
      <th>Accounts receivable, net</th>
      <td>2,197.0</td>
      <td>1,948.0</td>
    </tr>
    <tr>
      <th>Inventories</th>
      <td>2,944.0</td>
      <td>2,341.0</td>
    </tr>
    <tr>
      <th>Other current assets</th>
      <td>492.0</td>
      <td>413.0</td>
    </tr>
    <tr>
      <th>Total current assets</th>
      <td>10,638.0</td>
      <td>11,056.0</td>
    </tr>
    <tr>
      <th>Non-current assets:</th>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>Property, plant and equipment, net</th>
      <td>3,095.0</td>
      <td>3,033.0</td>
    </tr>
    <tr>
      <th>Notes receivable and investments in Flash Ventures</th>
      <td>2,105.0</td>
      <td>1,340.0</td>
    </tr>
    <tr>
      <th>Goodwill</th>
      <td>10,075.0</td>
      <td>10,014.0</td>
    </tr>
    <tr>
      <th>Other intangible assets, net</th>
      <td>2,680.0</td>
      <td>3,823.0</td>
    </tr>
    <tr>
      <th>Other non-current assets</th>
      <td>642.0</td>
      <td>594.0</td>
    </tr>
    <tr>
      <th>Total assets</th>
      <td>29,235.0</td>
      <td>29,860.0</td>
    </tr>
    <tr>
      <th>Current liabilities:</th>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>Accounts payable</th>
      <td>2,265.0</td>
      <td>2,144.0</td>
    </tr>
    <tr>
      <th>Accounts payable to related parties</th>
      <td>259.0</td>
      <td>206.0</td>
    </tr>
    <tr>
      <th>Accrued expenses</th>
      <td>1,274.0</td>
      <td>1,255.0</td>
    </tr>
    <tr>
      <th>Accrued compensation</th>
      <td>479.0</td>
      <td>506.0</td>
    </tr>
    <tr>
      <th>Current portion of long-term debt</th>
      <td>179.0</td>
      <td>233.0</td>
    </tr>
    <tr>
      <th>Total current liabilities</th>
      <td>4,456.0</td>
      <td>4,344.0</td>
    </tr>
    <tr>
      <th>Non-current liabilities:</th>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>Long-term debt</th>
      <td>10,993.0</td>
      <td>12,918.0</td>
    </tr>
    <tr>
      <th>Other liabilities</th>
      <td>2,255.0</td>
      <td>1,180.0</td>
    </tr>
    <tr>
      <th>Total liabilities</th>
      <td>17,704.0</td>
      <td>18,442.0</td>
    </tr>
    <tr>
      <th>Commitments and contingencies (Notes 6, 9, 13 and 16)</th>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>Shareholders’ equity:</th>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>Preferred stock, $0.01 par value; authorized — 5 shares; issued and outstanding — none</th>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>Common stock, $0.01 par value; authorized — 450 shares; issued — 312 shares in 2018 and 2017; outstanding — 296 shares in 2018 and 294 shares in 2017</th>
      <td>3.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>Additional paid-in capital</th>
      <td>4,254.0</td>
      <td>4,506.0</td>
    </tr>
    <tr>
      <th>Accumulated other comprehensive loss</th>
      <td>-39.0</td>
      <td>-58.0</td>
    </tr>
    <tr>
      <th>Retained earnings</th>
      <td>8,757.0</td>
      <td>8,633.0</td>
    </tr>
    <tr>
      <th>Treasury stock — common shares at cost; 16 shares in 2018 and 18 shares in 2017</th>
      <td>-1,444.0</td>
      <td>-1,666.0</td>
    </tr>
    <tr>
      <th>Total shareholders’ equity</th>
      <td>11,531.0</td>
      <td>11,418.0</td>
    </tr>
    <tr>
      <th>Total liabilities and shareholders’ equity</th>
      <td>29,235.0</td>
      <td>29,860.0</td>
    </tr>
  </tbody>
</table>
</div>
