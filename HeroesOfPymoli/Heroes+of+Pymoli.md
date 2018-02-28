

```python
import pandas as pd
import numpy as np
```

# this is a comment


```python
#Read in json file and review data
file_name = 'purchase_data.json'
purchase_data_df = pd.read_json(file_name)
purchase_data_df#.head()

```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Age</th>
      <th>Gender</th>
      <th>Item ID</th>
      <th>Item Name</th>
      <th>Price</th>
      <th>SN</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>20</td>
      <td>Male</td>
      <td>93</td>
      <td>Apocalyptic Battlescythe</td>
      <td>4.49</td>
      <td>Iloni35</td>
    </tr>
    <tr>
      <th>1</th>
      <td>21</td>
      <td>Male</td>
      <td>12</td>
      <td>Dawne</td>
      <td>3.36</td>
      <td>Aidaira26</td>
    </tr>
    <tr>
      <th>2</th>
      <td>17</td>
      <td>Male</td>
      <td>5</td>
      <td>Putrid Fan</td>
      <td>2.63</td>
      <td>Irim47</td>
    </tr>
    <tr>
      <th>3</th>
      <td>17</td>
      <td>Male</td>
      <td>123</td>
      <td>Twilight's Carver</td>
      <td>2.55</td>
      <td>Irith83</td>
    </tr>
    <tr>
      <th>4</th>
      <td>22</td>
      <td>Male</td>
      <td>154</td>
      <td>Feral Katana</td>
      <td>4.11</td>
      <td>Philodil43</td>
    </tr>
    <tr>
      <th>5</th>
      <td>8</td>
      <td>Male</td>
      <td>8</td>
      <td>Purgatory, Gem of Regret</td>
      <td>2.22</td>
      <td>Hainaria90</td>
    </tr>
    <tr>
      <th>6</th>
      <td>40</td>
      <td>Male</td>
      <td>148</td>
      <td>Warmonger, Gift of Suffering's End</td>
      <td>4.65</td>
      <td>Aerithllora36</td>
    </tr>
    <tr>
      <th>7</th>
      <td>28</td>
      <td>Male</td>
      <td>27</td>
      <td>Riddle, Tribute of Ended Dreams</td>
      <td>3.38</td>
      <td>Undirra90</td>
    </tr>
    <tr>
      <th>8</th>
      <td>18</td>
      <td>Male</td>
      <td>111</td>
      <td>Misery's End</td>
      <td>1.79</td>
      <td>Eolideu96</td>
    </tr>
    <tr>
      <th>9</th>
      <td>36</td>
      <td>Male</td>
      <td>139</td>
      <td>Mercy, Katana of Dismay</td>
      <td>4.25</td>
      <td>Aesurstilis64</td>
    </tr>
    <tr>
      <th>10</th>
      <td>24</td>
      <td>Male</td>
      <td>126</td>
      <td>Exiled Mithril Longsword</td>
      <td>1.08</td>
      <td>Jiskimsda56</td>
    </tr>
    <tr>
      <th>11</th>
      <td>36</td>
      <td>Female</td>
      <td>173</td>
      <td>Stormfury Longsword</td>
      <td>4.01</td>
      <td>Jiskim75</td>
    </tr>
    <tr>
      <th>12</th>
      <td>20</td>
      <td>Female</td>
      <td>90</td>
      <td>Betrayer</td>
      <td>4.12</td>
      <td>Lirtassa77</td>
    </tr>
    <tr>
      <th>13</th>
      <td>32</td>
      <td>Male</td>
      <td>23</td>
      <td>Crucifer</td>
      <td>1.62</td>
      <td>Hairith93</td>
    </tr>
    <tr>
      <th>14</th>
      <td>8</td>
      <td>Male</td>
      <td>44</td>
      <td>Bonecarvin Battle Axe</td>
      <td>4.36</td>
      <td>Yarith71</td>
    </tr>
    <tr>
      <th>15</th>
      <td>23</td>
      <td>Male</td>
      <td>94</td>
      <td>Mourning Blade</td>
      <td>3.64</td>
      <td>Sondim43</td>
    </tr>
    <tr>
      <th>16</th>
      <td>24</td>
      <td>Male</td>
      <td>174</td>
      <td>Primitive Blade</td>
      <td>1.36</td>
      <td>Zhisrisu83</td>
    </tr>
    <tr>
      <th>17</th>
      <td>9</td>
      <td>Male</td>
      <td>156</td>
      <td>Soul-Forged Steel Shortsword</td>
      <td>4.53</td>
      <td>Rarallo90</td>
    </tr>
    <tr>
      <th>18</th>
      <td>12</td>
      <td>Other / Non-Disclosed</td>
      <td>176</td>
      <td>Relentless Iron Skewer</td>
      <td>2.12</td>
      <td>Inadeu25</td>
    </tr>
    <tr>
      <th>19</th>
      <td>23</td>
      <td>Male</td>
      <td>154</td>
      <td>Feral Katana</td>
      <td>4.11</td>
      <td>Haerithp41</td>
    </tr>
    <tr>
      <th>20</th>
      <td>35</td>
      <td>Male</td>
      <td>10</td>
      <td>Sleepwalker</td>
      <td>1.81</td>
      <td>Streural92</td>
    </tr>
    <tr>
      <th>21</th>
      <td>11</td>
      <td>Male</td>
      <td>131</td>
      <td>Fury</td>
      <td>2.99</td>
      <td>Eoralphos86</td>
    </tr>
    <tr>
      <th>22</th>
      <td>16</td>
      <td>Male</td>
      <td>172</td>
      <td>Blade of the Grave</td>
      <td>2.71</td>
      <td>Shaidanu32</td>
    </tr>
    <tr>
      <th>23</th>
      <td>20</td>
      <td>Male</td>
      <td>158</td>
      <td>Darkheart, Butcher of the Champion</td>
      <td>1.94</td>
      <td>Lassimla92</td>
    </tr>
    <tr>
      <th>24</th>
      <td>23</td>
      <td>Male</td>
      <td>70</td>
      <td>Hope's End</td>
      <td>4.28</td>
      <td>Heosurnuru52</td>
    </tr>
    <tr>
      <th>25</th>
      <td>17</td>
      <td>Male</td>
      <td>71</td>
      <td>Demise</td>
      <td>3.09</td>
      <td>Ilara98</td>
    </tr>
    <tr>
      <th>26</th>
      <td>7</td>
      <td>Male</td>
      <td>98</td>
      <td>Deadline, Voice Of Subtlety</td>
      <td>1.29</td>
      <td>Lirtistanya48</td>
    </tr>
    <tr>
      <th>27</th>
      <td>25</td>
      <td>Male</td>
      <td>117</td>
      <td>Heartstriker, Legacy of the Light</td>
      <td>4.71</td>
      <td>Sundaky74</td>
    </tr>
    <tr>
      <th>28</th>
      <td>20</td>
      <td>Female</td>
      <td>170</td>
      <td>Shadowsteel</td>
      <td>1.74</td>
      <td>Sondassasya91</td>
    </tr>
    <tr>
      <th>29</th>
      <td>21</td>
      <td>Male</td>
      <td>90</td>
      <td>Betrayer</td>
      <td>4.12</td>
      <td>Arithllorin55</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>48</th>
      <td>25</td>
      <td>Male</td>
      <td>84</td>
      <td>Arcane Gem</td>
      <td>4.81</td>
      <td>Eusty71</td>
    </tr>
    <tr>
      <th>49</th>
      <td>20</td>
      <td>Male</td>
      <td>14</td>
      <td>Possessed Core</td>
      <td>2.82</td>
      <td>Frichilsa31</td>
    </tr>
    <tr>
      <th>50</th>
      <td>23</td>
      <td>Male</td>
      <td>176</td>
      <td>Relentless Iron Skewer</td>
      <td>2.12</td>
      <td>Filon68</td>
    </tr>
    <tr>
      <th>51</th>
      <td>28</td>
      <td>Male</td>
      <td>1</td>
      <td>Crucifer</td>
      <td>3.67</td>
      <td>Palyon91</td>
    </tr>
    <tr>
      <th>52</th>
      <td>23</td>
      <td>Female</td>
      <td>118</td>
      <td>Ghost Reaver, Longsword of Magic</td>
      <td>2.95</td>
      <td>Assistast50</td>
    </tr>
    <tr>
      <th>53</th>
      <td>16</td>
      <td>Female</td>
      <td>94</td>
      <td>Mourning Blade</td>
      <td>3.64</td>
      <td>Seostylis96</td>
    </tr>
    <tr>
      <th>54</th>
      <td>25</td>
      <td>Male</td>
      <td>111</td>
      <td>Misery's End</td>
      <td>1.79</td>
      <td>Iskadar31</td>
    </tr>
    <tr>
      <th>55</th>
      <td>20</td>
      <td>Male</td>
      <td>108</td>
      <td>Extraction, Quickblade Of Trembling Hands</td>
      <td>2.26</td>
      <td>Pheodaisun84</td>
    </tr>
    <tr>
      <th>56</th>
      <td>17</td>
      <td>Male</td>
      <td>79</td>
      <td>Alpha, Oath of Zeal</td>
      <td>1.31</td>
      <td>Yarmol79</td>
    </tr>
    <tr>
      <th>57</th>
      <td>23</td>
      <td>Female</td>
      <td>107</td>
      <td>Splitter, Foe Of Subtlety</td>
      <td>4.15</td>
      <td>Aeri79</td>
    </tr>
    <tr>
      <th>58</th>
      <td>30</td>
      <td>Female</td>
      <td>105</td>
      <td>Hailstorm Shadowsteel Scythe</td>
      <td>1.02</td>
      <td>Undosian34</td>
    </tr>
    <tr>
      <th>59</th>
      <td>39</td>
      <td>Female</td>
      <td>2</td>
      <td>Verdict</td>
      <td>2.65</td>
      <td>Aesririam61</td>
    </tr>
    <tr>
      <th>60</th>
      <td>23</td>
      <td>Female</td>
      <td>68</td>
      <td>Storm-Weaver, Slayer of Inception</td>
      <td>4.39</td>
      <td>Firon67</td>
    </tr>
    <tr>
      <th>61</th>
      <td>21</td>
      <td>Male</td>
      <td>31</td>
      <td>Trickster</td>
      <td>4.59</td>
      <td>Jiskjask76</td>
    </tr>
    <tr>
      <th>62</th>
      <td>18</td>
      <td>Male</td>
      <td>25</td>
      <td>Hero Cane</td>
      <td>4.78</td>
      <td>Chanirra64</td>
    </tr>
    <tr>
      <th>63</th>
      <td>11</td>
      <td>Female</td>
      <td>41</td>
      <td>Orbit</td>
      <td>3.85</td>
      <td>Isristira52</td>
    </tr>
    <tr>
      <th>64</th>
      <td>24</td>
      <td>Male</td>
      <td>164</td>
      <td>Exiled Doomblade</td>
      <td>1.31</td>
      <td>Chaniman66</td>
    </tr>
    <tr>
      <th>65</th>
      <td>23</td>
      <td>Male</td>
      <td>181</td>
      <td>Reaper's Toll</td>
      <td>4.12</td>
      <td>Yarithrgue83</td>
    </tr>
    <tr>
      <th>66</th>
      <td>24</td>
      <td>Male</td>
      <td>4</td>
      <td>Bloodlord's Fetish</td>
      <td>1.91</td>
      <td>Airi27</td>
    </tr>
    <tr>
      <th>67</th>
      <td>22</td>
      <td>Male</td>
      <td>94</td>
      <td>Mourning Blade</td>
      <td>3.64</td>
      <td>Undilsan50</td>
    </tr>
    <tr>
      <th>68</th>
      <td>21</td>
      <td>Male</td>
      <td>82</td>
      <td>Nirvana</td>
      <td>1.77</td>
      <td>Aidaira26</td>
    </tr>
    <tr>
      <th>69</th>
      <td>34</td>
      <td>Male</td>
      <td>126</td>
      <td>Exiled Mithril Longsword</td>
      <td>1.08</td>
      <td>Chamalo71</td>
    </tr>
    <tr>
      <th>70</th>
      <td>25</td>
      <td>Male</td>
      <td>98</td>
      <td>Deadline, Voice Of Subtlety</td>
      <td>1.29</td>
      <td>Undadar97</td>
    </tr>
    <tr>
      <th>71</th>
      <td>25</td>
      <td>Male</td>
      <td>60</td>
      <td>Wolf</td>
      <td>2.70</td>
      <td>Sundaky74</td>
    </tr>
    <tr>
      <th>72</th>
      <td>21</td>
      <td>Male</td>
      <td>180</td>
      <td>Stormcaller</td>
      <td>2.77</td>
      <td>Lisirra44</td>
    </tr>
    <tr>
      <th>73</th>
      <td>35</td>
      <td>Male</td>
      <td>93</td>
      <td>Apocalyptic Battlescythe</td>
      <td>4.49</td>
      <td>Chamast86</td>
    </tr>
    <tr>
      <th>74</th>
      <td>38</td>
      <td>Male</td>
      <td>163</td>
      <td>Thunderfury Scimitar</td>
      <td>4.16</td>
      <td>Ardcil81</td>
    </tr>
    <tr>
      <th>75</th>
      <td>15</td>
      <td>Male</td>
      <td>167</td>
      <td>Malice, Legacy of the Queen</td>
      <td>3.25</td>
      <td>Heudai45</td>
    </tr>
    <tr>
      <th>76</th>
      <td>24</td>
      <td>Male</td>
      <td>97</td>
      <td>Swan Song, Gouger Of Terror</td>
      <td>1.92</td>
      <td>Chaniman66</td>
    </tr>
    <tr>
      <th>77</th>
      <td>20</td>
      <td>Male</td>
      <td>134</td>
      <td>Undead Crusader</td>
      <td>2.15</td>
      <td>Syalallodil59</td>
    </tr>
  </tbody>
</table>
<p>78 rows × 6 columns</p>
</div>




```python
purchase_data_df.count()
```




    Age          78
    Gender       78
    Item ID      78
    Item Name    78
    Price        78
    SN           78
    dtype: int64




```python
# Drop all rows with missing information
purchase_data_df = purchase_data_df.dropna(how='any')
```


```python
purchase_data_df.count()
```




    Age          78
    Gender       78
    Item ID      78
    Item Name    78
    Price        78
    SN           78
    dtype: int64




```python
purchase_data_df.dtypes
```




    Age            int64
    Gender        object
    Item ID        int64
    Item Name     object
    Price        float64
    SN            object
    dtype: object




```python
purchase_data_df.count()
```




    Age          78
    Gender       78
    Item ID      78
    Item Name    78
    Price        78
    SN           78
    dtype: int64




```python
# Use pd.to_numeric() method to convert the datatype of the Amount column
purchase_data_df['Price'] = pd.to_numeric(purchase_data_df['Price'])
purchase_data_df.dtypes

```




    Age            int64
    Gender        object
    Item ID        int64
    Item Name     object
    Price        float64
    SN            object
    dtype: object




```python
purchase_data_df.describe()
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Age</th>
      <th>Item ID</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>78.000000</td>
      <td>78.000000</td>
      <td>78.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>22.551282</td>
      <td>93.935897</td>
      <td>2.924359</td>
    </tr>
    <tr>
      <th>std</th>
      <td>7.339003</td>
      <td>56.352633</td>
      <td>1.134913</td>
    </tr>
    <tr>
      <th>min</th>
      <td>7.000000</td>
      <td>0.000000</td>
      <td>1.020000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>20.000000</td>
      <td>48.000000</td>
      <td>1.925000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>22.500000</td>
      <td>97.500000</td>
      <td>2.770000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>25.000000</td>
      <td>137.000000</td>
      <td>4.092500</td>
    </tr>
    <tr>
      <th>max</th>
      <td>40.000000</td>
      <td>181.000000</td>
      <td>4.810000</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Create an empty dataframe
summary_dict = [{"Blank Column": "0"}]
summary_df = pd.DataFrame(summary_dict)
summary_df
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Blank Column</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Determine the number of players
print("Player Count")
total_players = purchase_data_df.SN.nunique()
summary_df["Total Players"] = total_players 
summary_df
```

    Player Count
    




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Blank Column</th>
      <th>Total Players</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>74</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Remove original empty column 
summary_df.drop('Blank Column', axis=1, inplace=True)
```


```python
summary_df
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Total Players</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>74</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Identify the number of Unique Items 
unique_items = len(purchase_data_df.groupby(["Item ID"]))
unique_items
summary_df["Number of Unique Items"] = unique_items 
summary_df 

#df.groupby(['group'])
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Total Players</th>
      <th>Number of Unique Items</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>74</td>
      <td>64</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Calculate the Average Price
average_price = purchase_data_df["Price"].mean()

summary_df["Average Purchase Price"] = average_price
summary_df["Average Purchase Price"].map('${:,.2f}'.format)
summary_df 

#.map("${:.2f}".format)

```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Total Players</th>
      <th>Number of Unique Items</th>
      <th>Average Purchase Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>74</td>
      <td>64</td>
      <td>2.924359</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Determine the number of purchases 
Number_of_Purchases = len(purchase_data_df.groupby(["Price"]))
Number_of_Purchases 

summary_df["Number of Purchases"] = Number_of_Purchases
summary_df
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Total Players</th>
      <th>Number of Unique Items</th>
      <th>Average Purchase Price</th>
      <th>Number of Purchases</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>74</td>
      <td>64</td>
      <td>2.924359</td>
      <td>60</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Total Revenue
print("Purchasing Analysis (Total)")
Total_Revenue = purchase_data_df["Price"].sum()
Total_Revenue 
summary_df["Total Revenue"] = Total_Revenue
summary_df["Total Revenue"].map('${:,.2f}'.format)
summary_df #
```

    Purchasing Analysis (Total)
    




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Total Players</th>
      <th>Number of Unique Items</th>
      <th>Average Purchase Price</th>
      <th>Number of Purchases</th>
      <th>Total Revenue</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>74</td>
      <td>64</td>
      <td>2.924359</td>
      <td>60</td>
      <td>228.1</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Create an empty dataframe
gender_dict = [{"Blank Column": "0"}]
gender_df = pd.DataFrame(gender_dict)
gender_df
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Blank Column</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Use a groupby to get the distribution by Gender
gender_groupby = purchase_data_df.groupby(["Gender"])
gender_groupby["Gender"].count()

gender_df = pd.DataFrame(gender_groupby["Gender"].count())

gender_df 

```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Gender</th>
    </tr>
    <tr>
      <th>Gender</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Female</th>
      <td>13</td>
    </tr>
    <tr>
      <th>Male</th>
      <td>64</td>
    </tr>
    <tr>
      <th>Other / Non-Disclosed</th>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Calculate the percent of total for each Gender
print("Gender Demographics")
gender_percent_of_total_df = pd.DataFrame(gender_groupby["Gender"].count() / int(summary_df["Total Players"] ))
gender_percent_of_total_df 

gender_df["Percentage of Players"] = gender_percent_of_total_df 
gender_df

```

    Gender Demographics
    




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Gender</th>
      <th>Percentage of Players</th>
    </tr>
    <tr>
      <th>Gender</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Female</th>
      <td>13</td>
      <td>0.175676</td>
    </tr>
    <tr>
      <th>Male</th>
      <td>64</td>
      <td>0.864865</td>
    </tr>
    <tr>
      <th>Other / Non-Disclosed</th>
      <td>1</td>
      <td>0.013514</td>
    </tr>
  </tbody>
</table>
</div>




```python
#data.groupby('month')['date'].count()

gender_purchase_groupby = purchase_data_df.groupby(["Gender","Price"])
gender_purchase_df = pd.DataFrame(gender_purchase_groupby.count())
gender_purchase_df 

```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th></th>
      <th>Age</th>
      <th>Item ID</th>
      <th>Item Name</th>
      <th>SN</th>
    </tr>
    <tr>
      <th>Gender</th>
      <th>Price</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="13" valign="top">Female</th>
      <th>1.02</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1.74</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1.89</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2.26</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2.65</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2.95</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3.64</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3.85</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4.01</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4.12</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4.15</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4.39</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4.71</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th rowspan="47" valign="top">Male</th>
      <th>1.08</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1.29</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1.31</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1.34</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1.36</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1.42</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1.62</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1.77</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1.79</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1.81</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1.84</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1.91</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1.92</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1.94</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1.96</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2.12</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2.15</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2.70</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2.71</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2.77</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2.82</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2.88</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2.92</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2.99</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3.09</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3.25</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3.36</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3.38</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3.58</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3.64</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3.67</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3.75</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4.04</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4.11</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>4.12</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>4.16</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4.25</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4.28</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4.36</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4.49</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>4.53</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4.59</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4.65</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4.71</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4.78</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4.81</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Other / Non-Disclosed</th>
      <th>2.12</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>65 rows × 4 columns</p>
</div>




```python
#Get the Age
purchase_count_df = pd.DataFrame(gender_purchase_df.groupby(["Gender"]).count())
Total_Purchases = purchase_count_df["Age"]
purchase_count_df
#len(purchase_data_df.groupby(["Price"]))


```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Age</th>
      <th>Item ID</th>
      <th>Item Name</th>
      <th>SN</th>
    </tr>
    <tr>
      <th>Gender</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Female</th>
      <td>13</td>
      <td>13</td>
      <td>13</td>
      <td>13</td>
    </tr>
    <tr>
      <th>Male</th>
      <td>51</td>
      <td>51</td>
      <td>51</td>
      <td>51</td>
    </tr>
    <tr>
      <th>Other / Non-Disclosed</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Create an empty dataframe
gender_summary_dict = [{"Blank Column": "0"}]
gender_summary_df2 = pd.DataFrame(gender_summary_dict)

#Remove original empty column 
gender_summary_df2.drop('Blank Column', axis=1, inplace=True)

gender_summary_df2

```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
    </tr>
  </tbody>
</table>
</div>




```python


#gender_summary_df2[:] = 0.0
#gender_summary_df2
```


```python
# Creating a group based off of the Gender
#gender_groups = purchase_data_df.groupby("Gender")
#gender_summary_df["Purchase Count"] = pd.DataFrame(gender_groups["Gender"].count())
#gender_summary_df

#Use a groupby to get the distribution by Gender
gender_groups = purchase_data_df.groupby(["Gender"])
gender_groups["Gender"].count()

```




    Gender
    Female                   13
    Male                     64
    Other / Non-Disclosed     1
    Name: Gender, dtype: int64




```python
gender_summary_purchase_count2 = gender_groups["Gender"].count()
gender_summary_purchase_count2

#gender_summary_df 


#final_df = pd.DataFrsme({'Purchase count': })
```




    Gender
    Female                   13
    Male                     64
    Other / Non-Disclosed     1
    Name: Gender, dtype: int64




```python
#Calculate the average 
gender_avg_price = gender_groups["Price"].mean()
gender_avg_price
```




    Gender
    Female                   3.183077
    Male                     2.884375
    Other / Non-Disclosed    2.120000
    Name: Price, dtype: float64




```python


#Calculate the Total Price for an SN
gender_summary_tot_purch = gender_groups["Price"].sum()
gender_summary_tot_purch

#type(gender_summary_df)

```




    Gender
    Female                    41.38
    Male                     184.60
    Other / Non-Disclosed      2.12
    Name: Price, dtype: float64




```python
gender_summary_df_final = pd.DataFrame({'Average Purchase Price': gender_avg_price,'Total Purchase Value': gender_summary_tot_purch,'Total Purchases': gender_summary_purchase_count2})

#gender_summary_df2["Average Purchase Price"] = gender_avg_price 
#gender_summary_df2["Total Purchase Value"] = gender_summary_tot_purch 
#gender_summary_df2["Total Purchases"] = gender_summary_purchase_count2
gender_summary_df_final

```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Average Purchase Price</th>
      <th>Total Purchase Value</th>
      <th>Total Purchases</th>
    </tr>
    <tr>
      <th>Gender</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Female</th>
      <td>3.183077</td>
      <td>41.38</td>
      <td>13</td>
    </tr>
    <tr>
      <th>Male</th>
      <td>2.884375</td>
      <td>184.60</td>
      <td>64</td>
    </tr>
    <tr>
      <th>Other / Non-Disclosed</th>
      <td>2.120000</td>
      <td>2.12</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Calculate the Normalized Value 
df_gender_summary_norm = (gender_summary_df_final["Total Purchase Value"] - gender_summary_df_final["Total Purchase Value"].mean()) / (gender_summary_df_final["Total Purchase Value"].max() - gender_summary_df_final["Total Purchase Value"].min())
df_gender_summary_norm

gender_summary_df_final["Normalized Totals"] = df_gender_summary_norm
gender_summary_df_final

```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Average Purchase Price</th>
      <th>Total Purchase Value</th>
      <th>Total Purchases</th>
      <th>Normalized Totals</th>
    </tr>
    <tr>
      <th>Gender</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Female</th>
      <td>3.183077</td>
      <td>41.38</td>
      <td>13</td>
      <td>-0.189902</td>
    </tr>
    <tr>
      <th>Male</th>
      <td>2.884375</td>
      <td>184.60</td>
      <td>64</td>
      <td>0.594951</td>
    </tr>
    <tr>
      <th>Other / Non-Disclosed</th>
      <td>2.120000</td>
      <td>2.12</td>
      <td>1</td>
      <td>-0.405049</td>
    </tr>
  </tbody>
</table>
</div>




```python
 

#Add the Mean and Total Purchase to the SN Summary Dataframe

print("Purchasing Analysis (Gender)") 

gender_summary_df_final.loc[:,["Purchase Count","Average Purchase Price",
                               "Total Purchase Value","Normalized Totals"]]
gender_summary_df_final
```

    Purchasing Analysis (Gender)
    




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Average Purchase Price</th>
      <th>Total Purchase Value</th>
      <th>Total Purchases</th>
      <th>Normalized Totals</th>
    </tr>
    <tr>
      <th>Gender</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Female</th>
      <td>3.183077</td>
      <td>41.38</td>
      <td>13</td>
      <td>-0.189902</td>
    </tr>
    <tr>
      <th>Male</th>
      <td>2.884375</td>
      <td>184.60</td>
      <td>64</td>
      <td>0.594951</td>
    </tr>
    <tr>
      <th>Other / Non-Disclosed</th>
      <td>2.120000</td>
      <td>2.12</td>
      <td>1</td>
      <td>-0.405049</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Calculate the Sum 
gender_purchase_df.groupby("Gender").sum()
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Age</th>
      <th>Item ID</th>
      <th>Item Name</th>
      <th>SN</th>
    </tr>
    <tr>
      <th>Gender</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Female</th>
      <td>13</td>
      <td>13</td>
      <td>13</td>
      <td>13</td>
    </tr>
    <tr>
      <th>Male</th>
      <td>64</td>
      <td>64</td>
      <td>64</td>
      <td>64</td>
    </tr>
    <tr>
      <th>Other / Non-Disclosed</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Create an age dataframe using a groupby
age_df = pd.DataFrame(purchase_data_df.groupby("Age").count())
age_df


```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Gender</th>
      <th>Item ID</th>
      <th>Item Name</th>
      <th>Price</th>
      <th>SN</th>
    </tr>
    <tr>
      <th>Age</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>7</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>8</th>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
    </tr>
    <tr>
      <th>9</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>11</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>12</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>15</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16</th>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
    </tr>
    <tr>
      <th>17</th>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>5</td>
    </tr>
    <tr>
      <th>18</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>20</th>
      <td>10</td>
      <td>10</td>
      <td>10</td>
      <td>10</td>
      <td>10</td>
    </tr>
    <tr>
      <th>21</th>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
    </tr>
    <tr>
      <th>22</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>23</th>
      <td>9</td>
      <td>9</td>
      <td>9</td>
      <td>9</td>
      <td>9</td>
    </tr>
    <tr>
      <th>24</th>
      <td>7</td>
      <td>7</td>
      <td>7</td>
      <td>7</td>
      <td>7</td>
    </tr>
    <tr>
      <th>25</th>
      <td>7</td>
      <td>7</td>
      <td>7</td>
      <td>7</td>
      <td>7</td>
    </tr>
    <tr>
      <th>28</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>30</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>32</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>33</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>34</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>35</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>36</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>38</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>40</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Create Bins and lables to separate the ages into bins 
#Add Age Summary column to identify which bin each row belongs 
bins = [0, 10, 14, 19, 24, 29,34,39,40]

# Create the names for the four bins
group_names = ['<10', '10-14', '15-19', '20-24','25-29','30-34','35-39','40+']
# Cut postTestScore and place the scores into bins
purchase_data_df["Age Summary"] = pd.cut(purchase_data_df["Age"], bins, labels=group_names)
purchase_data_df.head()
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Age</th>
      <th>Gender</th>
      <th>Item ID</th>
      <th>Item Name</th>
      <th>Price</th>
      <th>SN</th>
      <th>Age Summary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>20</td>
      <td>Male</td>
      <td>93</td>
      <td>Apocalyptic Battlescythe</td>
      <td>4.49</td>
      <td>Iloni35</td>
      <td>20-24</td>
    </tr>
    <tr>
      <th>1</th>
      <td>21</td>
      <td>Male</td>
      <td>12</td>
      <td>Dawne</td>
      <td>3.36</td>
      <td>Aidaira26</td>
      <td>20-24</td>
    </tr>
    <tr>
      <th>2</th>
      <td>17</td>
      <td>Male</td>
      <td>5</td>
      <td>Putrid Fan</td>
      <td>2.63</td>
      <td>Irim47</td>
      <td>15-19</td>
    </tr>
    <tr>
      <th>3</th>
      <td>17</td>
      <td>Male</td>
      <td>123</td>
      <td>Twilight's Carver</td>
      <td>2.55</td>
      <td>Irith83</td>
      <td>15-19</td>
    </tr>
    <tr>
      <th>4</th>
      <td>22</td>
      <td>Male</td>
      <td>154</td>
      <td>Feral Katana</td>
      <td>4.11</td>
      <td>Philodil43</td>
      <td>20-24</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Creating a group based off of the bins
print("Age Demographics")
age_groups = purchase_data_df.groupby("Age Summary")
age_summary_df = pd.DataFrame(age_groups["Age Summary"].count())
age_summary_df

```

    Age Demographics
    




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Age Summary</th>
    </tr>
    <tr>
      <th>Age Summary</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>&lt;10</th>
      <td>5</td>
    </tr>
    <tr>
      <th>10-14</th>
      <td>3</td>
    </tr>
    <tr>
      <th>15-19</th>
      <td>11</td>
    </tr>
    <tr>
      <th>20-24</th>
      <td>36</td>
    </tr>
    <tr>
      <th>25-29</th>
      <td>9</td>
    </tr>
    <tr>
      <th>30-34</th>
      <td>7</td>
    </tr>
    <tr>
      <th>35-39</th>
      <td>6</td>
    </tr>
    <tr>
      <th>40+</th>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>




```python
# How many rows the dataset
#Calculate the Percent of Total
age_summary_df["Percent of Total"] = (age_groups["Age Summary"].count())/purchase_data_df['Age Summary'].count()
age_summary_df.style.format("{:.2%}")
age_summary_df 

```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Age Summary</th>
      <th>Percent of Total</th>
    </tr>
    <tr>
      <th>Age Summary</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>&lt;10</th>
      <td>5</td>
      <td>0.064103</td>
    </tr>
    <tr>
      <th>10-14</th>
      <td>3</td>
      <td>0.038462</td>
    </tr>
    <tr>
      <th>15-19</th>
      <td>11</td>
      <td>0.141026</td>
    </tr>
    <tr>
      <th>20-24</th>
      <td>36</td>
      <td>0.461538</td>
    </tr>
    <tr>
      <th>25-29</th>
      <td>9</td>
      <td>0.115385</td>
    </tr>
    <tr>
      <th>30-34</th>
      <td>7</td>
      <td>0.089744</td>
    </tr>
    <tr>
      <th>35-39</th>
      <td>6</td>
      <td>0.076923</td>
    </tr>
    <tr>
      <th>40+</th>
      <td>1</td>
      <td>0.012821</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Calculate Mean and Sum of Age Groups and add them to the Age Summary Dataframe
age_summary_avg_price = age_groups["Price"].mean()
age_summary_avg_price 

age_summary_tot_purch = age_groups["Price"].sum()
age_summary_tot_purch

age_summary_purch_count = age_summary_df["Age Summary"]

age_summary_df["Purchase Count"] =  age_summary_purch_count 

age_summary_df["Average Purchase Price"] = age_summary_avg_price 
age_summary_df["Total Purchase Value"] = age_summary_tot_purch 

age_summary_df.head()


```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Age Summary</th>
      <th>Percent of Total</th>
      <th>Purchase Count</th>
      <th>Average Purchase Price</th>
      <th>Total Purchase Value</th>
    </tr>
    <tr>
      <th>Age Summary</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>&lt;10</th>
      <td>5</td>
      <td>0.064103</td>
      <td>5</td>
      <td>2.764000</td>
      <td>13.82</td>
    </tr>
    <tr>
      <th>10-14</th>
      <td>3</td>
      <td>0.038462</td>
      <td>3</td>
      <td>2.986667</td>
      <td>8.96</td>
    </tr>
    <tr>
      <th>15-19</th>
      <td>11</td>
      <td>0.141026</td>
      <td>11</td>
      <td>2.764545</td>
      <td>30.41</td>
    </tr>
    <tr>
      <th>20-24</th>
      <td>36</td>
      <td>0.461538</td>
      <td>36</td>
      <td>3.024722</td>
      <td>108.89</td>
    </tr>
    <tr>
      <th>25-29</th>
      <td>9</td>
      <td>0.115385</td>
      <td>9</td>
      <td>2.901111</td>
      <td>26.11</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Calculate the Normalized Value 
df_age_summary_norm = (age_summary_df["Total Purchase Value"] - age_summary_df["Total Purchase Value"].mean()) / (age_summary_df["Total Purchase Value"].max() - age_summary_df["Total Purchase Value"].min())
df_age_summary_norm

print("Purchasing Analysis Age")

age_summary_df["Normalized Totals"] = df_age_summary_norm
age_summary_df.loc[:,["Purchase Count","Average Purchase Price","Total Purchase Value","Normalized Totals"]]


```

    Purchasing Analysis Age
    




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Purchase Count</th>
      <th>Average Purchase Price</th>
      <th>Total Purchase Value</th>
      <th>Normalized Totals</th>
    </tr>
    <tr>
      <th>Age Summary</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>&lt;10</th>
      <td>5</td>
      <td>2.764000</td>
      <td>13.82</td>
      <td>-0.140949</td>
    </tr>
    <tr>
      <th>10-14</th>
      <td>3</td>
      <td>2.986667</td>
      <td>8.96</td>
      <td>-0.187572</td>
    </tr>
    <tr>
      <th>15-19</th>
      <td>11</td>
      <td>2.764545</td>
      <td>30.41</td>
      <td>0.018203</td>
    </tr>
    <tr>
      <th>20-24</th>
      <td>36</td>
      <td>3.024722</td>
      <td>108.89</td>
      <td>0.771081</td>
    </tr>
    <tr>
      <th>25-29</th>
      <td>9</td>
      <td>2.901111</td>
      <td>26.11</td>
      <td>-0.023048</td>
    </tr>
    <tr>
      <th>30-34</th>
      <td>7</td>
      <td>1.984286</td>
      <td>13.89</td>
      <td>-0.140277</td>
    </tr>
    <tr>
      <th>35-39</th>
      <td>6</td>
      <td>3.561667</td>
      <td>21.37</td>
      <td>-0.068520</td>
    </tr>
    <tr>
      <th>40+</th>
      <td>1</td>
      <td>4.650000</td>
      <td>4.65</td>
      <td>-0.228919</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Creating a group based off of the SN 
SN_groups = purchase_data_df.groupby("SN")
SN_summary_df = pd.DataFrame(SN_groups["SN"].count())
SN_summary_df

```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>SN</th>
    </tr>
    <tr>
      <th>SN</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Aeri79</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Aerithllora36</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Aesririam61</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Aesurstilis64</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Aidaira26</th>
      <td>2</td>
    </tr>
    <tr>
      <th>Aiduecal76</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Airi27</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Airithrin43</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Alarap40</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Ardcil81</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Arithllorin55</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Assistast50</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Chamalo71</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Chamast86</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Chamjaskya75</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Chaniman66</th>
      <td>2</td>
    </tr>
    <tr>
      <th>Chanirra64</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Chanjasksda31</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Chrathybust28</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Eolideu96</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Eollym91</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Eoralphos86</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Ethralan59</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Eusty71</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Eustyria89</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Filon68</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Firon67</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Frichilsa31</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Haerithp41</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Hainaria90</th>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th>Jiskimsda56</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Jiskjask76</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Lassimla92</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Lirtassa77</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Lirtastan49</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Lirtistanya48</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Lisirra44</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Lisosiast26</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Palyon91</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Pharithdil38</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Pheodaisun84</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Philodil43</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Rarallo90</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Saralp86</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Seostylis96</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Shaidanu32</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Sondassasya91</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Sondim43</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Streural92</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Sundaky74</th>
      <td>2</td>
    </tr>
    <tr>
      <th>Syalallodil59</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Undadar97</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Undilsan50</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Undirra90</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Undirrasta74</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Undosian34</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Yarith71</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Yarithrgue83</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Yarmol79</th>
      <td>1</td>
    </tr>
    <tr>
      <th>Zhisrisu83</th>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>74 rows × 1 columns</p>
</div>




```python
#Calculate the Mean Price for a SN 
SN_summary_avg_price = SN_groups["Price"].mean()
SN_summary_avg_price 


```




    SN
    Aeri79           4.150
    Aerithllora36    4.650
    Aesririam61      2.650
    Aesurstilis64    4.250
    Aidaira26        2.565
    Aiduecal76       1.420
    Airi27           1.910
    Airithrin43      2.260
    Alarap40         4.710
    Ardcil81         4.160
    Arithllorin55    4.120
    Assistast50      2.950
    Chamalo71        1.080
    Chamast86        4.490
    Chamjaskya75     2.770
    Chaniman66       1.615
    Chanirra64       4.780
    Chanjasksda31    1.960
    Chrathybust28    2.150
    Eolideu96        1.790
    Eollym91         3.750
    Eoralphos86      2.990
    Ethralan59       2.880
    Eusty71          4.810
    Eustyria89       2.700
    Filon68          2.120
    Firon67          4.390
    Frichilsa31      2.820
    Haerithp41       4.110
    Hainaria90       2.220
                     ...  
    Jiskimsda56      1.080
    Jiskjask76       4.590
    Lassimla92       1.940
    Lirtassa77       4.120
    Lirtastan49      1.340
    Lirtistanya48    1.290
    Lisirra44        2.770
    Lisosiast26      3.580
    Palyon91         3.670
    Pharithdil38     1.890
    Pheodaisun84     2.260
    Philodil43       4.110
    Rarallo90        4.530
    Saralp86         2.420
    Seostylis96      3.640
    Shaidanu32       2.710
    Sondassasya91    1.740
    Sondim43         3.640
    Streural92       1.810
    Sundaky74        3.705
    Syalallodil59    2.150
    Undadar97        1.290
    Undilsan50       3.640
    Undirra90        3.380
    Undirrasta74     2.420
    Undosian34       1.020
    Yarith71         4.360
    Yarithrgue83     4.120
    Yarmol79         1.310
    Zhisrisu83       1.360
    Name: Price, Length: 74, dtype: float64




```python
#Calculate the Total Price for an SN
SN_summary_tot_purch = SN_groups["Price"].sum()
SN_summary_tot_purch

```




    SN
    Aeri79           4.15
    Aerithllora36    4.65
    Aesririam61      2.65
    Aesurstilis64    4.25
    Aidaira26        5.13
    Aiduecal76       1.42
    Airi27           1.91
    Airithrin43      2.26
    Alarap40         4.71
    Ardcil81         4.16
    Arithllorin55    4.12
    Assistast50      2.95
    Chamalo71        1.08
    Chamast86        4.49
    Chamjaskya75     2.77
    Chaniman66       3.23
    Chanirra64       4.78
    Chanjasksda31    1.96
    Chrathybust28    2.15
    Eolideu96        1.79
    Eollym91         3.75
    Eoralphos86      2.99
    Ethralan59       2.88
    Eusty71          4.81
    Eustyria89       2.70
    Filon68          2.12
    Firon67          4.39
    Frichilsa31      2.82
    Haerithp41       4.11
    Hainaria90       2.22
                     ... 
    Jiskimsda56      1.08
    Jiskjask76       4.59
    Lassimla92       1.94
    Lirtassa77       4.12
    Lirtastan49      1.34
    Lirtistanya48    1.29
    Lisirra44        2.77
    Lisosiast26      3.58
    Palyon91         3.67
    Pharithdil38     1.89
    Pheodaisun84     2.26
    Philodil43       4.11
    Rarallo90        4.53
    Saralp86         2.42
    Seostylis96      3.64
    Shaidanu32       2.71
    Sondassasya91    1.74
    Sondim43         3.64
    Streural92       1.81
    Sundaky74        7.41
    Syalallodil59    2.15
    Undadar97        1.29
    Undilsan50       3.64
    Undirra90        3.38
    Undirrasta74     2.42
    Undosian34       1.02
    Yarith71         4.36
    Yarithrgue83     4.12
    Yarmol79         1.31
    Zhisrisu83       1.36
    Name: Price, Length: 74, dtype: float64




```python
#Add the Mean and Total Purchase to the SN Summary Dataframe

print("Top Spenders")
SN_summary_df["Average Purchase Price"] = SN_summary_avg_price 
SN_summary_df["Total Purchase Value"] = SN_summary_tot_purch 

SN_summary_df.nlargest(5,"Total Purchase Value")
```

    Top Spenders
    




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>SN</th>
      <th>Average Purchase Price</th>
      <th>Total Purchase Value</th>
    </tr>
    <tr>
      <th>SN</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Sundaky74</th>
      <td>2</td>
      <td>3.705</td>
      <td>7.41</td>
    </tr>
    <tr>
      <th>Aidaira26</th>
      <td>2</td>
      <td>2.565</td>
      <td>5.13</td>
    </tr>
    <tr>
      <th>Eusty71</th>
      <td>1</td>
      <td>4.810</td>
      <td>4.81</td>
    </tr>
    <tr>
      <th>Chanirra64</th>
      <td>1</td>
      <td>4.780</td>
      <td>4.78</td>
    </tr>
    <tr>
      <th>Alarap40</th>
      <td>1</td>
      <td>4.710</td>
      <td>4.71</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Creating a group based off of the Item ID 
ItemID_groups = purchase_data_df.groupby("Item ID")
ItemID_summary_df = pd.DataFrame(ItemID_groups["Item ID"].count())
ItemID_summary_df

```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Item ID</th>
    </tr>
    <tr>
      <th>Item ID</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>1</td>
    </tr>
    <tr>
      <th>6</th>
      <td>1</td>
    </tr>
    <tr>
      <th>8</th>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>1</td>
    </tr>
    <tr>
      <th>10</th>
      <td>1</td>
    </tr>
    <tr>
      <th>12</th>
      <td>1</td>
    </tr>
    <tr>
      <th>14</th>
      <td>1</td>
    </tr>
    <tr>
      <th>16</th>
      <td>1</td>
    </tr>
    <tr>
      <th>17</th>
      <td>1</td>
    </tr>
    <tr>
      <th>18</th>
      <td>1</td>
    </tr>
    <tr>
      <th>23</th>
      <td>1</td>
    </tr>
    <tr>
      <th>25</th>
      <td>1</td>
    </tr>
    <tr>
      <th>27</th>
      <td>1</td>
    </tr>
    <tr>
      <th>31</th>
      <td>1</td>
    </tr>
    <tr>
      <th>41</th>
      <td>1</td>
    </tr>
    <tr>
      <th>44</th>
      <td>1</td>
    </tr>
    <tr>
      <th>60</th>
      <td>2</td>
    </tr>
    <tr>
      <th>64</th>
      <td>2</td>
    </tr>
    <tr>
      <th>68</th>
      <td>1</td>
    </tr>
    <tr>
      <th>70</th>
      <td>1</td>
    </tr>
    <tr>
      <th>71</th>
      <td>1</td>
    </tr>
    <tr>
      <th>79</th>
      <td>1</td>
    </tr>
    <tr>
      <th>82</th>
      <td>1</td>
    </tr>
    <tr>
      <th>84</th>
      <td>1</td>
    </tr>
    <tr>
      <th>90</th>
      <td>2</td>
    </tr>
    <tr>
      <th>91</th>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th>104</th>
      <td>1</td>
    </tr>
    <tr>
      <th>105</th>
      <td>1</td>
    </tr>
    <tr>
      <th>107</th>
      <td>1</td>
    </tr>
    <tr>
      <th>108</th>
      <td>2</td>
    </tr>
    <tr>
      <th>111</th>
      <td>2</td>
    </tr>
    <tr>
      <th>117</th>
      <td>2</td>
    </tr>
    <tr>
      <th>118</th>
      <td>1</td>
    </tr>
    <tr>
      <th>123</th>
      <td>1</td>
    </tr>
    <tr>
      <th>126</th>
      <td>2</td>
    </tr>
    <tr>
      <th>127</th>
      <td>1</td>
    </tr>
    <tr>
      <th>129</th>
      <td>1</td>
    </tr>
    <tr>
      <th>131</th>
      <td>1</td>
    </tr>
    <tr>
      <th>134</th>
      <td>1</td>
    </tr>
    <tr>
      <th>138</th>
      <td>1</td>
    </tr>
    <tr>
      <th>139</th>
      <td>1</td>
    </tr>
    <tr>
      <th>148</th>
      <td>1</td>
    </tr>
    <tr>
      <th>154</th>
      <td>2</td>
    </tr>
    <tr>
      <th>155</th>
      <td>1</td>
    </tr>
    <tr>
      <th>156</th>
      <td>1</td>
    </tr>
    <tr>
      <th>158</th>
      <td>1</td>
    </tr>
    <tr>
      <th>163</th>
      <td>1</td>
    </tr>
    <tr>
      <th>164</th>
      <td>1</td>
    </tr>
    <tr>
      <th>167</th>
      <td>1</td>
    </tr>
    <tr>
      <th>170</th>
      <td>1</td>
    </tr>
    <tr>
      <th>172</th>
      <td>1</td>
    </tr>
    <tr>
      <th>173</th>
      <td>1</td>
    </tr>
    <tr>
      <th>174</th>
      <td>1</td>
    </tr>
    <tr>
      <th>176</th>
      <td>2</td>
    </tr>
    <tr>
      <th>180</th>
      <td>2</td>
    </tr>
    <tr>
      <th>181</th>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>64 rows × 1 columns</p>
</div>




```python
#Calculate the Total Purchases 
ItemID_summary_max_sum_price = ItemID_groups["Price"].sum()
ItemID_summary_max_sum_price 

ItemID_summary_df["Total Purchase Value"] = ItemID_summary_max_sum_price 

ItemID_summary_df 


```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Item ID</th>
      <th>Total Purchase Value</th>
    </tr>
    <tr>
      <th>Item ID</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>1.89</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>3.67</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>2.65</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1</td>
      <td>1.91</td>
    </tr>
    <tr>
      <th>5</th>
      <td>1</td>
      <td>2.63</td>
    </tr>
    <tr>
      <th>6</th>
      <td>1</td>
      <td>3.58</td>
    </tr>
    <tr>
      <th>8</th>
      <td>1</td>
      <td>2.22</td>
    </tr>
    <tr>
      <th>9</th>
      <td>1</td>
      <td>1.42</td>
    </tr>
    <tr>
      <th>10</th>
      <td>1</td>
      <td>1.81</td>
    </tr>
    <tr>
      <th>12</th>
      <td>1</td>
      <td>3.36</td>
    </tr>
    <tr>
      <th>14</th>
      <td>1</td>
      <td>2.82</td>
    </tr>
    <tr>
      <th>16</th>
      <td>1</td>
      <td>2.15</td>
    </tr>
    <tr>
      <th>17</th>
      <td>1</td>
      <td>1.96</td>
    </tr>
    <tr>
      <th>18</th>
      <td>1</td>
      <td>3.75</td>
    </tr>
    <tr>
      <th>23</th>
      <td>1</td>
      <td>1.62</td>
    </tr>
    <tr>
      <th>25</th>
      <td>1</td>
      <td>4.78</td>
    </tr>
    <tr>
      <th>27</th>
      <td>1</td>
      <td>3.38</td>
    </tr>
    <tr>
      <th>31</th>
      <td>1</td>
      <td>4.59</td>
    </tr>
    <tr>
      <th>41</th>
      <td>1</td>
      <td>3.85</td>
    </tr>
    <tr>
      <th>44</th>
      <td>1</td>
      <td>4.36</td>
    </tr>
    <tr>
      <th>60</th>
      <td>2</td>
      <td>5.40</td>
    </tr>
    <tr>
      <th>64</th>
      <td>2</td>
      <td>4.84</td>
    </tr>
    <tr>
      <th>68</th>
      <td>1</td>
      <td>4.39</td>
    </tr>
    <tr>
      <th>70</th>
      <td>1</td>
      <td>4.28</td>
    </tr>
    <tr>
      <th>71</th>
      <td>1</td>
      <td>3.09</td>
    </tr>
    <tr>
      <th>79</th>
      <td>1</td>
      <td>1.31</td>
    </tr>
    <tr>
      <th>82</th>
      <td>1</td>
      <td>1.77</td>
    </tr>
    <tr>
      <th>84</th>
      <td>1</td>
      <td>4.81</td>
    </tr>
    <tr>
      <th>90</th>
      <td>2</td>
      <td>8.24</td>
    </tr>
    <tr>
      <th>91</th>
      <td>1</td>
      <td>2.92</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>104</th>
      <td>1</td>
      <td>1.84</td>
    </tr>
    <tr>
      <th>105</th>
      <td>1</td>
      <td>1.02</td>
    </tr>
    <tr>
      <th>107</th>
      <td>1</td>
      <td>4.15</td>
    </tr>
    <tr>
      <th>108</th>
      <td>2</td>
      <td>4.52</td>
    </tr>
    <tr>
      <th>111</th>
      <td>2</td>
      <td>3.58</td>
    </tr>
    <tr>
      <th>117</th>
      <td>2</td>
      <td>9.42</td>
    </tr>
    <tr>
      <th>118</th>
      <td>1</td>
      <td>2.95</td>
    </tr>
    <tr>
      <th>123</th>
      <td>1</td>
      <td>2.55</td>
    </tr>
    <tr>
      <th>126</th>
      <td>2</td>
      <td>2.16</td>
    </tr>
    <tr>
      <th>127</th>
      <td>1</td>
      <td>1.34</td>
    </tr>
    <tr>
      <th>129</th>
      <td>1</td>
      <td>2.88</td>
    </tr>
    <tr>
      <th>131</th>
      <td>1</td>
      <td>2.99</td>
    </tr>
    <tr>
      <th>134</th>
      <td>1</td>
      <td>2.15</td>
    </tr>
    <tr>
      <th>138</th>
      <td>1</td>
      <td>2.63</td>
    </tr>
    <tr>
      <th>139</th>
      <td>1</td>
      <td>4.25</td>
    </tr>
    <tr>
      <th>148</th>
      <td>1</td>
      <td>4.65</td>
    </tr>
    <tr>
      <th>154</th>
      <td>2</td>
      <td>8.22</td>
    </tr>
    <tr>
      <th>155</th>
      <td>1</td>
      <td>4.04</td>
    </tr>
    <tr>
      <th>156</th>
      <td>1</td>
      <td>4.53</td>
    </tr>
    <tr>
      <th>158</th>
      <td>1</td>
      <td>1.94</td>
    </tr>
    <tr>
      <th>163</th>
      <td>1</td>
      <td>4.16</td>
    </tr>
    <tr>
      <th>164</th>
      <td>1</td>
      <td>1.31</td>
    </tr>
    <tr>
      <th>167</th>
      <td>1</td>
      <td>3.25</td>
    </tr>
    <tr>
      <th>170</th>
      <td>1</td>
      <td>1.74</td>
    </tr>
    <tr>
      <th>172</th>
      <td>1</td>
      <td>2.71</td>
    </tr>
    <tr>
      <th>173</th>
      <td>1</td>
      <td>4.01</td>
    </tr>
    <tr>
      <th>174</th>
      <td>1</td>
      <td>1.36</td>
    </tr>
    <tr>
      <th>176</th>
      <td>2</td>
      <td>4.24</td>
    </tr>
    <tr>
      <th>180</th>
      <td>2</td>
      <td>5.54</td>
    </tr>
    <tr>
      <th>181</th>
      <td>1</td>
      <td>4.12</td>
    </tr>
  </tbody>
</table>
<p>64 rows × 2 columns</p>
</div>




```python
#Identify the top 5 largest Total Purchases 
ItemID_summary_df.nlargest(5,'Total Purchase Value')


```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Item ID</th>
      <th>Total Purchase Value</th>
    </tr>
    <tr>
      <th>Item ID</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>94</th>
      <td>3</td>
      <td>10.92</td>
    </tr>
    <tr>
      <th>117</th>
      <td>2</td>
      <td>9.42</td>
    </tr>
    <tr>
      <th>93</th>
      <td>2</td>
      <td>8.98</td>
    </tr>
    <tr>
      <th>90</th>
      <td>2</td>
      <td>8.24</td>
    </tr>
    <tr>
      <th>154</th>
      <td>2</td>
      <td>8.22</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Identify the top 5 most popular based on number of times item was purchased 
ItemID_summary_df=ItemID_summary_df.rename(columns = {'Item ID':'Purchase Count'})
ItemID_summary_df.nlargest(5,'Purchase Count')

    
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Purchase Count</th>
      <th>Total Purchase Value</th>
    </tr>
    <tr>
      <th>Item ID</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>94</th>
      <td>3</td>
      <td>10.92</td>
    </tr>
    <tr>
      <th>60</th>
      <td>2</td>
      <td>5.40</td>
    </tr>
    <tr>
      <th>64</th>
      <td>2</td>
      <td>4.84</td>
    </tr>
    <tr>
      <th>90</th>
      <td>2</td>
      <td>8.24</td>
    </tr>
    <tr>
      <th>93</th>
      <td>2</td>
      <td>8.98</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Add Item Name to ItemID Summary Dataframe
ItemID_summary_df["Item Name"] = purchase_data_df["Item Name"]
ItemID_summary_df 


```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Purchase Count</th>
      <th>Total Purchase Value</th>
      <th>Item Name</th>
    </tr>
    <tr>
      <th>Item ID</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>1.89</td>
      <td>Apocalyptic Battlescythe</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>3.67</td>
      <td>Dawne</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>2.65</td>
      <td>Putrid Fan</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1</td>
      <td>1.91</td>
      <td>Feral Katana</td>
    </tr>
    <tr>
      <th>5</th>
      <td>1</td>
      <td>2.63</td>
      <td>Purgatory, Gem of Regret</td>
    </tr>
    <tr>
      <th>6</th>
      <td>1</td>
      <td>3.58</td>
      <td>Warmonger, Gift of Suffering's End</td>
    </tr>
    <tr>
      <th>8</th>
      <td>1</td>
      <td>2.22</td>
      <td>Misery's End</td>
    </tr>
    <tr>
      <th>9</th>
      <td>1</td>
      <td>1.42</td>
      <td>Mercy, Katana of Dismay</td>
    </tr>
    <tr>
      <th>10</th>
      <td>1</td>
      <td>1.81</td>
      <td>Exiled Mithril Longsword</td>
    </tr>
    <tr>
      <th>12</th>
      <td>1</td>
      <td>3.36</td>
      <td>Betrayer</td>
    </tr>
    <tr>
      <th>14</th>
      <td>1</td>
      <td>2.82</td>
      <td>Bonecarvin Battle Axe</td>
    </tr>
    <tr>
      <th>16</th>
      <td>1</td>
      <td>2.15</td>
      <td>Primitive Blade</td>
    </tr>
    <tr>
      <th>17</th>
      <td>1</td>
      <td>1.96</td>
      <td>Soul-Forged Steel Shortsword</td>
    </tr>
    <tr>
      <th>18</th>
      <td>1</td>
      <td>3.75</td>
      <td>Relentless Iron Skewer</td>
    </tr>
    <tr>
      <th>23</th>
      <td>1</td>
      <td>1.62</td>
      <td>Darkheart, Butcher of the Champion</td>
    </tr>
    <tr>
      <th>25</th>
      <td>1</td>
      <td>4.78</td>
      <td>Demise</td>
    </tr>
    <tr>
      <th>27</th>
      <td>1</td>
      <td>3.38</td>
      <td>Heartstriker, Legacy of the Light</td>
    </tr>
    <tr>
      <th>31</th>
      <td>1</td>
      <td>4.59</td>
      <td>Fate, Vengeance of Eternal Justice</td>
    </tr>
    <tr>
      <th>41</th>
      <td>1</td>
      <td>3.85</td>
      <td>Heartseeker, Reaver of Souls</td>
    </tr>
    <tr>
      <th>44</th>
      <td>1</td>
      <td>4.36</td>
      <td>Fusion Pummel</td>
    </tr>
    <tr>
      <th>60</th>
      <td>2</td>
      <td>5.40</td>
      <td>Storm-Weaver, Slayer of Inception</td>
    </tr>
    <tr>
      <th>64</th>
      <td>2</td>
      <td>4.84</td>
      <td>Exiled Doomblade</td>
    </tr>
    <tr>
      <th>68</th>
      <td>1</td>
      <td>4.39</td>
      <td>Nirvana</td>
    </tr>
    <tr>
      <th>70</th>
      <td>1</td>
      <td>4.28</td>
      <td>Deadline, Voice Of Subtlety</td>
    </tr>
    <tr>
      <th>71</th>
      <td>1</td>
      <td>3.09</td>
      <td>Wolf</td>
    </tr>
    <tr>
      <th>79</th>
      <td>1</td>
      <td>1.31</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>82</th>
      <td>1</td>
      <td>1.77</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>84</th>
      <td>1</td>
      <td>4.81</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>90</th>
      <td>2</td>
      <td>8.24</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>91</th>
      <td>1</td>
      <td>2.92</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>104</th>
      <td>1</td>
      <td>1.84</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>105</th>
      <td>1</td>
      <td>1.02</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>107</th>
      <td>1</td>
      <td>4.15</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>108</th>
      <td>2</td>
      <td>4.52</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>111</th>
      <td>2</td>
      <td>3.58</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>117</th>
      <td>2</td>
      <td>9.42</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>118</th>
      <td>1</td>
      <td>2.95</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>123</th>
      <td>1</td>
      <td>2.55</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>126</th>
      <td>2</td>
      <td>2.16</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>127</th>
      <td>1</td>
      <td>1.34</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>129</th>
      <td>1</td>
      <td>2.88</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>131</th>
      <td>1</td>
      <td>2.99</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>134</th>
      <td>1</td>
      <td>2.15</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>138</th>
      <td>1</td>
      <td>2.63</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>139</th>
      <td>1</td>
      <td>4.25</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>148</th>
      <td>1</td>
      <td>4.65</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>154</th>
      <td>2</td>
      <td>8.22</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>155</th>
      <td>1</td>
      <td>4.04</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>156</th>
      <td>1</td>
      <td>4.53</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>158</th>
      <td>1</td>
      <td>1.94</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>163</th>
      <td>1</td>
      <td>4.16</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>164</th>
      <td>1</td>
      <td>1.31</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>167</th>
      <td>1</td>
      <td>3.25</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>170</th>
      <td>1</td>
      <td>1.74</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>172</th>
      <td>1</td>
      <td>2.71</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>173</th>
      <td>1</td>
      <td>4.01</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>174</th>
      <td>1</td>
      <td>1.36</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>176</th>
      <td>2</td>
      <td>4.24</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>180</th>
      <td>2</td>
      <td>5.54</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>181</th>
      <td>1</td>
      <td>4.12</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>64 rows × 3 columns</p>
</div>




```python
#Add Price to ItemID Summary DataFrame
ItemID_summary_df["Price"] = purchase_data_df["Price"]

# Drop all rows with missing information
ItemID_summary_df = ItemID_summary_df.dropna(how='any')

ItemID_summary_df 




```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Purchase Count</th>
      <th>Total Purchase Value</th>
      <th>Item Name</th>
      <th>Price</th>
    </tr>
    <tr>
      <th>Item ID</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>1.89</td>
      <td>Apocalyptic Battlescythe</td>
      <td>4.49</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>3.67</td>
      <td>Dawne</td>
      <td>3.36</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>2.65</td>
      <td>Putrid Fan</td>
      <td>2.63</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1</td>
      <td>1.91</td>
      <td>Feral Katana</td>
      <td>4.11</td>
    </tr>
    <tr>
      <th>5</th>
      <td>1</td>
      <td>2.63</td>
      <td>Purgatory, Gem of Regret</td>
      <td>2.22</td>
    </tr>
    <tr>
      <th>6</th>
      <td>1</td>
      <td>3.58</td>
      <td>Warmonger, Gift of Suffering's End</td>
      <td>4.65</td>
    </tr>
    <tr>
      <th>8</th>
      <td>1</td>
      <td>2.22</td>
      <td>Misery's End</td>
      <td>1.79</td>
    </tr>
    <tr>
      <th>9</th>
      <td>1</td>
      <td>1.42</td>
      <td>Mercy, Katana of Dismay</td>
      <td>4.25</td>
    </tr>
    <tr>
      <th>10</th>
      <td>1</td>
      <td>1.81</td>
      <td>Exiled Mithril Longsword</td>
      <td>1.08</td>
    </tr>
    <tr>
      <th>12</th>
      <td>1</td>
      <td>3.36</td>
      <td>Betrayer</td>
      <td>4.12</td>
    </tr>
    <tr>
      <th>14</th>
      <td>1</td>
      <td>2.82</td>
      <td>Bonecarvin Battle Axe</td>
      <td>4.36</td>
    </tr>
    <tr>
      <th>16</th>
      <td>1</td>
      <td>2.15</td>
      <td>Primitive Blade</td>
      <td>1.36</td>
    </tr>
    <tr>
      <th>17</th>
      <td>1</td>
      <td>1.96</td>
      <td>Soul-Forged Steel Shortsword</td>
      <td>4.53</td>
    </tr>
    <tr>
      <th>18</th>
      <td>1</td>
      <td>3.75</td>
      <td>Relentless Iron Skewer</td>
      <td>2.12</td>
    </tr>
    <tr>
      <th>23</th>
      <td>1</td>
      <td>1.62</td>
      <td>Darkheart, Butcher of the Champion</td>
      <td>1.94</td>
    </tr>
    <tr>
      <th>25</th>
      <td>1</td>
      <td>4.78</td>
      <td>Demise</td>
      <td>3.09</td>
    </tr>
    <tr>
      <th>27</th>
      <td>1</td>
      <td>3.38</td>
      <td>Heartstriker, Legacy of the Light</td>
      <td>4.71</td>
    </tr>
    <tr>
      <th>31</th>
      <td>1</td>
      <td>4.59</td>
      <td>Fate, Vengeance of Eternal Justice</td>
      <td>2.88</td>
    </tr>
    <tr>
      <th>41</th>
      <td>1</td>
      <td>3.85</td>
      <td>Heartseeker, Reaver of Souls</td>
      <td>1.34</td>
    </tr>
    <tr>
      <th>44</th>
      <td>1</td>
      <td>4.36</td>
      <td>Fusion Pummel</td>
      <td>2.42</td>
    </tr>
    <tr>
      <th>60</th>
      <td>2</td>
      <td>5.40</td>
      <td>Storm-Weaver, Slayer of Inception</td>
      <td>4.39</td>
    </tr>
    <tr>
      <th>64</th>
      <td>2</td>
      <td>4.84</td>
      <td>Exiled Doomblade</td>
      <td>1.31</td>
    </tr>
    <tr>
      <th>68</th>
      <td>1</td>
      <td>4.39</td>
      <td>Nirvana</td>
      <td>1.77</td>
    </tr>
    <tr>
      <th>70</th>
      <td>1</td>
      <td>4.28</td>
      <td>Deadline, Voice Of Subtlety</td>
      <td>1.29</td>
    </tr>
    <tr>
      <th>71</th>
      <td>1</td>
      <td>3.09</td>
      <td>Wolf</td>
      <td>2.70</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Display top 5 most popular Items based on number of times it was purchased 
ItemID_summary_df.nlargest(5,'Purchase Count')
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Purchase Count</th>
      <th>Total Purchase Value</th>
      <th>Item Name</th>
      <th>Price</th>
    </tr>
    <tr>
      <th>Item ID</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>60</th>
      <td>2</td>
      <td>5.40</td>
      <td>Storm-Weaver, Slayer of Inception</td>
      <td>4.39</td>
    </tr>
    <tr>
      <th>64</th>
      <td>2</td>
      <td>4.84</td>
      <td>Exiled Doomblade</td>
      <td>1.31</td>
    </tr>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>1.89</td>
      <td>Apocalyptic Battlescythe</td>
      <td>4.49</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>3.67</td>
      <td>Dawne</td>
      <td>3.36</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>2.65</td>
      <td>Putrid Fan</td>
      <td>2.63</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Change Display order of columns 
print("Most Popular Items")
ItemID_summary_df.loc[:,["Item Name", "Purchase Count", "Price", "Total Purchase Value"]].nlargest(5,"Purchase Count")


```

    Most Popular Items
    




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Item Name</th>
      <th>Purchase Count</th>
      <th>Price</th>
      <th>Total Purchase Value</th>
    </tr>
    <tr>
      <th>Item ID</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>60</th>
      <td>Storm-Weaver, Slayer of Inception</td>
      <td>2</td>
      <td>4.39</td>
      <td>5.40</td>
    </tr>
    <tr>
      <th>64</th>
      <td>Exiled Doomblade</td>
      <td>2</td>
      <td>1.31</td>
      <td>4.84</td>
    </tr>
    <tr>
      <th>0</th>
      <td>Apocalyptic Battlescythe</td>
      <td>1</td>
      <td>4.49</td>
      <td>1.89</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Dawne</td>
      <td>1</td>
      <td>3.36</td>
      <td>3.67</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Putrid Fan</td>
      <td>1</td>
      <td>2.63</td>
      <td>2.65</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Ident Most Profitable Items based on Amount of Total Purchases 
print("Most Profitable Items")
ItemID_summary_df.loc[:,["Item Name", "Purchase Count", "Price", "Total Purchase Value"]].nlargest(5,"Total Purchase Value")
```

    Most Profitable Items
    




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Item Name</th>
      <th>Purchase Count</th>
      <th>Price</th>
      <th>Total Purchase Value</th>
    </tr>
    <tr>
      <th>Item ID</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>60</th>
      <td>Storm-Weaver, Slayer of Inception</td>
      <td>2</td>
      <td>4.39</td>
      <td>5.40</td>
    </tr>
    <tr>
      <th>64</th>
      <td>Exiled Doomblade</td>
      <td>2</td>
      <td>1.31</td>
      <td>4.84</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Demise</td>
      <td>1</td>
      <td>3.09</td>
      <td>4.78</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Fate, Vengeance of Eternal Justice</td>
      <td>1</td>
      <td>2.88</td>
      <td>4.59</td>
    </tr>
    <tr>
      <th>68</th>
      <td>Nirvana</td>
      <td>1</td>
      <td>1.77</td>
      <td>4.39</td>
    </tr>
  </tbody>
</table>
</div>


