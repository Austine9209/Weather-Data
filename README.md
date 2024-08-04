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
   ```python
# Find all records where the weather was exactly clear:
  	clear_weather_records = data[data['Weather'] == 'Clear']

  	# Display all record where the weather was exactly clear
  	print(clear_weather_records)
```
Answer:
![answer 1](https://github.com/user-attachments/assets/a2c64025-4adc-4baf-8e71-c8a9ec921baf)
  	
2.	Find the number of times the wind speed was exactly 4 km/hr.
   ```python
# Find the number of times the wind speed was exactly 4 km/hr:

wind_speed_4 = data[data['Wind Speed_km/h'] == 4]
wind_speed_4.shape
```
Answer: (478, 8)

3.	Check if there are any NULL values present in the dataset.
 ```python
# Check if there are any NULL values present in the dataset:

data.isnull().sum()
```
Answer:
![ans3](https://github.com/user-attachments/assets/532c2031-bbfb-4e2a-987d-3299814b3d89)
   
4.	Rename the column "Weather" to "Weather_Condition."
 ```bash
# Find the number of times the wind speed was exactly 4 km/hr:

wind_speed_4 = data[data['Wind Speed_km/h'] == 4]
wind_speed_4.shape
```

5.	What is the mean visibility of the dataset?
```python
# What is the mean visibility of the dataset?

data['Visibility_km'].mean()
```
Answer: 27.664446721311478


6.	Find the number of records where the wind speed is greater than 24 km/hr and visibility is equal to 25 km.
```python
# Find the number of records where the wind speed is greater than 24 km/hr and visibility is equal to 25 km:

wind_speed_visibility = data[(data['Wind Speed_km/h'] > 24) & (data['Visibility_km'] == 25)]
wind_speed_visibility.shape
```
Answer: (308, 8)

7.	What is the mean value of each column for each weather condition?
```python
# Calculate the mean value of each column for each weather condition
# Exclude the 'Date/Time' column as it contains strings

mean_values_by_weather = data.drop('Date/Time', axis=1).groupby('Weather').mean()

print(mean_values_by_weather)
```
Answer: https://colab.research.google.com/drive/1NiCofCytSVMUbqxaiQ7oMuTpWYRCxcFx#scrollTo=aCiHinsQW2m3&line=1&uniqifier=1

8.	Find all instances where the weather is clear and the relative humidity is greater than 50, or visibility is above 40.

```python
# Find instances where the weather is clear and the relative humidity is greater than 50, or visibility is above 40
result = data[(data['Weather'] == 'Clear') & ((data['Rel Hum_%'] > 50) | (data['Visibility_km'] > 40))]

# Display the result
print(result)
```

Answer:
![ans8](https://github.com/user-attachments/assets/5dd56557-bb57-4187-86e5-bb2db0128526)

9.	Find the number of weather conditions that include snow.

```python
# Find the number of weather conditions that include snow.

# Filter the DataFrame for weather conditions containing "Snow"
snow_conditions = data[data['Weather'].str.contains('Snow')]

# Count the number of unique weather conditions
num_snow_conditions = snow_conditions['Weather'].nunique()

# Print the result
print("Number of weather conditions including snow:", num_snow_conditions)
```
Answer: Number of weather conditions including snow: 19

### Part 2: SQL
Import the CSV into the database:
![CSVImport](https://github.com/user-attachments/assets/774fbbbd-2d52-4721-9a9f-be7e603e4e5c)
