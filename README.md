# Salary Data Exploratory Data Analysis (EDA)

## Project Overview
This project presents an exploratory data analysis (EDA) of a salary dataset to uncover key insights about workforce demographics, salary distributions, and factors affecting employee compensation. The dataset includes attributes such as Age, Gender, Education Level, Job Title, Years of Experience, and Salary. The main objective is to clean, analyze, and visualize the dataset to answer important business questions and highlight relationships between variables that influence salaries.

## Data Metadata

- **Number of Rows:** 200  
- **Number of Columns:** 6

### Columns Description:

| Column Name         | Description                                           |
|---------------------|-------------------------------------------------------|
| Age                 | Age of the employee (years)                            |
| Gender              | Gender of the employee (Male, Female, Other)          |
| Education Level     | Highest education attained (e.g., Bachelor's, Master's, PhD, High School) |
| Job Title           | Employee's job role/title                              |
| Years of Experience | Total years of professional experience                |
| Salary              | Annual salary in USD                                   |


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
### Before
(https://github.com/user-attachments/assets/9d440dc1-8de6-476f-91ce-04cc9b3334a9)




3. **Handling Inconsistent Data**  
   - Inspected unique values in key categorical columns (`Gender`, `Education Level`).  
   - Standardized inconsistent labels in `Education Level` (e.g., `"Bachelor's Degree"` → `"Bachelor's"`) for consistency.
     Before :
      ![![image](https://github.com/user-attachments/assets/3e3b4c39-7581-4972-82e6-fbfbc86a92b9)
     After :
      ![WhatsApp Image 2025-06-14 at 23 28 05_790ba5f2](https://github.com/user-attachments/assets/fbef79e8-687a-4ed8-ba93-377adeb0fb48)

4. **Handling Outliers**  
   - Visualized distributions and outliers with boxplots for numeric columns (`Age`, `Years of Experience`, `Salary`).  
   - Applied the "cap" method (clipping values at calculated upper and lower bounds based on IQR) to handle outliers in `Age` and `Years of Experience`.  
   - Rechecked boxplots post-processing to confirm successful outlier mitigation.
     Before:
     ![WhatsApp Image 2025-06-14 at 23 23 42_c15602d6](https://github.com/user-attachments/assets/3ac412c9-5a43-4ca8-bb48-ef658abb1ea9)
     After :
     ![WhatsApp Image 2025-06-14 at 23 23 59_8e8993d1](https://github.com/user-attachments/assets/5bf43381-59bf-43dc-b031-b507d127fe81)


---
## Exploratory Data Analysis (EDA)

### 1.  What is the distribution of salaries in the dataset?
- Visualized distributions of `Age`, `Years of Experience`, and `Salary` using histograms with kernel density estimates (KDE).  
- **Insight:** Majority of employees are between 25 and 40 years old. Experience is skewed towards fewer years, and salaries mostly range between $50,000 and $150,000 with a wide spread. This distribution shows a relatively young workforce with varying experience levels and salaries.
  ![image](https://github.com/user-attachments/assets/50327999-6ed0-4ce4-bdb1-e24059715347)


### 2.  How does Salary vary by Gender?
- Boxplots show how salary varies by gender categories (`Male`, `Female`, `Other`).  
- **Insight:** Male employees tend to have a wider salary range and higher median salaries. The "Other" category shows a high median salary but contains fewer records.
  ![image](https://github.com/user-attachments/assets/883d7319-fe8d-47d4-b549-49a4241d67b0)


### 3. How does Education Level impact Salary?
- Compared salary distributions across education levels using boxplots.  
- **Insight:** PhD holders have the highest median salaries but also show some outliers with lower salaries. In addition, Master's degree holders earn more on average than Bachelor's degree holders. Those with High School education tend to earn the least, with many salaries clustered at the lower end.
  ![image](https://github.com/user-attachments/assets/03140480-95a8-48a8-913b-9c2c5379da73)


### 4. What is the relationship between Years of Experience and Salary?
- Scatterplots and regression plots show the correlation between years of experience and salary, segmented by gender.  
- **Insight:** Salary increases with years of experience, and male employees generally earn more than female or other genders with similar experience levels. The scatter plot shows salary growth tends to flatten after about 15-20 years of experience. In, addition linear regression confirms the overall positive linear trend between experience and salary.
  ![image](https://github.com/user-attachments/assets/5447371f-47d9-4629-985a-1e0b10ef2b2e)
  ![image](https://github.com/user-attachments/assets/b5ffe1fd-2ab7-49cc-8da8-c07e56a7e4e0)


### 5. Which Job Titles have the highest average salaries?
- Aggregated average salaries by job titles and displayed the top 10 highest paying roles using a bar chart.  
- **Insight:** Highest average salaries are for executive and senior leadership roles:CEO and Chief Technology Officer top the list with salaries around $250,000. Other high-paying titles include Chief Data Officer, Directors, VPs of Finance and Operations.These roles show the expected hierarchy where senior leadership commands the highest pay.
  ![image](https://github.com/user-attachments/assets/362b4b7a-4a7a-4118-a476-a3e67ea3a7a4)


### 6. What is the distribution of Age and how does it correlate with Salary?
- Scatterplots visualize salary in relation to age and gender.  
- **Insight:** Salary tends to increase with age, with a similar gender pattern seen before: Male employees generally earn more across age groups.Females and others earn less on average but follow the upward trend with age. A wide spread in salary exists at almost every age, suggesting other factors also influence salary beyond age.
  ![image](https://github.com/user-attachments/assets/e6821e33-7307-42f2-9854-4fbe9390866f)


### 7.  Is there multicollinearity between Age and Years of Experience?
- Calculated Variance Inflation Factor (VIF) for `Age` and `Years of Experience` to assess multicollinearity.  
- **Insight:** Variance Inflation Factor (VIF) values are both ~5.7, which indicates moderate multicollinearity. This means Age and Years of Experience are correlated variables, which is expected since more age usually means more experience.
  ![image](https://github.com/user-attachments/assets/19820e43-01bd-4e68-8989-76534987fdd8)


