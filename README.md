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

##### Rating Distr.
![rating_distribution](https://user-images.githubusercontent.com/42388234/159532175-54b2e7fa-eacf-4553-a878-0bb868543b9f.png)

#### Problem Statement =>  Top Restaurants Chains in Bangalore. 

use `value_counts()` on the `name` column to return the number of restaurants and there outlet. you can visualize using barplot 

##### Top Chains_rest.
![top_chains_restaurants](https://user-images.githubusercontent.com/42388234/159532476-9b5b4298-a19a-4c0f-adfe-52d0aaf120d3.png)


#### Problem Statement =>  How many of the Restuarants Do Not  Accep Online Orders . 
Do a `value_counts` on the `online_order` column  and visualize using pie chart.

![Online_order](https://user-images.githubusercontent.com/42388234/159532897-178495e6-ed06-4319-a750-bfb9fbaa3a7c.png)


####  Problem Statement =>   Ratio Between Restauarants that Provide Table and Restaurants that do not Provide Table.

Do a `value_counts` on `book_table` and visualize using `graph_objs` from `plotly`

![bookings_or_not](https://user-images.githubusercontent.com/42388234/159533186-f5a2c69d-da23-4f84-88d7-96e2f8124d00.png)


###### NOTE:

Different plotly Extension: 

1. `import plotly.express as px` ploting `px.pie()` the `pie` is lowercase.

2.  `import plotly.graph_objs as go` ploting `go.Pie()` the `Pie` is uppercase. (graph_objs takes on uppercase)


####  Problem Statement =>  Indept  Analysis on Types of Restaurants we have.

To discover the most populated species of Rest. Drop the `null` values in `rest_type` columns, do a `value_count` and visualize using `Bar` plot. 

##### Types of Rest.
![types_rest](https://user-images.githubusercontent.com/42388234/159533426-562a47cd-38f6-4c04-8797-76fb48a173a6.png)

#### Problem Statement => Highest Voted Restaurants.

group the `name` and `votes` of rest. and Visulize using `Bar`

##### Most Voted_rest.
![voted_rest](https://user-images.githubusercontent.com/42388234/159533758-4376a84e-629e-47e8-a362-06857015eece.png)

#### Problem Statement => Total Restaurants at different locations in Bangalore.

create two list to store the group rest.locations and rest.names count. apply `sort_values()` function to return locations with highest number of rest.names_count.  










