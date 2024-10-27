# Ultra Marathon Running Data - A Comprehensive EDA

## Project Description

This project provides an extensive exploratory data analysis (EDA) on ultra-marathon race records collected over two centuries (1798–2022). The primary goal of this project is to uncover patterns and insights in ultra-marathon running, including runner demographics, performance metrics, and seasonal patterns, aiming to understand athlete performance trends.

In analyzing this vast dataset, we aim to visualize trends and answer intriguing questions about ultra-marathon running. This project is valuable for athletes, coaches, sports scientists, and enthusiasts interested in long-distance running data and insights.

## Dataset
- **Dataset Name:** Two Centuries of Ultra-Marathon Races
- **File Name:** [TWO_CENTURIES_OF_UM_RACES.csv](https://www.kaggle.com/datasets/aiaiaidavid/the-big-dataset-of-ultra-marathon-running
)
- **Key Features Explored:** Event distance/length, Event date, Athlete demographics, Athlete performance, and Average speed.

## Steps Performed in the Analysis
1. **Loading and Basic Exploration**
   - Loaded the dataset and displayed the first few rows to understand the structure.
   - Checked data types, dimensions, and unique values.

2. **Filtering and Subsetting**
   - Focused on 50 km and 50 mi races, specifically from 2020, within the USA.
   - Created a filtered DataFrame (`df2`) with relevant rows and cleaned up the 'Event name' column for easier interpretation.
   
3. **Feature Engineering**
   - **Calculating Athlete Age:** Subtracted the `Athlete year of birth` from 2020 to derive `Athlete age`.
   - **Extracting Performance Time:** Split the `Athlete performance` column to retain the time component.
   - **Dropping Irrelevant Columns:** Removed columns not required for further analysis, such as `Athlete club`, `Athlete country`, etc.
   
4. **Data Cleaning**
   - Dropped rows with missing values and duplicate entries to ensure data integrity.
   - Converted data types of columns to appropriate formats for analysis.
   
5. **Column Renaming**
   - Renamed columns to more descriptive names (e.g., `Year of event` to `year`, `Athlete performance` to `athlete_performance`) for better readability.

6. **Feature Transformation**
   - **Race Season Categorization:** Derived the `race_season` column based on the month of each race to group races into Winter, Fall, Summer, and Spring.
   - **Data Subsetting:** Created a subset of relevant columns for analysis (stored as `df3`).

## Data Visualizations and Insights
1. **Race Distribution Analysis**
   - Visualized the distribution of `race_length` and `athlete_gender` to understand race demographics.
   - Generated a histogram to compare `athlete_gender` distribution across different race lengths.

2. **Performance Analysis**
   - Created violin plots to analyze athlete speed distribution by gender and race length.
   - Aggregated and analyzed average speed data by `athlete_age` to identify age groups with highest and lowest average speeds.

3. **Seasonal Performance Trends**
   - Explored seasonal trends by calculating average athlete speed across different seasons.
   - Compared the mean and count of `athlete_average_speed` for each season, with a focus on 50 mi races.

## Summary of Findings
- **Age Influence on Speed:** Identified age groups with the highest and lowest average speeds for 50 mi races, revealing age-related performance trends.
- **Seasonal Performance Variations:** Observed that athlete speed varies significantly by season, with peak performance in [specific seasons if observed].
- **Gender Distribution in Races:** Provided a breakdown of gender representation in different race lengths, highlighting potential trends in gender participation.
