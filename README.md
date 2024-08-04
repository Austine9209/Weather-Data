# Week 1 Challenge: Weather Data Analysis

This project explores a weather dataset using Python libraries such as Pandas, NumPy, and SQLite.

## Data Source

The weather data was downloaded from Kaggle (https://www.kaggle.com/datasets/ayushmi77al/weather-data-set-for-beginners).

## Dataset

The dataset contains weather records with the following columns:

- Date/Time
- Temp_C
- Dew Point Temp_C
- Rel Hum_%
- Wind Speed_km/hr
- Visibility_km
- Press_kPa
- Weather

## Analysis
### Part 1
Using python. the following questions were answered
1.	Find all records where the weather was exactly clear.
   `
  	# Find all records where the weather was exactly clear:
  	clear_weather_records = data[data['Weather'] == 'Clear']

  	# Display all record where the weather was exactly clear
  	print(clear_weather_records)
  	`
  	
3.	Find the number of times the wind speed was exactly 4 km/hr.
4.	Check if there are any NULL values present in the dataset.
5.	Rename the column "Weather" to "Weather_Condition."
6.	What is the mean visibility of the dataset?
7.	Find the number of records where the wind speed is greater than 24 km/hr and visibility is equal to 25 km.
8.	What is the mean value of each column for each weather condition?
9.	Find all instances where the weather is clear and the relative humidity is greater than 50, or visibility is above 40.
10.	Find the number of weather conditions that include snow.

