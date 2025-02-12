# Geopatial_Analysis
Geopatial Analysis Project Involving (Zomata Case Study) on Restuarants,Hotels in Bangalore.

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

Create two list to store the group rest.locations and rest.names count. apply `sort_values()` function to return locations with highest number of rest.names_count.

##### Rest_count by locations.

![location_rest_count](https://user-images.githubusercontent.com/42388234/159534101-3fb30ff7-46dc-4835-bdfa-a1d8973394de.png)

#### Problem Statement =>  Total number of variety of Restaurants in Banglore

Do a `Value_count` on `cuisines` column and Visualize using `Bar`

![Variety_rest](https://user-images.githubusercontent.com/42388234/160211910-c6b57640-c205-42e7-b64d-29ef9e47299f.png)


#### Problem Statement => Appro Cost for 2 People Feature

we need to remove the `','` in the `uique` features before `datatype` can be  converted from `obj` to `int` and also before `seaborn` can visualize it.

![Appr_2_peop_cost_plot](https://user-images.githubusercontent.com/42388234/160211992-0f867d7a-21b2-4a02-99ad-1a4641cc246e.png)


#### Problem Statement =>  Analyse  'Approx. Cost  of 2 People' vs 'ratiing' Find out some Relationship.

use `Scatterplot` to find out there relationship and and apply `hue` over the `online_order` to come with a conslusion 
over the top_rated restaurants that accept online_order.

![Appro_2_peop_vs_rate](https://user-images.githubusercontent.com/42388234/160212076-c3fb93c0-76d7-4af9-afb5-103d69aad1c9.png)

#### Problem Statement => Is there any difference b/w Votes of Restaurants Accepting and not  Accepting Online_Order.

Do a `box plot`  on `Online Order` vs `votes` to see the d/f. 

![difference_bw_Votes_of_Restaurants_online_order](https://user-images.githubusercontent.com/42388234/160212198-5fbfc05a-5474-40cd-a9d9-5257482f15dc.png)


#### Problem Statement => Is there any difference b/w Price of Restaurants Accepting and not  Accepting Online_Order.

Do a `box plot`  on `Online Order` vs `Appro Cost (for two people)` to see the d/f. 

![online_order_price_difference](https://user-images.githubusercontent.com/42388234/160212299-be375adb-ece1-41ba-94bb-74fc0476f199.png)

#### Problem Statement => Find Out the Most Luxurius Rest. in Banglore.

find the `max` price for two people and filter the `df` to return rest with max_price.

#### Problem Statement => Top 10 Most Expensive  Rest. with  Approx. Cost for two People.

Make a copy of the `df` and reset `name` as `index` find the `nlargest` and visualized similary for `cheapest` rest find the `nsmallest` and visualized.

###### Most Luxurius
![Mosr_Exp_rest](https://user-images.githubusercontent.com/42388234/160212439-577b8691-0d86-409d-95d0-a3722e2f2924.png)

###### Most Cheapest
![Most_cheap_rest](https://user-images.githubusercontent.com/42388234/160212550-fb4bad7f-bc47-477a-9ef8-cbb71a991800.png)


#### Problem Statement => Find Out the Rest that are Below 500 as well as Affordable.

Filter the Cost of two people on the rest less than 500. 

#### Problem Statement => Rest. with Rating > 4 and the Budget are Good/Affordable.

Filter the `rate` > 4 and `approx_cost(for two people` `columns` <=500  and return the `len` of the `unique` `name`.

#### Problem Statement =>  Total Afordabele Hotels in all  the Locations in Bangalore. 

Filter the `rate` > 4 and `approx_cost(for two people` `columns` <=500 and `group` the total number of hotels according to locations. 

#### Problem Statement =>  Finding  the Best Budget Restaurant in any Location.

Fileter the `df` on `Cost of two peop.`, `rate` and return the `location` and `restaurants` list passed in the filter.

#### Problem Statement =>  Which Areas are the Foodie.

Do a `value_count` on the `location` and visualized the most foodie areas. 

![foodie](https://user-images.githubusercontent.com/42388234/160273813-88b563b2-bb58-4d98-9b71-bc4c68efdc1d.png)

## Geopatial Analysis.

In this project, get the locations `name`, get the location `latitude and longitude`, `Merge` with location `Rest_count` and convert the `latitude and longitude` to array and generate a `baseMap` based on the `default_location` and `zoom_start` from the Restaurants_locations, to generate a `HeatMap` apply the function on the `lat`, `lon` and `count` of Restaurants locations and use value_tollist to convert to array and add it back to the basemap in other to visualized the HeatMpap on tne Restaurants locations.

##### Basemap
![basemap](https://user-images.githubusercontent.com/42388234/160280113-c275bfa0-0e53-4d85-88e7-eebc0e4108f8.png)

##### HeatMap Basemap
![heatmap_basemap](https://user-images.githubusercontent.com/42388234/160280118-de8e1d96-f299-4185-a432-95ea1404a417.png)

##### Heat map of North Indian Restaurants

Filter the `north_indian` rest.count and `merge` it with the `locations df` and apply the HeatMap on the `lat` and `lon` from the basemap function to visualize.

![north_india_heatmap](https://user-images.githubusercontent.com/42388234/160284535-452d5ada-bf09-44a6-aa28-a7c9dad0c017.png)

##### Which are the Most Popular Casual Dining Restaurants Chains.

group the `name` of restaurants according to there `rest_type` and `agg` count, group again and sort according to `url` to get a total count, filter out the `name`, `url` and `rest_type` columns. To get Most Popular Casual Dining Restaurants Chains. Do a filter on the `rest_type`. 











