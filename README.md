# 🚲Yulu-Business-case
Yulu - Hypothesis Testing

## ⚡About Yulu
Yulu, India's pioneering micro-mobility service provider, has embarked on a mission to
revolutionize daily commutes by offering unique, sustainable transportation solutions.
However, recent revenue setbacks have prompted Yulu to seek the expertise of a consulting
company to delve into the factors influencing the demand for their shared electric cycles,
specifically in the Indian market.

## 💡About this business case
This project focuses on analyzing the demand for shared electric cycles in the Indian market, a strategic move by Yulu to expand its services and recover revenue. The goal is to understand the factors influencing demand, helping Yulu optimize its offerings, tailor marketing strategies, and regain profitability in a new market.

Concept Used:
- Bi-Variate Analysis
- 2-sample t-test: testing for difference across populations
- ANNOVA
- Chi-square

## 📑Data overview
- datetime: datetime
- season: season (1: spring, 2: summer, 3: fall, 4: winter)
- holiday: whether day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
- workingday: if day is neither weekend nor holiday is 1, otherwise is 0.
- weather:
  1.  Clear, Few clouds, partly cloudy, partly cloudy
  2. Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
  3. Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
  4. Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
- temp: temperature in Celsius
- atemp: feeling temperature in Celsius
- humidity: humidity
- windspeed: wind speed
- casual: count of casual users
- registered: count of registered users
- count: count of total rental bikes including both casual and registered

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Insights and Recommrndations
Step 1: Exploratory Data Analysis (EDA)

A. Examine dataset structure, characteristics, and statistical summary.

Insights:

The dataset contains detailed information on bike rentals, including various attributes such as date, weather, season, and rental counts. The dataset appears to have no missing values or duplicate records, ensuring data quality.

Recommendations:

Continue to ensure data quality by regularly checking for missing values and duplicates. This will help in maintaining accurate and reliable data for future analysis.

Implement automated data quality checks in the data pipeline to detect and rectify any anomalies promptly.

B. Identify missing values and perform imputation using an appropriate method.

Insights:

No missing values were found in the dataset.

Recommendations:

Maintain consistent and complete data entry practices to avoid missing values in future datasets.

If missing values do occur, establish a protocol for imputation using appropriate methods to ensure data integrity.

C. Identify and remove duplicate records.

Insights: No duplicate records were found in the dataset.

Recommendations: Implement validation checks to prevent duplicate entries in the system. This ensures the accuracy of usage statistics and demand forecasting.

D. Analyze the distribution of Numerical & Categorical variables

Insights:
Numerical variables show varying distributions, some of which may be skewed. Categorical variables have different levels of frequency, indicating varied usage patterns.

Recommendations:
Consider transforming skewed numerical variables to normalize the data. This can improve the performance of predictive models.
For imbalanced categorical variables, consider strategies like targeted marketing or promotions to balance usage across different categories.

e. Check for Outliers and deal with them accordingly.

Insights:
Outliers were detected and removed based on the IQR method.

Recommendations:
Investigate the causes of outliers to determine if they indicate data issues or true anomalies. Implement policies to address data entry errors.


Step 2: Establish a Relationship between the Dependent and Independent Variables

Insights:
The correlation heatmap indicates some highly correlated numerical variables.

Recommendations:
Remove or combine highly correlated variables to prevent multicollinearity, which can skew the results of predictive models.
Consider using techniques like Principal Component Analysis (PCA) to reduce the dimensionality of the data while preserving important information.


Step 3: Significant difference between the number of bike rides on Weekdays and Weekends

Insights:
A significant difference in bike rides between Weekdays and Weekends was found.

Recommendations:
Increase bike availability during weekends to meet higher demand.
Develop specific marketing strategies for weekdays to boost rentals, such as weekday promotions or partnerships with businesses for commuter benefits.


Step 4: Demand for bicycles on rent for different Weather conditions

Insights:
The demand for bicycles varies significantly with weather conditions.

Recommendations:
Adjust the fleet size and maintenance schedules based on weather forecasts to ensure availability during favorable conditions.
Provide weather-appropriate gear (e.g., raincoats, umbrellas) to customers to encourage bike rentals during less favorable weather conditions.


Step 5: Demand for bicycles on rent for different Seasons

Insights:
The demand for bicycles varies significantly with seasons.

Recommendations:
Plan for increased maintenance and resource allocation during peak seasons to ensure that the fleet is in optimal condition.
Launch seasonal marketing campaigns to capitalize on higher demand periods, such as summer or spring.

Step 6: Weather conditions during different Seasons

Insights:
Weather conditions significantly differ across seasons.

Recommendations:
Use historical weather patterns to predict bike rental demand and adjust operations accordingly.
Optimize inventory levels based on expected seasonal weather conditions to avoid under- or over-supply of bikes.


## SUMMARY AND RECOMMENDATIONS

Based on the analysis, Yulu can enhance its bike-sharing service by implementing the following strategies:

- Maintain data quality and consistency to ensure reliable analysis. Address data anomalies and manage outliers to improve the accuracy of insights.
- Optimize bike availability and maintenance schedules based on demand patterns influenced by day of the week, weather, and seasons.
- Develop targeted marketing campaigns to boost rentals during low-demand periods and capitalize on high-demand times.
- Use advanced analytics techniques to manage multicollinearity and dimensionality in the data for better predictive modeling.
By leveraging these Insights and Recommendations, Yulu can improve its operational efficiency, customer satisfaction, and overall business performance.
