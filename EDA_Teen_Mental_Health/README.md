# Teen Mental Health & AI Usage — Exploratory Data Analysis

This repository contains the code and insights from an exploratory data analysis (EDA) conducted on a Kaggle dataset related to teenagers’ mental health and their interaction with AI tools. The analysis covers data cleaning, visualization, correlation analysis, feature engineering, and key behavioral trends.

---

## Project Objectives
- Explore patterns in AI tool usage among teenagers  
- Examine how factors like screen time, sleep hours, and stress levels interrelate  
- Identify potential correlations between mood, mental health indicators, and technology habits  
- Engineer new features like risk flags and age groups to support future modeling tasks

---

## Tools & Technologies
- Python (`pandas`, `matplotlib`, `seaborn`)  
- Jupyter Notebook  
- Kaggle Dataset  
- Git & GitHub

---

## Key Insights
#### 1. Missing Values
- 12009 nulls in 'ai_tool' column
- Filled using most frequently occurring (mode) value in that column ('Gemini')

#### 2. Univariate Analysis
- Gender skewed toward Male
- Age mostly 14–17
- Screen time hours peaked around 7

#### 3. Bivariate Insights
- Suggests a global trend of high AI usage today across countries, especially in USA and Canada
- All gender groups show more AI usage than non-usage, indicating overall positive adoption across genders. However, there’s a gender gap, with females having the lowest AI usage among the three.
- Age in this narrow range doesn’t significantly influence social interaction ratings
- Teens across all age groups (14 to 17) show similar screen time patterns.
- No clear linear trend, but might indicate a positive association: teens with more screen time could be experiencing higher stress, but further statistical analysis is needed to confirm this.

#### 5. Correlation
- mood and stress_level: high negative correlation (-0.93), meaning higher stress = worse mood
- used_ai_today, journaling, meditation, etc., show minimal correlation with screen time or social rating.
- Stress vs Screen Time : Slight clustering, meaning higher stress may associate with higher screen time, but not strongly
- sleep_hours and stress_level: weak negative correlation (-0.0058)
- social_interaction_rating and stress_level: very weak positive correlation (0.0026)

#### 6. Outliers
- There are no points beyond the whiskers, therefore this dataset has no age outliers
- The data is slightly right-skewed, as the box is slightly longer on the right side of the median, indicating a few more older teens in the dataset.

#### 7. Feature Engineering
- Added ‘HighRisk’ binary flag for teens having sleep hours less than 4 and stress levels higher than 5.
- Added 'AgeGroup' column for further classification into young teens and older teens
- Added 'DateSince' column for tracking days since survey

---

## Future Scope
- Develop predictive models to classify mental health risk levels  
- Implement dashboards for visual storytelling  
- Integrate time-series or sentiment analysis from social media data

---

## License

This repository is for educational and research purposes. Dataset and visuals belong to Kaggle (https://www.kaggle.com/).
