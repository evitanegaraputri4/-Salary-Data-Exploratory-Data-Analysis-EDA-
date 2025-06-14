# Salary Data Exploratory Data Analysis (EDA)

## Project Overview
This project presents an exploratory data analysis (EDA) of a salary dataset to uncover key insights about workforce demographics, salary distributions, and factors affecting employee compensation. The dataset includes attributes such as Age, Gender, Education Level, Job Title, Years of Experience, and Salary. The main objective is to clean, analyze, and visualize the dataset to answer important business questions and highlight relationships between variables that influence salaries.

---

## Tools and Libraries
- Python
- Pandas
- Matplotlib
- Seaborn
- Statsmodels
---
## Step-by-Step Process

1. **Data Loading and Initial Inspection**  
   - Loaded data using `pandas.read_csv()`.  
   - Explored dataset shape and data types with `.info()` and `.shape`.  
   - Used `.describe()` to summarize numeric and categorical columns.

2. **Handling Missing Values**  
   - Checked missing data with `.isna().sum()`.  
   - Dropped rows containing missing values to ensure clean analysis.  
   - Verified no missing values remained after cleaning.

3. **Handling Inconsistent Data**  
   - Inspected unique values in key categorical columns (`Gender`, `Education Level`).  
   - Standardized inconsistent labels in `Education Level` (e.g., `"Bachelor's Degree"` → `"Bachelor's"`) for consistency.

4. **Handling Outliers**  
   - Visualized distributions and outliers with boxplots for numeric columns (`Age`, `Years of Experience`, `Salary`).  
   - Applied the "cap" method (clipping values at calculated upper and lower bounds based on IQR) to handle outliers in `Age` and `Years of Experience`.  
   - Rechecked boxplots post-processing to confirm successful outlier mitigation.
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

