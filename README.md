# Geopatial_Analysis
Geopatial Analysis Project Involving (Zomata Case Study) on Restuarants in Bangalore.

#### Dataset:
download dataset here https://drive.google.com/drive/u/0/folders/11-efbrZ5FZRPtcHaytKbtqwA20DZiORn 

#### Problem Statement => Data Cleaning, Find % of missing values, Deal with missing values

To find `the  % missing of values`, use a `list_conprehension` iterate the columns to return all the features with `null_na`. and calculating `the % missing of values` we return the sum of `null_na` and divided it by the lenght of `df` and multiply by 100. `{df[features].isnull().sum()/len(df)*100}` 

To deal with the missing values, a column with highest number of  missing values(`rate`) was choosing and manipulations where done to remove and replace missing values other than `null_na`. 

#### Problem Statement => Cal. Avg Rating of each Restuarant.

call a `groupby` function on the `name` and `rate` column to return the mean of  all the restaurants.

#### Problem Statement =>  Get Distributions of Rating Column & try to find out what Distribution this Feature Support.

Used `displot` from `searborn` to visualized Restuarants with highest Avg. ratings.

#### Problem Statement =>  Top Restaurants Chains in Bangalore. 

use `value_counts()` on the `name` column to return the number of restaurants and there outlet. you can visualize using barplot 

#### Problem Statement =>  How many of the Restuarants Do Not  Accep Online Orders . 
Do a `value_counts` on the `online_order` column  and visualize using pie chart.


