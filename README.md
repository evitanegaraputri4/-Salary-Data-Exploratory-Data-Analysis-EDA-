# Salary Data Exploratory Data Analysis (EDA)

## Project Overview
This project involves conducting an exploratory data analysis (EDA) on a salary dataset containing information about employee demographics, job titles, experience, and salaries. The goal is to clean the data, analyze key relationships, and visualize insights that can help understand the factors affecting salary distributions.

---

## Tools Used
- Python
- Pandas
- Matplotlib
- Seaborn
- Statsmodels (for multicollinearity check)

---

## Data Cleaning & Preparation
- Loaded and inspected the dataset for structure, data types, and missing values.
- Removed rows containing missing values to maintain data quality.
- Standardized inconsistent data entries, such as variations in the "Education Level" field.
- Identified and handled outliers in `Age` and `Years of Experience` using the capping method.

---
## Exploratory Data Analysis (EDA)

### 1.  What is the distribution of salaries in the dataset?
- Visualized distributions of `Age`, `Years of Experience`, and `Salary` using histograms with kernel density estimates (KDE).  
- **Insight:** Majority of employees are between 25 and 40 years old. Experience is skewed towards fewer years, and salaries mostly range between $50,000 and $150,000 with a wide spread.

### 2.  How does Salary vary by Gender?
- Boxplots show how salary varies by gender categories (`Male`, `Female`, `Other`).  
- **Insight:** Male employees tend to have a wider salary range and higher median salaries. The "Other" category shows a high median salary but contains fewer records.

### 3. How does Education Level impact Salary?
- Compared salary distributions across education levels using boxplots.  
- **Insight:** Higher education levels such as Master's and PhD are associated with higher salaries, while High School level employees generally earn less.

### 4. What is the relationship between Years of Experience and Salary?
- Scatterplots and regression plots show the correlation between years of experience and salary, segmented by gender.  
- **Insight:** Salary increases with years of experience, and male employees generally earn more than female or other genders with similar experience levels.

### 5. Which Job Titles have the highest average salaries?
- Aggregated average salaries by job titles and displayed the top 10 highest paying roles using a bar chart.  
- **Insight:** Executive roles like CEO, Chief Technology Officer, and Directors are the highest paying positions.

### 6. What is the distribution of Age and how does it correlate with Salary?
- Scatterplots visualize salary in relation to age and gender.  
- **Insight:** Salary tends to increase with age, likely due to accumulated experience. Gender salary gaps are also noticeable.

### 7.  Is there multicollinearity between Age and Years of Experience?
- Calculated Variance Inflation Factor (VIF) for `Age` and `Years of Experience` to assess multicollinearity.  
- **Insight:** Both variables exhibit moderate multicollinearity (VIF ~5.7), expected since age and experience are related.

---

## Contact
For questions or feedback, please reach out at [your email or LinkedIn].

