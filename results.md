# 📄 Detailed Results and Interpretation

## 1. 📈 ANOVA Test – Weather vs Productivity

**Test:** One-way ANOVA  
**Groups compared:** Rainy days, Rain+Snow days, Clear days  
- **F-statistic:** 1.131  
- **p-value:** 0.3325  

### ✅ Interpretation:
There is **no statistically significant** difference in productivity time across different weather conditions.

➤ We **fail to reject the null hypothesis (H₀)** — this suggests that weather type (in this dataset) does not have a strong measurable impact on work-related app usage.

📦 **Boxplot:**
![Weather vs Productivity](images/Productivity_Time_across_Different_Weather_Types.png)

---

## 2. 🔍 Chi-Square Test – Exam Period vs Dominant Activity

**Test:** Chi-Square Test of Independence  
**Variables:**  
- Exam Period (Yes/No)  
- Dominant Activity (Work vs Entertainment)

- **Chi-square statistic:** 0.259  
- **p-value:** 0.6110  

### ✅ Interpretation:
There is **no statistically significant** relationship between whether it's an exam period and whether a day is work-dominant or entertainment-dominant.

➤ We **fail to reject the null hypothesis (H₀)** — suggesting that the exam period, in this case, does not shift behavior significantly from entertainment to work or vice versa.

📊 **Bar Chart:**
![Exam Period Activity](images/Dominant_Activity_During_Exam_vs_Non-Exam_Periods.png)

---

## 📈 Additional Visual Insights

### Distribution of Productivity Time
![Productivity Histogram](images/Distribution_of_Productivity_Time.png)

### Distribution of Entertainment Time
![Entertainment Histogram](images/Distribution_of_Entertainment_Time.png)

### Correlation Heatmap
Shows the relationship between productivity, screen activity types, and weather-related features:
![Correlation Heatmap](images/Correlation_Heatmap.png)

---

> 🚀 These findings are preliminary and context-specific. Further analysis with more diverse data and ML techniques will strengthen interpretation.
