# Weather and Productivity Analysis

## Project Overview

This project explores the impact of daily weather conditions on productivity, specifically defined as the time spent on **work-related applications** (e.g., IDEs, Google Docs, email). By combining personal screen time and sleep data with weather statistics, the study aims to reveal how environmental factors—alongside academic events like exams—affect daily behavior and focus levels.

## Datasets

### 1. Weather Data

Weather data will be sourced from **Meteoroloji Genel Müdürlüğü (General Directorate of Meteorology)**. The dataset includes:

- **Date (YYYY-MM-DD)**
- **Temperature (°C)**
- **Humidity (%)**
- **Precipitation (mm)**
- **Cloud Cover (%)**
- **Wind Speed (m/s)**
- **Weather Condition** (Clear, Rain, Snow, Cloudy, etc.)
- **Sunlight Hours** (hours of daylight per day)

### 2. Screen Time & Productivity Data

Screen time data will be gathered from both phone and computer applications. Sleep data will also be recorded. The dataset includes:

- **Date (YYYY-MM-DD)**
- **Total Screen Time** (hours)
- **Time on Work Apps** (Google Docs, IDEs, email)
- **Time on Social Media** (Instagram, Twitter, etc.)
- **Time on Gaming Apps**
- **Time on YouTube/Entertainment**
- **Break Frequency**
- **Sleep Duration**
- **Exam Period** (binary: exam week or not)

## Research Questions

1. Does daily weather condition (e.g., clear, rainy, cloudy) affect time spent on work-related applications?
2. Is social media usage correlated with temperature changes?
3. Does cloudy weather lead to increased gaming time?
4. Does more sunlight increase time spent on work apps?
5. Do exam periods influence the relationship between weather and work app usage?

## Hypothesis

- **Null Hypothesis (H0)**: Weather conditions and exam periods have no significant impact on the time spent on work-related applications.
- **Alternative Hypothesis (H1)**: Weather conditions and exam periods significantly affect the time spent on work-related applications.

Separate hypotheses will also be tested for other screen time categories.

### Data Collection
[📁 View Data Folder](./data)

- Weather data will be scraped daily from the [General Directorate of Meteorology](https://www.google.com/search?client=safari&rls=en&q=meteoroloji+genel+m%C3%BCd%C3%BCrl%C3%BC%C4%9F%C3%BC&ie=UTF-8&oe=UTF-8).
- Screen time and sleep data will be exported weekly from device usage tracking tools.
- Exam dates will be manually logged.

### Data Preparation and Analysis

1. **Data Cleaning**: Remove missing values, format dates, and normalize features.
2. **Exploratory Data Analysis (EDA)**:
   - Visualize distributions and time trends.
   - Use heatmaps and boxplots to explore relationships.
3. **Statistical Analysis**:
   - ANOVA: Used to test if productivity differs significantly across weather conditions.
   - Chi-Square Test: Examined if exam periods influence dominant activity patterns.
   - Correlation Matrix: Explored relationships between weather features, productivity, sleep, and screen time.
4. **Optional**: Classification of days into work-dominant or entertainment-dominant using thresholds on work app usage.

## Data Collection Period

The data will be collected **daily over a 14-week period**, aligned with the academic term, and will include exam periods.

## Expected Outcomes

1. Identification of weather conditions that promote or hinder time spent on work apps.
2. Behavioral insights related to environmental and academic factors.
3. A simple predictive model estimating daily productivity based on weather and calendar features.

## Methods
- Exploratory Data Analysis (EDA)
- Correlation Heatmaps
- Statistical Hypothesis Testing:
  - ANOVA (weather vs productivity)
  - Chi-Square Test (exam period vs dominant activity)

## Results Summary

### ANOVA: Weather vs Productivity
- F-statistic: (insert your value)
- p-value: (insert your value)
- **Interpretation:**  
  ➤ **No statistically significant difference** in productivity across different weather types.  
  ➤ We **fail to reject the null hypothesis**.

### Chi-Square: Exam Period vs Dominant Activity
- Chi-square statistic: (insert your value)
- p-value: (insert your value)
- **Interpretation:**  
  ➤ **No significant relationship** between exam periods and whether a day is work- or entertainment-dominant.  
  ➤ We **fail to reject the null hypothesis**.

> 📄 See full detailed results and plots here: [results.md](results.md)

## 📈 Visualizations
[View All Images](./images)

- Distribution of productivity and entertainment time
- Boxplots across weather types
- Correlation heatmap
- Bar plots for exam vs non-exam dominant activities

## Machine Learning Results: Predicting Productivity

### 🎯 Goal
Use weather, sleep, and exam indicators to predict daily **Productivity (min)** spent on work-related apps.

### Models Applied
- **Linear Regression**
- **Random Forest Regressor**

### Results Summary

| Model                | MAE (min) | R² Score |
|---------------------|-----------|----------|
| Linear Regression    | 41.7      | 0.27     |
| Random Forest        | 17.1      | 0.89 ✅  |

### Interpretation
- **Linear Regression** showed weak performance, with an R² of 0.27, indicating limited ability to model the data.
- **Random Forest Regressor** performed significantly better, achieving **R² = 0.89**, meaning it explained about 89% of the variance in productivity.
- This suggests that **weather and sleep** do contain predictive signal, and **non-linear models** are better suited to this task.

### Visualization
![Prediction vs Reality](images/ML_Prediction_vs_Reality.png)

> 📁 This plot compares predicted vs actual productivity values for both models. The closer the points are to the red reference line (y = x), the more accurate the prediction.

<!--
## Installation

To run this project locally, clone the repository:

```bash
git clone https://github.com/your-username/weather-productivity-analysis.git
