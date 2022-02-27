---
layout: single
title:  "Practice # 10 broadcasting"
---


```python
import pandas as pd
```


```python
df1 = pd.read_excel("E11EXAMPLE.xlsx").set_index("Stock")
df2 = pd.read_excel("E11EXAMPLE.xlsx", sheet_name=1)
```


```python
df1.mul(df2.iloc[-1, 1:],axis=0).dropna().head(3)
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
      <th>E</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>KT</th>
      <td>31800000.0</td>
      <td>25440000.0</td>
      <td>6360000.0</td>
      <td>0.0</td>
      <td>38160000.0</td>
    </tr>
    <tr>
      <th>SK</th>
      <td>640000000.0</td>
      <td>800000000.0</td>
      <td>0.0</td>
      <td>960000000.0</td>
      <td>320000000.0</td>
    </tr>
    <tr>
      <th>Samsung</th>
      <td>16140000.0</td>
      <td>32280000.0</td>
      <td>16140000.0</td>
      <td>8070000.0</td>
      <td>8070000.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1.mul(df2.iloc[-1, 1:],axis=0).dropna().to_clipboard()
```
