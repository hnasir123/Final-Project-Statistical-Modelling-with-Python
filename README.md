# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
The goal of the project is to extract the data from three different APIs of citybikes,foursquare and Yelp for bikes and POIs in the area and try to find any relationship between number of bikes and POI characterstics. We build Statistical model after extracting data from all the APIs and anayzed the results. We have to choose a city for this purpose so i chose Paris and extracted data from all the APIs for paris and built a regression model


## Process
### Step 1: Connect and extract data from CityBikes API
The first step was to connect to citybikes API and extract data for my chosen city Paris. First network id was identified from the initial endpoint API and later using that network id details of all the bike station within the city was extracted. The data was cleaned and transformed to pandas dataframe. The city of Paris contained more than 1400 bike stations.


### Step 2: Connect to Foursquare and Yelp API
The second step was to connect to Foursquare and Yelp API and extract data for the location where bike stations are located. For this purpose latitude and longitude information was used from citybikes dataframe and API calls was sent for each latitude and longitude. The key point was figuring out the query parameters for each API
The data was collected then parsed to our desired format for further processing.
 
 ### Step 3: Joining Data
The data collected from step 1 and step 2 was joined in this step to creat a dataframe that contains necessary information like reviews, ratings, distance, free bikes required for further analysis. Exploratory data analysis was done at this point to understand the data using visulizations

 ### Step 4: Building a Model
 A regression model was build using the data collected from previous steps. First we use  descriptive satistics nad hypothesis testing to understand the data and relationships then we build a regression model using review count, ratings and free bikes as features and dependent variable respectively.

## Results
We were trying to find a relatioship between review,ratings and free bikes available in a station. It means that if a POI is more popular having great reviews and ratings does it have any impact of number of bikes in a bike station. After building the regression model and hypothesis testing we find that there is not any direct correlation on the number of bikes surounding POIs with good ratings and reviews and the relationship is statiscally insignificant.

## Challenges 
Below are the challanges faced during the project

1. Extracting the data from citybikes, foursqure and yelp API. Figuring out the right query parameters for each API 
2. Parsing of the data from citybikes,foursquare and yelp api. Most of the time was consumed by this step as the json files had nested structure and specific python    routines had to written for each API to parse the data and convent it into desired dataframe structure
3. Matching the data from different API took some effort.
4. Creating statistical model and analyzing the results

## Future Goals
AS observed during the analysis the ratings parameter can be considered as categorial variable and furhter analysis can be done to check if any relationship exists.
Furthermore we observed that the free bikes and review count parameters were not normally distributed so we can futher use transformation techniques to these variables and then observed if it makes any difference.
