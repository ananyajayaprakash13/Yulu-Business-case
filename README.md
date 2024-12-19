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

### **Step 1: Exploratory Data Analysis (EDA)**

- **A. Dataset Structure & Summary**
  - The dataset contains bike rental data (weather, season, rental counts).
  - No missing values or duplicates found.
  - **Recommendation**: Continue data quality checks to ensure reliability.

- **B. Missing Values**
  - No missing values detected.
  - **Recommendation**: Maintain data entry consistency.

- **C. Duplicate Records**
  - No duplicates present.
  - **Recommendation**: Implement validation checks for accuracy.

- **D. Distribution of Variables**
  - Skewed numerical distributions; varying categorical frequencies.
  - **Recommendation**: Normalize numerical data and balance categorical variables.

- **E. Outliers**
  - Outliers removed using IQR method.
  - **Recommendation**: Investigate outliers for potential data issues.

---

### **Step 2: Relationship Between Variables**
- **Insights**: Correlation between several numerical variables.
- **Recommendation**: Eliminate highly correlated variables using PCA for dimensionality reduction.

---

### **Step 3: Weekday vs Weekend Demand**
- **Insights**: Significant difference in bike demand between weekdays and weekends.
- **Recommendation**: Increase bike availability on weekends. Implement weekday promotions.

---

### **Step 4: Demand for Bikes Based on Weather**
- **Insights**: Demand varies significantly with weather.
- **Recommendation**: Adjust fleet size according to weather forecasts and offer weather gear.

---

### **Step 5: Seasonal Demand**
- **Insights**: Demand fluctuates with the seasons.
- **Recommendation**: Plan resource allocation and marketing during peak seasons.

---

### **Step 6: Weather Across Seasons**
- **Insights**: Seasonal weather patterns affect bike demand.
- **Recommendation**: Use historical weather data to optimize bike availability.

---

### **Summary & Recommendations**
- **Data Quality**: Ensure consistency and accuracy in the data.
- **Bike Availability**: Adjust fleet based on day, weather, and seasonal demand.
- **Marketing**: Launch targeted campaigns for weekdays and peak seasons.
- **Predictive Modeling**: Utilize advanced analytics for better forecasting and operational efficiency.

By following these recommendations, Yulu can improve service efficiency, customer satisfaction, and overall performance.
