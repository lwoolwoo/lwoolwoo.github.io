## 1. Read a excel file : read_excel()


```python
import pandas as pd

df1 = pd.read_excel("E07EXAMPLE.xlsx", sheet_name=1)
df1
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
      <th>Subject</th>
      <th>Name</th>
      <th>Mark</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Economics</td>
      <td>Louis</td>
      <td>99.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Economics</td>
      <td>Harvey</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Economics</td>
      <td>G-dragon</td>
      <td>95.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Economics</td>
      <td>Lola</td>
      <td>74.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Economics</td>
      <td>Jorge</td>
      <td>75.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>150</th>
      <td>Math</td>
      <td>CoolJ</td>
      <td>95.0</td>
    </tr>
    <tr>
      <th>151</th>
      <td>Math</td>
      <td>Kara</td>
      <td>92.0</td>
    </tr>
    <tr>
      <th>152</th>
      <td>Math</td>
      <td>Tiara</td>
      <td>74.0</td>
    </tr>
    <tr>
      <th>153</th>
      <td>Math</td>
      <td>Kolon</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>154</th>
      <td>Math</td>
      <td>SungGil</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>155 rows × 3 columns</p>
</div>



## 2. Restructure the chart : pivot_table()


```python
pdf1 = df1.pivot_table("Mark", index="Name", columns="Subject", aggfunc="count")
pdf1
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
      <th>Subject</th>
      <th>Economics</th>
      <th>English</th>
      <th>Math</th>
      <th>Science</th>
      <th>Sociology</th>
    </tr>
    <tr>
      <th>Name</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Coline</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Conner</th>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>CoolJ</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Fibio</th>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>G-dragon</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Gerge</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Gorila</th>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>Grace</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Guggi</th>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Harvey</th>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>James</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Jorge</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Kara</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Katy</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Kim</th>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Kolon</th>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Lola</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Louis</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Marry</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Mitchy</th>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Phil</th>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Piona</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Sally</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Sanchez</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Stacy</th>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>SungGil</th>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>Sunny</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>TL</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Tiara</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Zhen</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>kipling</th>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>



## 3. "If" function in Excel : mask()


```python
cond1 = pdf1 >= 1
pdf1 = pdf1.mask(cond1, "O").mask(~cond1, "X")
pdf1
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
      <th>Subject</th>
      <th>Economics</th>
      <th>English</th>
      <th>Math</th>
      <th>Science</th>
      <th>Sociology</th>
    </tr>
    <tr>
      <th>Name</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Coline</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Conner</th>
      <td>O</td>
      <td>O</td>
      <td>X</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>CoolJ</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Fibio</th>
      <td>O</td>
      <td>X</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>G-dragon</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Gerge</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Gorila</th>
      <td>O</td>
      <td>X</td>
      <td>O</td>
      <td>O</td>
      <td>X</td>
    </tr>
    <tr>
      <th>Grace</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Guggi</th>
      <td>O</td>
      <td>X</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Harvey</th>
      <td>X</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>James</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Jorge</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Kara</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>X</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Katy</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Kim</th>
      <td>O</td>
      <td>O</td>
      <td>X</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Kolon</th>
      <td>O</td>
      <td>O</td>
      <td>X</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Lola</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Louis</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Marry</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Mitchy</th>
      <td>O</td>
      <td>O</td>
      <td>X</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Phil</th>
      <td>O</td>
      <td>X</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Piona</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Sally</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Sanchez</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Stacy</th>
      <td>X</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>SungGil</th>
      <td>O</td>
      <td>O</td>
      <td>X</td>
      <td>O</td>
      <td>X</td>
    </tr>
    <tr>
      <th>Sunny</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>X</td>
      <td>O</td>
    </tr>
    <tr>
      <th>TL</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Tiara</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
    <tr>
      <th>Zhen</th>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>X</td>
      <td>O</td>
    </tr>
    <tr>
      <th>kipling</th>
      <td>X</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
      <td>O</td>
    </tr>
  </tbody>
</table>
</div>



## 4. Copy to the clipboard : to_clipboard()


```python
pdf1.to_clipboard()
```

## 5. Total Code


```python

import pandas as pd

df1 = pd.read_excel("E07EXAMPLE.xlsx", sheet_name=1)
pdf1 = df1.pivot_table("Mark", index="Name", columns="Subject", aggfunc="count")
cond1 = pdf1==1
pdf1 = pdf1.mask(cond1, "O").mask(~cond1, "X")
pdf1.to_clipboard()

```
