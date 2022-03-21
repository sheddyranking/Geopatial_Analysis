# Geopatial_Analysis
Geopatial Analysis Project Involving (Zomata Case Study).


### Problem Statement => Data Cleaning, Find % of missing values, Deal with missing values

To find `the  % missing of values`, use a `list_conprehension` iterate the columns to return all the features with `null_na`. and calculating `the % missing of values` we return the sum of `null_na` and divided it by the lenght of `df` and multiply by 100. `{df[features].isnull().sum()/len(df)*100}` 

To deal with the missing values, a column with highest number of  missing values(`rate`) was choosing and manipulations where done to remove and replace missing values other than `null_na`. 

##### upload larging csv
check here for documentation https://git-lfs.github.com/

#### dataset
download dataset here https://drive.google.com/drive/u/0/folders/11-efbrZ5FZRPtcHaytKbtqwA20DZiORn
