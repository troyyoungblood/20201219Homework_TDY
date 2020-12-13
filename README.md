# 20201219Homework_TDY
API homework
# Python API Homework - What's the Weather Like?

Summary of observations from exercise.

Observation 1
The City Latitude vs Maximum Temperature scatter plot is analyzing the various maximum temperatures against latitude.
The data presented indicates an interesting relationship for the northern and southern hemispheres.
To the left of zero (southern hemisphere), the temperatures a fairly closely distributed from 40 F to 80 F,
increasing as approaching the equator.
To the right of zero (northern hemisphere), the temperatures have a wide range, decreasing as approaching the pole.
These behaviors are most likely presented because of the current season,
late fall, northern hemisphere, and late spring, southern hemisphere. (tilt of the earth and less sunlight)

Observation 2
The City Latitude vs Humidity scatter plot is analyzing the various humidity percentage values against latitude.
The data presented indicates a wide distribution of data points, most likely related to current weather conditions
such as a front or recent rain.
To the left of zero (southern hemisphere), the humidity is fairly scattered between latitidue values
with the majority of the points above 60% humidity.
To the right of zero (northern hemisphere), the humidity is fairly scatteres between latitiude values,
with the majority of the points above 60% humidity.  

Observation 3
The City Latitude vs Cloudiness and City Latitude vs Wind Speed scatter plots
represent data that is a snapshot in time when the data was collected. 
They are not very valuable datasets.

## Part I - WeatherPy

Python script was used to visualize the weather of 500+ cities across the world of varying distance from the equator. A  [simple Python library](https://pypi.python.org/pypi/citipy) was utilized along with the [OpenWeatherMap API](https://openweathermap.org/api), to create a representative model of weather across world cities.

A first set of scatter plots to presenting the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

After each plot, information describing the plots was presented and then used to compose overall obersations.

Separate datasets were then created for the Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude) and used to present information similar to the first series of scatter plots.  Linear regression on each relationship was also completed with Pearson's coefficient to identify the fit. 

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

After each plot, information describing the plots was presented and then used to compose overall obersations.

The final notebook contains:

* Randomly selected greater than 500 unique (non-repeat) cities based on latitude and longitude.
* A weather check on each of the cities using a series of successive API calls.
* A print log of each city as it's being processed with the city number and city name.
* A CSV of all retrieved data and a PNG image for each scatter plot.

### Part II - VacationPy

To complete this part, the csv file of cities was imported for Part I - WeatherPy.

A heatmap was created displaying the humidity for every city from Part I.

Then, the data was filtered using the follwoing criteria to generate a list of potenital vaction locaitons.

  * A max temperature lower than 90 degrees but higher than 40.

  * Humidity percentage less than 60%.

  * Country of Australia.
  
  The locations selected were:
  
  * Hobart Australia
  * Cockburn, Australia
  * Narrabri, Australia
  * Innisfail, Australia
  * Mackay, Australia
  * Townsville, Australia
  * Ulladulla, Australia
  * Flinders, Australia
  
 Then, Google Places API was used to find the first hotel for each city located within 5000 meters of the coordinates of the heat locations.

The hotels were then layered on top of the humidity heatmap with a pin containing the **Hotel Name**, **City**, and **Country**.


