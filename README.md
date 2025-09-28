# Weather Analysis

## A brief description of what the project does and its purpose.
This project compares whether it rains more in Seattle or Portland using a 5 year historical weather data.

---

## Project Overview

Provide a short and concise overview of the project. Mention the problem it solves, the data used, and the key outcomes or findings.

- **Objective:** Clearly state the main goal of the project.
- **Domain:** (e.g., Healthcare, Finance, E-commerce, etc.)
- **Key Techniques:** (e.g., Regression, Classification, Clustering, NLP, Time Series)

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

- **Source:** Link to the data source(s) https://www.ncei.noaa.gov/cdo-web/search?datasetid=GHCND
- **Description:** Brief overview of the dataset features, size, and format
- **License:** (if applicable)

---

## Analysis

### Data Cleaning

Precipitation data is downloaded from NOAA's Climate Data Online Search tool for Seattle and Portland from the dates Jan 1 2018 to Dec 31 2022.

Name of the file that performs the data preparation: weather/code/Seattle_Portland_Weather_Data.ipynb

#### Import pandas, numpy, and matplotlib libraries
#### Load the Seattle & Portland Data set using read_csv
#### Start by looking at the head of each Dataframe using .head()
#### Check for the columns in each dataframe using .columns
#### Use the info() method to check the data types, size of the data frame, and numbers of missing values.
#### Use ‘shape’ attributes to compare the dataframe sizes.
#### Examine the ’STATION’ column
#### Check for unique stations in each dataframe using .unique()
#### Check for ‘DATE’ column and covert it to datetime using to_datetime()
#### Check for the range of dates on each dataframe using ‘min’ and ‘max’ function
#### Plot the daily precipitation for each city
#### Join the Portland and Seattle dataframes keeping the date and precipitation column using outer join
#### Create a tidy data frame for columns city and precipitation.
#### Rename the city values to ‘PORT’ and ‘SEA
#### Rename the columns to lowercase using .rename()
#### Identify the missing values using .isna().sum()
#### Count the null values in the precipitation column for Portland
#### Count the null values in the precipitation column for Seattle
#### Impute missing values by designing an algorithm to replace the null values with the mean across years of values on that day.
- Create a new column for the day of the year
- Calculate the mean precipitation for each day of the year for Seattle using groupby function
- Check for null values in the precipitation column
- Get the indices of the rows with null values in the precipitation column
- Replace the null values in precipitation to the mean values
- Check for null values in the dataframe
#### Export the clean .csv file.
Name of the cleaned csv file: data/clean_seattle_portland_weather.csv

## Results

Include a short discussion of the findings and what they imply.

---

## Authors

- Rashmi Kamath - [@rkamatn](https://github.com/rkamatn)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- Tools/libraries used
- Tutorials or papers referenced
- Inspiration or collaborators
