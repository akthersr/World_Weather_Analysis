# World_Weather_Analysis
## Overview
This analysis collect and analyze weather data across cities worldwide.The python based app "PlanMyTrip" will use the data to recommend ideal hotels based on clients' weather preferences.In this analysis,we will create a Pandas DataFrame with 500 or more of the world's unique cities and their weather data in real time. This process will entail collecting, analyzing, and visualizing the data.
Specifically,after adding the weather description to the weather data we use input statements to filter the data for their weather preferences, which will be used to identify potential travel destinations and nearby hotels. From the list of potential travel destinations,we will choose four cities to create a travel itinerary. Then, using the Google Maps Directions API, we will create a travel route between the four cities as well as a marker layer map.Finally, a directions layer is produced in Google map to show the directions between multiple cities for travel.

## Resources
### Data sources:

1.WeatherPy_Database.csv

2.WeatherPy_vacation.csv

### Software:

1.Python 3.9.7

2.Jupyter Notebook 6.4.5

3.Pandas, citipy, Scipy, requests, gmaps, and numpy libraries and dependencies

4.OpenWeatheMap API and Directions API

## Analysis

This analysis of the data will be split into three main parts, or stages.

1. We create a DataFrame by using OpenWeatherMap API search with weather parameters.Then,parse the JSON data from the API request.The weather parameters consists of:

 City and country

 Latitude and longitude

 Maximum temperature

 Humidity

 Cloudiness

 Wind speed

 Current weather description

2. By identifing potential travel destinations and nearby hotels for each city, we create a marker layer map with pop-up markers that will display information on specific cities based on a customer's weather preferences.At first,we filter the Pandas DataFrame based on user inputs for a minimum and maximum temperature and find a hotel from the cities' coordinates using Google's Maps and Places API, and Search Nearby feature.At the end,the marker layer map with a pop-up marker for each city display information about the country, current weather decription and the hotel name of the city.

3. In this step,four DataFrames are created, one for each city on the itinerary and the latitude and longitude pairs for each of the four cities are retrieved.A directions layer map between the cities and the travel map is created.Finally,using the Google Maps Directions API,a marker layer map with a pop-up marker between four nearby cities on the vacation itinerary is created. Each marker has the following information:

 Hotel name

 City

 Country

 Current weather description with the maximum temperature

## Outputs

### Weather Database

Using OpenWeatherMap API,679 unique cities were determined from 2000 randomly selected latitudes and longitudes.The dataframe is as follows:

![](https://github.com/akthersr/World_Weather_Analysis/blob/main/Weather_Database/current%20weather.png)

After cleaning the data frame by dropping the empty rows and null hotel values we get the following data frame:

![](https://github.com/akthersr/World_Weather_Analysis/blob/main/Weather_Database/hotel%20name.png)

### Vacation Search

The figure below shows the locations of all the places in the database that have a daily maximum temperature between 75 and 90 degrees farinheit.

![](https://github.com/akthersr/World_Weather_Analysis/blob/main/Vacation_Search/WeatherPy_vacation_map.png)


### Vacation Itinerary

The image below shows a 4 stop itinerary in Brazil that features Vila Velha, Santa Vitoria, Palmas, and Mombaca.

![](https://github.com/akthersr/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map.png)


Also, as with the vacation search, there is a hotel at each location.

![](https://github.com/akthersr/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map_markers.png)











