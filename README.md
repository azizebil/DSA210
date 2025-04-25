# 🌤️ Weather and Productivity Analysis

## 📚 Project Overview
This project explores the impact of daily weather conditions and exam periods on productivity, defined by time spent on **work-related applications** (IDEs, Google Docs, email, etc.). We combine personal screen time, sleep data, and daily weather statistics to uncover behavior patterns.

---

## 📂 Datasets

### 1️⃣ Weather Data
🌦️ Collected from **Meteoroloji Genel Müdürlüğü (General Directorate of Meteorology)**:
- 📅 **Date (YYYY-MM-DD)**
- 🌡️ **Temperature (°C)**
- 💧 **Humidity (%)**
- 🌧️ **Precipitation (mm)**
- ☁️ **Cloud Cover (%)**
- 🌬️ **Wind Speed (m/s)**
- 🌤️ **Weather Condition** (Clear, Rain, Snow, Cloudy, etc.)
- ☀️ **Sunlight Hours** (hours of daylight per day)

### 2️⃣ Screen Time & Productivity Data
📱 Data from phone/computer apps + manually logged sleep:
- 📅 **Date (YYYY-MM-DD)**
- ⏳ **Total Screen Time** (hours)
- 💼 **Time on Work Apps** (Google Docs, IDEs, email)
- 📱 **Time on Social Media** (Instagram, Twitter, etc.)
- 🎮 **Time on Gaming Apps**
- 🎥 **Time on YouTube/Entertainment**
- 🔄 **Break Frequency**
- 🛌 **Sleep Duration**
- 📝 **Exam Period** (binary: exam week or not)

---

## 🎯 Research Questions

1. 🌦️ Does daily weather condition (e.g., clear, rainy, cloudy) affect time spent on work-related applications?
2. 📱 Is social media usage correlated with temperature changes?
3. ☁️ Does cloudy weather lead to increased gaming time?
4. ☀️ Does more sunlight increase time spent on work apps?
5. 📝 Do exam periods influence the relationship between weather and work app usage?

---

## 🧪 Hypotheses

- **Null Hypothesis (H₀)**: Weather conditions and exam periods have no significant impact on time spent on work apps.
- **Alternative Hypothesis (H₁)**: Weather conditions and exam periods significantly affect time spent on work apps.

(Separate hypotheses for other categories like gaming, social media, etc.)

---

## 🛠️ Methods

### 📥 Data Collection
- 🌦️ Scrape daily weather reports.
- 📱 Export weekly screen time and sleep data.
- 📝 Manually record exam periods.

### 🔎 Data Preparation & Analysis
- 🧹 Data Cleaning
- 📊 Exploratory Data Analysis (EDA)
- 🧪 Statistical Testing:
  - 📈 ANOVA (weather vs productivity)
  - 🔍 Chi-Square Test (exam vs dominant activity)

### 🤖 Optional:
- Categorize days into work-dominant or entertainment-dominant.

---

## 🗓️ Data Collection Period
- Collected **daily over a 14-week period**, covering normal weeks and exam periods.

---

## 🎯 Expected Outcomes
- 🔍 Discover weather patterns affecting productivity.
- 🧠 Behavioral insights based on environmental & academic factors.
- 🛠️ Build a predictive model linking weather/calendar to productivity.

---

# 📊 Results Summary

### ANOVA: Weather vs Productivity
- 🧮 F-statistic: (insert your value)
- 📈 p-value: (insert your value)
- **Interpretation**:  
  (State whether productivity differs significantly across weather types.)

---

### Chi-Square: Exam Period vs Dominant Activity
- 🧮 Chi-square statistic: (insert your value)
- 📈 p-value: (insert your value)
- **Interpretation**:  
  (State if exam periods affect dominant activity choice.)

---

> 📄 Full results and plots: [results.md](results.md)

---

## 📈 Visualizations
- 📊 Productivity and entertainment distributions
- 📦 Boxplots by weather conditions
- 🔥 Correlation heatmaps
- 📊 Bar plots: Work vs Entertainment during exams

---

## 🧩 Requirements

Install dependencies with:

```bash
pip install -r requirements.txt
