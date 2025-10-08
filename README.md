# Project Title 
Weather Report- Comparative analysis of rainfall between Seattle and New York City
---

## Project Overview

This analysis aims to determine whether Seattle truly receives more rainfall than New York City. By comparing daily precipitation data from both locations, we will explore the differences in rainfall frequency and total precipitation amounts using the data science methodology.
Precipitation data is downloaded from NOAA's Climate Data Online Search tool for Seattle and NYC from the dates 1st January 2018 to 31st December 2022. The findings reveal how each city's climate pattern differ, with Seattle experiencing more proportion of days with rainfall and New York City having fewer days of rainfall with heavier rain.


- **Objective:** The goal of this project is to compare the precipitation between Seattle and New York city and conclude which city recieve more rainfall.
- **Domain:** Climate Data Analysis
- **Key Techniques:** Exploratory data Analysis(EDA),Statistical Hypothesis test(t-test, z-test)

---

## Project Structure

```
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
```

---

## Data

- **Source:** Link to the data source(s) 
https://www.ncei.noaa.gov/cdo-web/search?datasetid=GHCND
https://www.ncei.noaa.gov/data/daily-summaries/doc/GHCND_documentation.pdf
- **Description:** Data is downloaded from NOAA's Climate Data Online Search tool for Seattle and NYC.  The GHCND dataset includes: Station, Date, Precipitaion,Temperature, Snowfall, Snowdepth etc.

---

## Analysis

### Data Cleaning

Precipitation data is downloaded from NOAA's Climate Data Online Search tool for Seattle and NYC from the dates Jan 1 2018 to Dec 31 2022.

Name of the file that performs the data preparation: weather/code/seattle_nyc_weather_data.ipynb
 1. Import pandas, numpy, and matplotlib libraries
 2. Load the Seattle (seattle_rain.csv) & NYC (nyc_rain.csv) data set using read_csv. The csv files are in the data folder.
 3. Start by looking at the head of each Dataframe using .head()
 4. Check for the columns in each dataframe using .columns
 5. Use the info() method to check the data types, size of the data frame, and numbers of missing values.
 6. Use ‘shape’ attributes to compare the dataframe sizes.
 7. Examine the ’STATION’ column
 8. Check for unique stations in each dataframe using .unique()
 9. Check for ‘DATE’ column and covert it to datetime using to_datetime()
 10. Check for the range of dates on each dataframe using ‘min’ and ‘max’ function
 11. Plot the daily precipitation for each city
 12. Join the NYC and Seattle dataframes keeping the date and precipitation column using outer join
 13. Create a tidy data frame for columns city and precipitation.
 14. Rename the city values to ‘NYC’ and ‘SEA
 15. Rename the columns to lowercase using .rename()
 16. Identify the missing values using .isna().sum()
 17. Count the null values in the precipitation column for NYC
 18. Count the null values in the precipitation column for Seattle
 19. Impute missing values by designing an algorithm to replace the null values with the mean across years of values on that   day.
 20. Export the clean .csv file.

Name of the cleaned csv file: data/clean_seattle_NYC_weather.csv


### Exploratory Data Analysis(EDA)& Modeling 
Name of the file that performs the EDA and modeling : weather/code/Exploratory.data.ipynb
1. Calculate basic descriptive statistics using groupby and describe
2. Create a bar plot of mean daily precipitation for each cit
3. Add a new column to the data frame indicating the month
4. Create a box plot of precipitation by month for each cit
5. Create a bar plot of mean precipitation by month for each city
6. Calculate mean precipitation by city and month using groupby
7. Add a new column indicating if any precipitation occurred
8. Calculate and plot the proportion of days with any precipitation
9. Perform a statistical t-test for differences in the mean precipitation each month between the cities
10. Perform a statistical z-test for differences in the proportion of days with any precipitation each month between the cities

## Results

This analysis revealed clear differences in rainfall patterns between Seattle and New York City. Seattle experiences higher rainfall only during winter months compared to New York city. However if we compare the proporation of days, Seattle has higher number of days with rainfall across the year.These findings imply that while Seattle is rainier in terms of frequency, New York City often receives more total rainfall.

---

## Authors

- Rashmi Kamath - [@rkamatn](https://github.com/rkamatn)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- Libraries used: pandas,numpy,matplotlib,seaborn
- Models used: scikit-learn,statsmodels
- References :Wikipedia
- Data Source: National Oceanic and Atmospheric Administration (NOAA),Global Historical Climatology Network Daily (GHCND)
