## 1. Read a excel file : read_excel()


```python
import pandas as pd

df1 = pd.read_excel("E03EXAMPLE.xlsx", sheet_name=1)
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
      <th>Name</th>
      <th>Cafe Name</th>
      <th>Drink</th>
      <th>Quantity</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Louis</td>
      <td>Starbucks</td>
      <td>Americano</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Harvey</td>
      <td>CoffeeBean</td>
      <td>CafeLatte</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>G-dragon</td>
      <td>CoffeeBean</td>
      <td>IcedTea</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Lola</td>
      <td>Starbucks</td>
      <td>IcedTea</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jorge</td>
      <td>CoffeeBean</td>
      <td>Americano</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Piona</td>
      <td>CoffeeBean</td>
      <td>CafeLatte</td>
      <td>1</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Mitchy</td>
      <td>CoffeeBean</td>
      <td>CafeLatte</td>
      <td>1</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Fibio</td>
      <td>Starbucks</td>
      <td>IcedTea</td>
      <td>1</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Kim</td>
      <td>CoffeeBean</td>
      <td>IcedTea</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Stacy</td>
      <td>CoffeeBean</td>
      <td>Americano</td>
      <td>1</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Grace</td>
      <td>CoffeeBean</td>
      <td>Americano</td>
      <td>1</td>
    </tr>
    <tr>
      <th>11</th>
      <td>TL</td>
      <td>CoffeeBean</td>
      <td>IcedTea</td>
      <td>1</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Sanchez</td>
      <td>CoffeeBean</td>
      <td>CafeLatte</td>
      <td>1</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Zhen</td>
      <td>Starbucks</td>
      <td>Americano</td>
      <td>1</td>
    </tr>
    <tr>
      <th>14</th>
      <td>James</td>
      <td>Starbucks</td>
      <td>CafeLatte</td>
      <td>1</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Coline</td>
      <td>Starbucks</td>
      <td>IcedTea</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Gorila</td>
      <td>Starbucks</td>
      <td>CafeLatte</td>
      <td>1</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Sunny</td>
      <td>CoffeeBean</td>
      <td>IcedTea</td>
      <td>1</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Conner</td>
      <td>Starbucks</td>
      <td>CafeLatte</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2 = pd.read_excel("E03EXAMPLE.xlsx", sheet_name=2)
df2
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
      <th>Cafe Name</th>
      <th>Drink</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Starbucks</td>
      <td>Americano</td>
      <td>4400</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Starbucks</td>
      <td>CafeLatte</td>
      <td>4700</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Starbucks</td>
      <td>IcedTea</td>
      <td>5000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>CoffeeBean</td>
      <td>Americano</td>
      <td>4900</td>
    </tr>
    <tr>
      <th>4</th>
      <td>CoffeeBean</td>
      <td>CafeLatte</td>
      <td>4200</td>
    </tr>
    <tr>
      <th>5</th>
      <td>CoffeeBean</td>
      <td>IcedTea</td>
      <td>4500</td>
    </tr>
  </tbody>
</table>
</div>



## 2. Merge two dataframes : merge()


```python
df3 = df1.merge(df2, how='left')
df3
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
      <th>Cafe Name</th>
      <th>Drink</th>
      <th>Quantity</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Louis</td>
      <td>Starbucks</td>
      <td>Americano</td>
      <td>1</td>
      <td>4400</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Harvey</td>
      <td>CoffeeBean</td>
      <td>CafeLatte</td>
      <td>1</td>
      <td>4200</td>
    </tr>
    <tr>
      <th>2</th>
      <td>G-dragon</td>
      <td>CoffeeBean</td>
      <td>IcedTea</td>
      <td>1</td>
      <td>4500</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Lola</td>
      <td>Starbucks</td>
      <td>IcedTea</td>
      <td>1</td>
      <td>5000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jorge</td>
      <td>CoffeeBean</td>
      <td>Americano</td>
      <td>1</td>
      <td>4900</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Piona</td>
      <td>CoffeeBean</td>
      <td>CafeLatte</td>
      <td>1</td>
      <td>4200</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Mitchy</td>
      <td>CoffeeBean</td>
      <td>CafeLatte</td>
      <td>1</td>
      <td>4200</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Fibio</td>
      <td>Starbucks</td>
      <td>IcedTea</td>
      <td>1</td>
      <td>5000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Kim</td>
      <td>CoffeeBean</td>
      <td>IcedTea</td>
      <td>1</td>
      <td>4500</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Stacy</td>
      <td>CoffeeBean</td>
      <td>Americano</td>
      <td>1</td>
      <td>4900</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Grace</td>
      <td>CoffeeBean</td>
      <td>Americano</td>
      <td>1</td>
      <td>4900</td>
    </tr>
    <tr>
      <th>11</th>
      <td>TL</td>
      <td>CoffeeBean</td>
      <td>IcedTea</td>
      <td>1</td>
      <td>4500</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Sanchez</td>
      <td>CoffeeBean</td>
      <td>CafeLatte</td>
      <td>1</td>
      <td>4200</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Zhen</td>
      <td>Starbucks</td>
      <td>Americano</td>
      <td>1</td>
      <td>4400</td>
    </tr>
    <tr>
      <th>14</th>
      <td>James</td>
      <td>Starbucks</td>
      <td>CafeLatte</td>
      <td>1</td>
      <td>4700</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Coline</td>
      <td>Starbucks</td>
      <td>IcedTea</td>
      <td>1</td>
      <td>5000</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Gorila</td>
      <td>Starbucks</td>
      <td>CafeLatte</td>
      <td>1</td>
      <td>4700</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Sunny</td>
      <td>CoffeeBean</td>
      <td>IcedTea</td>
      <td>1</td>
      <td>4500</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Conner</td>
      <td>Starbucks</td>
      <td>CafeLatte</td>
      <td>1</td>
      <td>4700</td>
    </tr>
  </tbody>
</table>
</div>



## 3. Restructuring the chart : pivot_table()


```python
pdf1 = df3.pivot_table("Quantity", index=["Cafe Name", "Drink"], aggfunc="count")
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
      <th></th>
      <th></th>
      <th>Quantity</th>
    </tr>
    <tr>
      <th>Cafe Name</th>
      <th>Drink</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="3" valign="top">CoffeeBean</th>
      <th>Americano</th>
      <td>3</td>
    </tr>
    <tr>
      <th>CafeLatte</th>
      <td>4</td>
    </tr>
    <tr>
      <th>IcedTea</th>
      <td>4</td>
    </tr>
    <tr>
      <th rowspan="3" valign="top">Starbucks</th>
      <th>Americano</th>
      <td>2</td>
    </tr>
    <tr>
      <th>CafeLatte</th>
      <td>3</td>
    </tr>
    <tr>
      <th>IcedTea</th>
      <td>3</td>
    </tr>
  </tbody>
</table>
</div>




```python
pdf2 = df3.pivot_table("Price", index="Cafe Name", aggfunc="sum")
pdf2
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
      <th>Price</th>
    </tr>
    <tr>
      <th>Cafe Name</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>CoffeeBean</th>
      <td>49500</td>
    </tr>
    <tr>
      <th>Starbucks</th>
      <td>37900</td>
    </tr>
  </tbody>
</table>
</div>



## 4. Copy to the clipboard : to_clipboar()


```python
pdf1.to_clipboard(index=False)
```


```python
pdf2.to_clipboard(index=False)
```

## 5. Total code


```python
import pandas as pd

df1 = pd.read_excel("E03EXAMPLE.xlsx", sheet_name=1)
df2 = pd.read_excel("E03EXAMPLE.xlsx", sheet_name=2)
df3 = df1.merge(df2, how="left")
pdf1 = df3.pivot_table("Quantity", index=["Cafe Name", "Drink"], aggfunc="count")
pdf2 = df3.pivot_table("Price", index="Cafe Name", aggfunc="sum")
pdf1.to_clipboard(index=False)
pdf2.to_cllpboard(index=False)
```
