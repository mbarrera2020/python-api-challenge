### python-api-challenge

Author: Maria Barrera
Date: 02/07/2021
Description:  Creating a Python script to visualize the weather of various cities.

#### Part 1 -- mainWeatherPy
Goal:  Create a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. 

Process:  Use citypy (python library) and the OpenWeatherMap API; 
          randomly select at least 500 unique (non-repeat) cities based on latitude and longitude.

Output: Randomly select at least 500 unique (non-repeat) cities based on latitude and longitude & store city data into a CSV file    
    
Tasks:
    1) create a series of scatter plots to showcase the following relationships:
        Temperature (F) vs. Latitude
        Humidity (%) vs. Latitude
        Cloudiness (%) vs. Latitude
        Wind Speed (mph) vs. Latitude
        
    2) run linear regression on each relationship
        ** Need to separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and 
        Southern Hemisphere (less than 0 degrees latitude):
            Northern Hemisphere - Temperature (F) vs. Latitude
            Southern Hemisphere - Temperature (F) vs. Latitude
            Northern Hemisphere - Humidity (%) vs. Latitude
            Southern Hemisphere - Humidity (%) vs. Latitude
            Northern Hemisphere - Cloudiness (%) vs. Latitude
            Southern Hemisphere - Cloudiness (%) vs. Latitude
            Northern Hemisphere - Wind Speed (mph) vs. Latitude
            Southern Hemisphere - Wind Speed (mph) vs. Latitude
            
#### Part 1 -- Observations -- based on sample city data

For ALL cities:
Latitude vs Temperature: Temperature decreases as latitude increases

Latitude vs Humidity: Humidity is usually between 40 – 100% for latitude between -40 to 80.

Latitude vs Cloudiness: Cloudiness is between 0 to 100 for latitude between -40 to 80.

Latitude vs Wind Speed: Wind speed is between 0 to 10 for latitude between -40 to 80.

Northern Hemisphere -- Max Temp vs Latitude: As the city latitude increases, the temperature decreases.
    Correlation: Lat = 0.83, Temp = 2.2

Southern Hemisphere -- Max Temp vs Latitude: As the city latitude increases, the temperature increases.
    Correlation: Lat = 0.61, Temp = 1.0

Northern Hemisphere -- Humidity vs Latitude Linear Regression: As the city latitude increases, the temperature decreases.
    Correlation: Lat = 0.83, Temp = 0.21
    
Northern Hemisphere -- Wind Speed (mph) vs. Latitude Linear Regression:
    Wind speed is between 0 – 20 mph for latitude between 0 to 80.
    Correlation: Lat = 0.11, Wind = 0.10
    
Southern Hemisphere -- Wind Speed (mph) vs. Latitude Linear Regression:
    Wind speed is between 0 – 20 mph for latitude between 0 to -60.
    Correlation: Lat = 0.05, Wind = 0.61
    
#### Part 2 -- mainVacationPy

Input:  CSV city file (from part 1 above)

Tasks:  Create a heat map that displays the humidity for every city from Part I
        ** see screen shots of vac_map_1 & vac_map_2 in the images folder

Output:  
    Narrow down the DataFrame to find your ideal weather condition. For example:
    A max temperature lower than 80 degrees but higher than 70.
    Wind speed less than 10 mph.
    Zero cloudiness.
    Drop any rows that don't contain all three conditions. You want to be sure the weather is ideal.
    