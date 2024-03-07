DU - DA Module 6 challenge
--------------------------------
--------------------------------
Python - API - Challenge
--------------------------------
by Laura Vara
--------------------------------
![WeatherVacAPI](https://github.com/vara-co/python-api-challenge/assets/152572519/ab277542-c68c-41c8-b14a-c3e92b828165)

Note: It is important that if you are going to use this code, the csv file
is placed in a directory called output_data, in the same directory as a directory named JupyterNotebook_files
wher eyou will place your main Jupyter Notebook files. Otherwise the code with the path were you intend to read 
your csv file, needs to be updated to where the new path is located for the
csv file. Ideally they will be set in the same way they are found in this repository.
In addition, you need an api_key file in the same directory as your main Jupyter Notebook files, where you will 
add your API keys between the quotations to use the code.
This is the format in the api_key file. It should be in a .py format idealy to work.
Create your file and copy paste the following code. You will paste your obtained API keys in the appropirate line between the quotations
and save the file. Close it and then work on the Jupyter Notebook. 

--------------------------------------

# OpenWeatherMap API Key
weather_api_key = "YOUR KEY HERE"

# Geoapify API Key
geoapify_key = "YOUR KEY HERE"

----------------------------------------

Follow the instructions in each website to get your API keys.
Links for obtaining an API key:
1. For the weather_api_key: https://openweathermap.org/
2. For the geoapify_key: https://www.geoapify.com/get-started-with-maps-api

This repository consists of a challenge created using Pandas and Matplotlib via Jupyter Notebook:
---------------------------------
INDEX
---------------------------------
1. Content of the repository
2. Instructions for the Python Api Challenge

---------------------------------
Content of the repository
---------------------------------
1. Python API Challenge
- JupyterNotebook_files Directory:
    - WeatherPyLMVS.ipynb file
    - VacationPyLMVS.ipynb file
    - This is where you would add your api_key.py file
      (Note it is not present in this repository for security measures)
- output_data Directory:
    - cities.csv

----------------------------------
Instructions for the Python API Challenge
----------------------------------

Instructions
This activity is broken down into two deliverables, WeatherPy and VacationPy.

# Part 1: WeatherPy
In this deliverable, you'll create a Python script to visualize the weather of over 500 cities of varying distances from the equator. You'll use the citipy Python libraryLinks to an external site., the OpenWeatherMap APILinks to an external site., and your problem-solving skills to create a representative model of weather across cities.

For this part, you'll use the WeatherPy.ipynb Jupyter notebook provided in the starter code ZIP file. The starter code will guide you through the process of using your Python coding skills to develop a solution to address the required functionalities.

To get started, the code required to generate random geographic coordinates and the nearest city to each latitude and longitude combination is provided.

## Requirement 1: Create Plots to Showcase the Relationship Between Weather Variables and Latitude
To fulfill the first requirement, you'll use the OpenWeatherMap API to retrieve weather data from the cities list generated in the starter code. Next, you'll create a series of scatter plots to showcase the following relationships:

Latitude vs. Temperature
Latitude vs. Humidity
Latitude vs. Cloudiness
Latitude vs. Wind Speed

## Requirement 2: Compute Linear Regression for Each Relationship
To fulfill the second requirement, compute the linear regression for each relationship. Separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude). You may find it helpful to define a function in order to create the linear regression plots.

## You should create the following plots:
Northern Hemisphere: Temperature vs. Latitude
Southern Hemisphere: Temperature vs. Latitude
Northern Hemisphere: Humidity vs. Latitude
Southern Hemisphere: Humidity vs. Latitude
Northern Hemisphere: Cloudiness vs. Latitude
Southern Hemisphere: Cloudiness vs. Latitude
Northern Hemisphere: Wind Speed vs. Latitude
Southern Hemisphere: Wind Speed vs. Latitude

After each pair of plots, explain what the linear regression is modeling. Describe any relationships that you notice and any other findings you may uncover.

# Part 2: VacationPy
In this deliverable, you'll use your weather data skills to plan future vacations. Also, you'll use Jupyter notebooks, the geoViews Python library, and the Geoapify API.
The code needed to import the required libraries and load the CSV file with the weather and coordinates data for each city created in Part 1 is provided to help you get started.
Your main tasks will be to use the Geoapify API and the geoViews Python library and employ your Python skills to create map visualizations.
To succeed on this deliverable of the assignment, open the VacationPy.ipynb starter code and complete the following steps:
Create a map that displays a point for every city in the city_data_df DataFrame as shown in the following image. The size of the point should be the humidity in each city.

Narrow down the city_data_df DataFrame to find your ideal weather condition. For example:
A max temperature lower than 27 degrees but higher than 21
Wind speed less than 4.5 m/s
Zero cloudiness

## NOTE
Feel free to adjust your specifications but make sure to set a reasonable limit to the number of rows returned by your API requests.
Create a new DataFrame called hotel_df to store the city, country, coordinates, and humidity.
For each city, use the Geoapify API to find the first hotel located within 10,000 meters of your coordinates.
Add the hotel name and the country as additional information in the hover message for each city on the map

## Hints and Considerations
The city data that you generate is based on random coordinates and different query times, so your outputs will not be an exact match to the provided starter notebook.
If you'd like a refresher on the geographic coordinate system, this siteLinks to an external site. has great information.
Take some time to study the OpenWeatherMap API. Based on your initial study, you should be able to answer basic questions about the API: Where do you request the API key? Which Weather API in particular will you need? What URL endpoints does it expect? What JSON structure does it respond with? Before you write a line of code, you should have a crystal-clear understanding of your intended outcome.
A starter code for citipy has been provided. However, if you're craving an extra challenge, push yourself to learn how it works by using the citipy Python libraryLinks to an external site.. Before you try to incorporate the library in your analysis, start with simple test cases outside of your main script to confirm that you are using it correctly. Often, when introduced to a new library, learners spend hours trying to figure out errors in their code when a simple test case can save you a lot of time and frustration.
You will need to apply your critical thinking skills to understand how and why we're recommending these tools. What is citipy used for? Why would you use it in conjunction with the OpenWeatherMap API? How would you do so?
While building your script, pay attention to the cities you are using in your query pool. Are you covering the full range of latitudes and longitudes? Or are you choosing 500 cities from one region of the world? Even if you were a geography genius, simply listing 500 cities based on your personal selection would create a biased dataset. Try to think of ways that you can counter these selection issues.

## Hint: Consider the full range of latitudes.
Once you have computed the linear regression for one relationship, you will follow a similar process for all other charts. Optionally, try to create a function that will create these charts based on different parameters. (Note: there will be no extra points for completing this.)
Remember that each coordinate will trigger a separate call to the Google API. If you're creating your own criteria to plan your vacation, try to reduce the results in your DataFrame to 10 or fewer cities.
Ensure that your repository has regular commits and a thorough README.md file.
