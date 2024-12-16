COVID-19 Virus Trends Analysis

Project Overview

This project investigates the global and country-specific trends of COVID-19 confirmed cases. It uses data from the Johns Hopkins University COVID-19 data repository to track infection trends, and visualizes these trends using R. Specifically, the analysis includes:

Downloading and processing COVID-19 data.
Analyzing the trends for a specific country (e.g., India).
Comparing trends across multiple countries (e.g., India, United States, Brazil).
Visualizing the trends using line plots.
Prerequisites

Ensure you have the following R libraries installed:

tidyverse (for data manipulation and plotting)
ggplot2 (for data visualization)
lubridate (for date handling)
httr (for downloading data)
You can install the libraries by running the following commands in R:

install.packages(c("tidyverse", "ggplot2", "lubridate", "httr"))
Steps in the Code

Step 1: Download COVID-19 Data
The data is downloaded from the Johns Hopkins University GitHub repository, which contains daily reports of confirmed COVID-19 cases globally. The URL points to the file for confirmed global cases.

Step 2: Load the Data
The CSV file is read into R and stored as a dataframe covid_data. A temporary file is used to download the data.

Step 3: Data Preprocessing
The data is reshaped into a long format using pivot_longer(), making it easier to analyze trends over time.
The column names for dates are cleaned, and the date format is adjusted using mdy() from the lubridate package.
The data is grouped by Country.Region and Date, and the total number of confirmed cases is summarized for each country on each date.
Step 4: Analyze Trends for a Specific Country (India)
The code filters the data for India, sorting it by date to visualize the trend of confirmed cases over time.

Step 5: Visualize the Trends for India
A line plot is created using ggplot2 to visualize the total confirmed COVID-19 cases in India over time.

Step 6: Compare Trends Across Countries (Optional)
If desired, trends from multiple countries can be compared. The example compares India, the United States, and Brazil. A line plot is created to visualize the trends for these three countries on the same graph, with each country assigned a different color.

Running the Code

Download and Prepare Data: When you run the script, the code will automatically download the latest COVID-19 data from the Johns Hopkins repository.
Select a Country: Modify the country name in the filter() function to analyze trends for other countries. For example, change "India" to "United States" to track trends for the United States.
Compare Multiple Countries: To compare multiple countries, modify the countries_to_compare vector. Add or remove country names as needed.
Plot Visualization: The script generates plots for both individual and multiple countries. You can save the plots or adjust the styling (e.g., change colors, labels, or axis scales) as needed.
Sample Output

COVID-19 Trend in India
A line plot showing the total number of confirmed COVID-19 cases over time in India.

COVID-19 Trends Across Countries
A line plot comparing the total confirmed COVID-19 cases over time in India, the United States, and Brazil, with each country displayed in a different color.

License

This project uses data from the Johns Hopkins University COVID-19 repository, which is publicly available. Please cite the source if you use the data in your research or reports# Investigating-COVID-19-Virus-Trends
Investigating COVID-19 virus trends involves analyzing patterns in infection rates, mutations, and global spread to understand its impact and guide public health responses. It also includes tracking vaccination progress and the emergence of new variants to inform prevention strategies
