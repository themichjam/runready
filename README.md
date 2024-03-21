# RunReady Analysis and Recommendations

The Running Weather Analysis Toolkit is a Python-based application that analyzes running logs to provide insights into how weather conditions affect running experiences. It leverages data science and machine learning techniques to offer personalized clothing recommendations for runners, ensuring they are dressed comfortably for the weather. This guide outlines the exact functionalities implemented in the toolkit as reflected in a Jupyter Notebook (.ipynb file).

## Features Overview
-Data Loading and Overview: Imports the running log dataset and displays its structure, providing an initial understanding of the available data.
-Data Visualization: Utilizes matplotlib and seaborn for generating various plots to visualize weather conditions and their effects on running experiences.
-Data Preprocessing: Cleans the dataset by handling missing values and creating dummy variables for categorical data, preparing it for further analysis.
-Correlation Analysis: Analyzes correlations between different weather parameters to understand their interdependencies.
--Predictive Modeling: Employs machine learning to predict the 'Feels Like' temperature based on other weather parameters, enhancing the clothing recommendation process.
Recommendation System: Based on historical data and current weather conditions, recommends the most suitable attire for running.

## Step-by-Step Guide

### Initial Setup
The notebook begins by importing necessary Python libraries and suppressing warnings for a cleaner output. It then loads the running log data from a CSV file, displaying the first few entries and providing a summary of the dataset's structure and contents.

### Data Visualization
Several types of visualizations are generated to explore the data:
-Histograms and violin plots to examine the distributions of temperature, wind speed, and 'Feels Like' temperature.
-Box plots to visualize the spread and outliers of the same parameters.
-A heatmap to show correlations between numerical features.
-Scatter plots and scatter matrices to visualize relationships between different weather parameters.

### Data Cleaning and Preprocessing
The notebook proceeds to clean the data, which includes handling missing values and converting categorical variables (like sky conditions and precipitation) into dummy variables. This step is crucial for preparing the data for machine learning models.

### Predictive Modeling
A machine learning model is trained to predict the 'Feels Like' temperature based on other weather conditions. The dataset is split into training and testing sets, the data is standardized, and a linear regression model is fitted. The model's performance is evaluated using the Mean Absolute Error (MAE) metric on both training and testing sets. Residuals are also plotted to assess the model's prediction errors.

### Clothing Recommendation
Finally, the notebook implements a function that uses the nearest neighbors algorithm to recommend clothing based on the current weather conditions. It compares the input conditions with historical data to find the most similar weather conditions and suggests the attire worn during those conditions.

## How to Use
To utilize the toolkit, simply input your current weather conditions into the system, and it will provide clothing options based on your previous experiences logged in the dataset. The toolkit learns from your preferences and experiences, offering more personalized and accurate recommendations over time.

Example Input:

| Clothing Item | Recommendation      |
|---------------|---------------------|
| Top, base     | Blue Nathan base    |
| Top, mid      | New Balance half zip|
| Bottom, base  | Nike unlined tights |
| Bottom, top   | nan                 |
| Head Warmth   | nan                 |
| Head Hat      | Baseball cap        |
| Hands         | nan                 |


| Condition    | Value |
|--------------|-------|
| Temp         | 45°F  |
| Feels Like   | 40°F  |
| Wind         | 5 mph |
| Sunny        | No    |
| Precip       | Light |


## Conclusion
The Running Weather Analysis Toolkit is a practical application of data science and machine learning for everyday life, particularly for runners looking to optimize their comfort based on weather conditions. By analyzing personal running logs and weather data, it provides insights and recommendations that help runners make informed decisions about their attire, ultimately enhancing their running experience.
