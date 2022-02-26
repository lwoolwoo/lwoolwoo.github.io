---
layout: single
title:  "Practice #9 Sort_values"
---



```python
import pandas as pd 
```


```python
df1 = pd.read_excel("E10EXAMPLE.xlsx", sheet_name=0)
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
      <th>Age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Louis</td>
      <td>100</td>
      <td>34.5</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Harvey</td>
      <td>100</td>
      <td>61.4</td>
    </tr>
    <tr>
      <th>2</th>
      <td>G-dragon</td>
      <td>89</td>
      <td>62.5</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Lola</td>
      <td>76</td>
      <td>60.3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jorge</td>
      <td>62</td>
      <td>20.5</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Piona</td>
      <td>79</td>
      <td>64.2</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Mitchy</td>
      <td>69</td>
      <td>37.8</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Fibio</td>
      <td>78</td>
      <td>49.8</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Kim</td>
      <td>71</td>
      <td>48.9</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Stacy</td>
      <td>74</td>
      <td>22.9</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Grace</td>
      <td>88</td>
      <td>30.4</td>
    </tr>
    <tr>
      <th>11</th>
      <td>TL</td>
      <td>67</td>
      <td>63.1</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Sanchez</td>
      <td>68</td>
      <td>57.2</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Zhen</td>
      <td>71</td>
      <td>42.2</td>
    </tr>
    <tr>
      <th>14</th>
      <td>James</td>
      <td>89</td>
      <td>28.8</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Coline</td>
      <td>98</td>
      <td>22.2</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Gorila</td>
      <td>87</td>
      <td>67.7</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Sunny</td>
      <td>96</td>
      <td>46.1</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Conner</td>
      <td>61</td>
      <td>54.2</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Sally</td>
      <td>95</td>
      <td>55.4</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Marry</td>
      <td>70</td>
      <td>36.4</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Katy</td>
      <td>80</td>
      <td>23.4</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Gerge</td>
      <td>84</td>
      <td>68.8</td>
    </tr>
    <tr>
      <th>23</th>
      <td>kipling</td>
      <td>74</td>
      <td>58.8</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Guggi</td>
      <td>99</td>
      <td>28.4</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Phil</td>
      <td>97</td>
      <td>40.2</td>
    </tr>
    <tr>
      <th>26</th>
      <td>CoolJ</td>
      <td>83</td>
      <td>30.5</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Kara</td>
      <td>93</td>
      <td>47.5</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Tiara</td>
      <td>61</td>
      <td>25.9</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Kolon</td>
      <td>99</td>
      <td>27.2</td>
    </tr>
    <tr>
      <th>30</th>
      <td>SungGil</td>
      <td>71</td>
      <td>53.5</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1["Sort"] = df1["Age"].mask(df1["Age"]<60,0)
df1 = df1.sort_values(["Mark", "Sort", "Age"], ascending=[0, 0,1])
df1.drop("Sort", axis=1).to_clipboard(index=False)
```

## Total Code


```python
import pandas as pd
df1 = pd.read_excel("E10EXAMPLE.xlsx")
df1["Sort"] = df1["Age"].mask(df1["Age"] < 60, 0)
df1 = df1.sort_values(["Mark", "Sort", "Age"], ascending= [0,0,1])
df1.drop("Sort", axis=1).to_clipboard(index=False)
```
