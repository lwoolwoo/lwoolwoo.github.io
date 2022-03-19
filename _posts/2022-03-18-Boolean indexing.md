---
layout: single
title:  "Practice #10 Boolean indexing"
---


```python
import pandas as pd
```


```python
df = pd.read_excel("E12EXAMPLE.xlsx")
df.head(3)
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
      <th>Name</th>
      <th>Subject</th>
      <th>Phone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Louis</td>
      <td>Korean</td>
      <td>010-6138-6625</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Harvey</td>
      <td>Japanese</td>
      <td>010-2901-3320</td>
    </tr>
    <tr>
      <th>2</th>
      <td>G-dragon</td>
      <td>Chinese</td>
      <td>010-5132-3850</td>
    </tr>
  </tbody>
</table>
</div>




```python
pdf = df.pivot_table("Name", index="Subject", aggfunc="count")
pdf
a1 = pdf.loc[pdf["Name"]<10].index
df.loc[df["Subject"].isin(a1)].to_clipboard(index=False)
```
