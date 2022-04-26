# Python-API-Challenge
Python API exercises 

## Overview:

   Using Jupyter Notebooks to develop a report provides an opportunity to present a wide array of data frames, charts, and other visualization tools that make it easier for the consumer to understand the data. Ultimately, our goal in developing reports should be to allow the user to make the decisions necessary based on their data efficiently. As usual, once we understand the customer's needs, we should take a moment to explore the data and better understand its design and potential limitations. In this scenario, we will develop a report containing information that will enable the user to understand weather data surrounding certain cities based on their geographical location. We will take advantage of several modules, including the requests module, that will enable us to utilize API functionality.   
    We begin our Python script by importing the necessary dependents that will enable us to perform the required functions within the script. This is an important step, as these additional modules will make processing the data more accessible. Along with your dependencies, you will need to make sure that you already have the API keys required to access the data resources for the OpenWeatherMap API and the Google Maps API. Being able to request data from these resources is critical to these exercises. Remember to utilize proper security practices to protect your API keys. 
    In both exercises, we will create the basic URL address and the parameters needed to run the requests to retrieve the data we need to make our analysis. For the Weatherpy exercise, we take advantage of the matplotlib functionality to create visualizations with charts. We use scatter plots and regression charts to analyze the relationship between specific locations and weather conditions. In the Vacationpy exercise, we utilize the Google Maps functionality to locate hotels within certain cities based on ideal weather conditions.
    The information from the weatherpy exercise allows the user to develop an idea of potential relationships within the data that can help to determine the different weather conditions that may or may not be impacted by a cities location, and based on the user's definition of ideal weather; they are also able to utilize the vacation exercise to see potential vacation locations. You can see how gaining this type of insight can facilitate better decisions based on data rather than making assumptions.
    

## Part 1: WeatherPy

In this section, you'll create a Python script to visualize the weather of 500+ cities of varying distance from the equator. To do so, you'll use a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api), and your problem-solving skills to create a representative model of weather across cities.

The first requirement is to create a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

After each plot, add a sentence or two explaining what the code is analyzing.

The second requirement is to compute the linear regression for each relationship. This time, separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

After each pair of plots, explain what the linear regression is modeling. For example, describe any relationships that you notice and any other findings you may have.

Your final notebook must:

* Randomly select **at least** 500 unique (non-repeated) cities based on latitude and longitude.
* Perform a weather check on each of the cities using a series of successive API calls.
* Include a print log of each city as it's being processed, with the city number and city name.
* Save a CSV of all retrieved data and a PNG image for each scatter plot.

### Part 2: VacationPy

Now, let's use your skills working with weather data to plan future vacations. Use Jupyter-gmaps and the Google Places API for this part of the assignment.

To complete this part of the assignment, you will need to do the following:

* Narrow down the DataFrame to find your ideal weather condition. For example:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

  * Drop any rows that don't satisfy all three conditions. You want to be sure the weather is ideal.
 
* Use Google Places API to find the first hotel for each city located within 5,000 meters of your coordinates.

* Plot the hotels on top of the humidity heatmap, with each pin containing the **Hotel Name**, **City**, and **Country**, as in the following image: