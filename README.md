# USA Economic data 2023 with the use of Fred API

## Overview

This Python script demonstrates how to access and analyze economic data from the Federal Reserve Economic Data (FRED) database using the FRED API. The code goes through various steps, including data retrieval, manipulation, and visualization. It specifically focuses on unemployment and labor force participation rates in the United States. To access the FRED API, this code utilizes the Kaggle Secrets feature to securely store the API key.


## Prerequisites
To run the script, you'll need the following prerequisites:

Python 3.x
Kaggle account for storing secrets
FRED API key (stored as a Kaggle secret)

## Getting Started
Clone this repository to your local machine or download the script.
Install the necessary Python libraries using pip install pandas numpy matplotlib plotly fredapi.

## Code Explanation
### 1. Importing Libraries

The script starts by importing essential Python libraries for data manipulation, plotting, and handling time-related functionality.

### 2. Setting DataFrame Options

It configures Pandas to display a maximum of 500 columns in DataFrames, ensuring that a large number of columns can be viewed.

### 3. Accessing API Key from Kaggle Secrets

The script securely retrieves the FRED API key from Kaggle Secrets and stores it in the fred_api variable.

### 4. Creating a FRED Object
A FRED object is created using the API key obtained in step 3. This object is used to interact with the FRED database.

### 5. Search for Economic Data
The script performs a search for economic data related to the S&P 500 using the fred.search function. The search results are stored in the df DataFrame.

### 6. Plotting Raw Data
The script retrieves and plots the S&P 500 data using the fred.get_series function and the plot function, displaying a time series plot of the S&P 500 data.

### 7. Searching for Unemployment Data
The script searches for unemployment-related data and stores the results in the unemployement_resuts DataFrame.

### 8. Filtering Unemployment Data

It filters the unemployment data to include only data with seasonal adjustments and in percentage units. The script narrows down the results to those with "Unemployment Rate" in the title.

### 9. Creating a DataFrame for State Unemployment Rates

The script iterates through the filtered unemployment data and creates a DataFrame called unemployment_states containing unemployment rates for different U.S. states.

### 10. Plotting NaN Values by Year

It plots the number of NaN (missing) values in the unemployment data by year.

### 11. Dropping NaN Values

The script drops rows with NaN values from the unemployment_states DataFrame.

### 12. Renaming State Names

It renames the columns of the unemployment_states DataFrame to include the full state names.

### 13. Plotting Unemployment Rates by States

It uses Plotly Express to create line plots of unemployment rates by states.

### 14. Plotting May 2020 Unemployment Rates

It creates a horizontal bar plot of unemployment rates for May 2020 for various states.

![download (1)](https://github.com/Ethann93/Ultra-Marathon/assets/133777296/621028b4-7d25-4e30-a2bc-3ca4b9345d99)

### 15. Pulling Participation Rate Data

The script searches for labor force participation rate data and filters it for seasonally adjusted data in percentage units.

### 16. Creating a DataFrame for State Participation Rates

It creates a DataFrame called Participation_states containing labor force participation rates for different states.

### 17. Renaming State Names for Participation Rates

The script renames the columns of the Participation_states DataFrame to include the full state names.

### 18. Changing District of Columbia's Name

It changes the name of the "District of Columbia" column to "The District of Columbia."

### 19. Plotting Participation Rates by States

It uses Plotly Express to create line plots of labor force participation rates by states.

### 20. Plotting Unemployment vs. Participation Rates

The script creates a 10x5 grid of subplots to compare unemployment and participation rates for various states from 2020 to 2023.

![download](https://github.com/Ethann93/Ultra-Marathon/assets/133777296/abceb8b7-d5a6-4e63-8610-2e76881d8ed9)


## Conclusion

This code provides a comprehensive example of how to use the FRED API to access and analyze economic data, specifically related to unemployment and labor force participation rates in the United States. It includes data retrieval, data cleaning, and visualization of the economic data for different states and time periods.
