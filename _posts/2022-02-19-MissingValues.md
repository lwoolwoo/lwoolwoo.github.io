## 1. Read a excel file : read_excel()


```python
import pandas as pd

df1 = pd.read_excel("E04EXAMPLE.xlsx", sheet_name=1)
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
      <th>Mark</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Louis</td>
      <td>100.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Harvey</td>
      <td>59.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>G-dragon</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Lola</td>
      <td>87.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jorge</td>
      <td>90.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Piona</td>
      <td>54.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Mitchy</td>
      <td>93.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Fibio</td>
      <td>94.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Kim</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Stacy</td>
      <td>71.0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Grace</td>
      <td>96.0</td>
    </tr>
    <tr>
      <th>11</th>
      <td>TL</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Sanchez</td>
      <td>80.0</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Zhen</td>
      <td>86.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>James</td>
      <td>84.0</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Coline</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Gorila</td>
      <td>52.0</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Sunny</td>
      <td>77.0</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Conner</td>
      <td>84.0</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Sally</td>
      <td>52.0</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Marry</td>
      <td>70.0</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Katy</td>
      <td>55.0</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Gerge</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>23</th>
      <td>kipling</td>
      <td>76.0</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Guggi</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



## 2. Checking missing values


```python
df1.isnull()
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
      <th>Mark</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>5</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>6</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>7</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>8</th>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>9</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>10</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>11</th>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>12</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>13</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>14</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>15</th>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>16</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>17</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>18</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>19</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>20</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>21</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>22</th>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>23</th>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>24</th>
      <td>False</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1.isnull().sum().sum()>0
```




    True




```python
df1.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 25 entries, 0 to 24
    Data columns (total 2 columns):
     #   Column  Non-Null Count  Dtype  
    ---  ------  --------------  -----  
     0   Name    25 non-null     object 
     1   Mark    19 non-null     float64
    dtypes: float64(1), object(1)
    memory usage: 528.0+ bytes
    

## 3. Imputation : fillna()


```python
df2 = df1.fillna(0)
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
      <th>Name</th>
      <th>Mark</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Louis</td>
      <td>100.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Harvey</td>
      <td>59.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>G-dragon</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Lola</td>
      <td>87.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jorge</td>
      <td>90.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Piona</td>
      <td>54.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Mitchy</td>
      <td>93.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Fibio</td>
      <td>94.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Kim</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Stacy</td>
      <td>71.0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Grace</td>
      <td>96.0</td>
    </tr>
    <tr>
      <th>11</th>
      <td>TL</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Sanchez</td>
      <td>80.0</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Zhen</td>
      <td>86.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>James</td>
      <td>84.0</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Coline</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Gorila</td>
      <td>52.0</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Sunny</td>
      <td>77.0</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Conner</td>
      <td>84.0</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Sally</td>
      <td>52.0</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Marry</td>
      <td>70.0</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Katy</td>
      <td>55.0</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Gerge</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>23</th>
      <td>kipling</td>
      <td>76.0</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Guggi</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
</div>



## 4. Deletion : dropna()


```python
df3 = df1.dropna()
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
      <th>Mark</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Louis</td>
      <td>100.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Harvey</td>
      <td>59.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Lola</td>
      <td>87.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jorge</td>
      <td>90.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Piona</td>
      <td>54.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Mitchy</td>
      <td>93.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Fibio</td>
      <td>94.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Stacy</td>
      <td>71.0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Grace</td>
      <td>96.0</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Sanchez</td>
      <td>80.0</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Zhen</td>
      <td>86.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>James</td>
      <td>84.0</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Gorila</td>
      <td>52.0</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Sunny</td>
      <td>77.0</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Conner</td>
      <td>84.0</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Sally</td>
      <td>52.0</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Marry</td>
      <td>70.0</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Katy</td>
      <td>55.0</td>
    </tr>
    <tr>
      <th>23</th>
      <td>kipling</td>
      <td>76.0</td>
    </tr>
  </tbody>
</table>
</div>



## 5. Coppy to clipboard : to_clipboard()


```python
df2.to_clipboard(index=False)
```


```python
df3.to_clipboard(index=False)
```

## 6. Total code


```python
import pandas as pd

df1 = pd.read_excel("E04EXAMPLE.xlsx", sheet_name=1)
df2 = df1.fillna(0)
df3 = df1.dropna()

df2.to_clipboard(index=False)
df3.to_clipboard(index=False)
```
