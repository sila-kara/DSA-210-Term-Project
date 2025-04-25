# DSA210-Term-Project: "Analysis of the Impact of Education Level, Demographic Factors and Inflation on Wage Disparities (2000-2022)"

This project was prepared by **Sıla Kara** as a term project for the **DSA 210** course at **Sabancı University** in the **2025 Spring semester**. It examines the impact of education level and demographic factors on real wage disparities over the years from **2000 to 2022**.

In accordance with the goals of the project, two hypotheses will be tested:

**Hypothesis 1:** The real wage gap between men and women is significantly larger at higher education levels (Bachelor’s + Advanced) than at lower education levels (Some College + High School + Less than High School) over the period 2000–2022.

**Hypothesis 2:** For each education level, the real wage gap between White and Black individuals has not significantly changed between the two time periods: 2000–2010 and 2011–2022.

---

# Contents
- [Motivation](#motivation)
- [Project Goal](#project-goal)
- [Data Collection](#data-collection)
- [Data Sources and Preprocessing](#data-sources-and-preprocessing)
- [Data Analysis](#data-analysis)
- [Findings](#findings)
  - [EDA (Visual Summary of The Data)](#eda-visual-summary-of-the-data)
  - [Hypothesis 1: Wage Gap Between Men and Women](#hypothesis-1-wage-gap-between-men-and-women)
  - [Hypothesis 2: Wage Gap Between White and Black Individuals](#hypothesis-2-wage-gap-between-white-and-black-individuals)

---

## **Motivation**
As a university student, I have always been interested in the relationship between education, socioeconomic factors, and financial stability. Understanding how wages vary based on education level, gender, and ethnicity, and how inflation further affects these disparities, is not only important for academic research but also crucial for gaining a better understanding of the dynamics of professional life as a future employee. Through this analysis, I will have the opportunity to apply what I have learned in class and gain hands-on experience in data analysis, while also developing a deeper understanding of the socioeconomic factors underlying wage inequality.

---

## **Project Goal**
This project aims to shed light on the underlying factors of wage inequality over the years and examine the impact of inflation on this disparity. In this context, comparisons will be made regarding the wages of individuals from different groups over the years by considering factors such as education level, gender, and ethnicity. As a conclusion of this project it is aimed to identify long-term wage inequality trends and examine how education, demographics, and inflation impact economic mobility. The findings may help better understand income disparities and support future policies to reduce wage gaps.

---

## **Data Collection**

For this project, data was collected from multiple publicly available sources to ensure a comprehensive and reliable dataset. The main steps in the data collection process were as follows:

1. **Researching Available Datasets:** I explored various sources, including Kaggle, government economic databases, and academic repositories, to find relevant datasets on wages and inflation. Keywords such as "historical wage data," "inflation rates dataset," and "wage inequality statistics" were used to search for structured datasets.

2. **Selecting the Most Relevant Data:** After reviewing multiple datasets, I prioritized those that covered the years 2000-2022 and included necessary details such as wage levels by education, gender, and ethnicity, along with annual inflation rates. Datasets with missing critical information or inconsistencies were excluded.

3. **Downloading and Storing Data:** The chosen datasets were downloaded in CSV format from Kaggle. To keep the data organized, all files were stored in a structured directory, ensuring easy access during the preprocessing phase.

---

## Data Sources and Preprocessing

### Data Sources

1. **Wages by Education (https://github.com/sila-kara/DSA-210-Term-Project/blob/main/wages_by_education.csv)**
   Source: "https://www.kaggle.com/datasets/asaniczka/wages-by-education-in-the-usa-1973-2022"
   - This dataset contains **average wages by education level and gender** for the years **2000-2022**. The data includes:
     - Education levels: Less Than High School, High School, Some College, Bachelor's Degree, Advanced Degree.
     - Gender-based wages for each education level.
   - Information on **average wages by education level** was provided, which served as the foundation for the wage gap analysis.

3. **Inflation Data (https://github.com/sila-kara/DSA-210-Term-Project/blob/main/inflation.csv)**
   Source: "https://www.kaggle.com/datasets/neelgajare/usa-cpi-inflation-from-19132022"
   - The inflation dataset includes **annual inflation rates** for the years **2000-2022**.
   - Inflation rates were used to **adjust nominal wages to real wages**, making the data comparable across years.

---

### Preprocessing

### Objective:
The preprocessing aimed to merge the wage data with inflation data in order to calculate **real wages**. Real wages, adjusted for inflation, provide a more accurate representation of the actual purchasing power over time.

#### Steps:

1. **Inflation Adjustment:**
   - **Nominal wages** were adjusted using the **annual inflation rates** to obtain the **real wages**.
   - The real wage calculation formula used was:
     ```
     Real Wage = Nominal Wage / (1 + Inflation Rate)
     ```
   - This adjustment allowed for a **comparison of wages over time**, eliminating the influence of inflation and providing the **true value** of wages in terms of purchasing power.

2. **Data Merging:**
   - The **wages_by_education** dataset was merged with the **inflation** dataset.
   - The merging step aligned the **yearly wage data** (by education level and gender) with the corresponding **inflation rates** for each year, ensuring that wages were adjusted correctly.

3. **Real Wages Cleaned Dataset:**
   - The **real_wages_cleaned** dataset was created using the merged data, which contained **real wages** adjusted for inflation.
   - This dataset includes:
     - Real wages for each year, education level, and gender.
     - The data is now **comparable across years**, providing a true picture of wage changes over time.

---

### Why Was the Data Merged?
The merging process was essential to calculate the **real wages**, adjusted for inflation. Without this adjustment, nominal wage differences across years would not provide meaningful insights. By incorporating inflation rates, it was ensured that **wage comparisons** reflected the **true economic impact** over time, providing more accurate insights into the wage gap across different education levels and genders.

The final **real_wages_cleaned** dataset facilitated accurate comparisons of **wage gaps** by **education level** and **gender**, offering a reliable foundation for hypothesis testing and further analysis.

---

## Data Analysis

### 1. Data Preprocessing

As outlined in the **Data Sources and Preprocessing** section, two primary datasets were used:
- **Wages by Education**: This dataset contained wage information segmented by **education level** and **gender** for the years **2000–2022**.
- **Inflation Data**: This dataset included **annual inflation rates** for the same period.

These datasets were merged to adjust the nominal wages for inflation, resulting in the **real_wages_cleaned** dataset. This dataset provided **real wages** for each year, education level, and gender, enabling accurate comparisons over time.

---

### 2. Exploratory Data Analysis (EDA)

The **wage gap** between **men and women** for each education level was analyzed over two time periods: **2000–2010** and **2011–2022**. Findings indicated that **high education levels** experienced a **larger wage gap** compared to **low education levels**. Over time, the gap increased for high education levels, while low education levels remained relatively stable.

---

### 3. Visualization

**Bar Charts**, **Boxplots**, and **Line Charts** were utilized to visualize the **wage gap trends** and **distributions** across education levels and time periods. These visualizations helped in understanding the patterns and changes in the wage gap between men and women over the years.

---

## Findings

### EDA (Visual Summary of The Data)
#### Hypothesis 1: Wage Gap Between Men and Women
For the first hypothesis, **the real wage gap between men and women at different education levels** has been visualized using **five separate bar charts**. Each bar chart represents the wage gap for a specific education level. The bar charts clearly showcase the differences in wages between men and women across various education categories.

Additionally, to provide a more comprehensive comparison, the data from all five education levels was combined into a **single line chart**. This chart illustrates the changes in wage gaps across the years for both men and women, allowing for an easier visual comparison of trends.

#### Hypothesis 2: Wage Gap Between White and Black Individuals
For the second hypothesis, **the real wage gap between Black and White individuals at different education levels** has been visualized using a **bar chart**. This bar chart highlights the wage disparities between the two groups across each education level.

Similarly to the first hypothesis, the wage gaps for each education level were combined into a **single line chart**. This line chart depicts the wage gap trends over time for Black and White individuals, offering a clear visual comparison of how these gaps evolved across the five education levels.

#### General Insights
These visualizations provide an overall understanding of the wage gaps by education level and allow for meaningful observations about the trends in the wage disparities between different demographic groups. The detailed visualizations of wage differences between men and women, as well as Black and White individuals, present valuable insights into the nature of wage inequality over time.

The **key insights** derived from these visualizations can be found in the corresponding sections of the `.ipynb` file, which include specific commentary and overview regarding the charts.

## Hypothesis 1: Wage Gap Between Men and Women

The first hypothesis proposed that the **real wage gap** between men and women is significantly larger at **higher education levels** (Bachelor’s + Advanced) compared to **lower education levels** (Some College + High School + Less than High School) over the period 2000–2022.

### Null Hypothesis (H₀):
"There is no significant difference in the real wage gap between men and women across higher education levels (Bachelor’s + Advanced) and lower education levels (Some College + High School + Less than High School) over the period 2000–2022."

### Alternative Hypothesis (H₁):
"The real wage gap between men and women is significantly larger at higher education levels (Bachelor’s + Advanced) than at lower education levels (Some College + High School + Less than High School) over the period 2000–2022."

### Step-by-Step Explanation of Hypothesis Testing:

#### Step 1: Data Preparation
We begin by loading the dataset containing real wage information for different education levels and time periods. The data spans 2000–2022, with information on men and women in various education categories:
- **Lower Education Levels**: Less than High School, High School, Some College
- **Higher Education Levels**: Bachelor’s Degree, Advanced Degree

#### Step 2: Defining Education Levels
To test the hypothesis, we divide the education levels into two groups:
- **Higher Education Levels**: Bachelor’s Degree and Advanced Degree
- **Lower Education Levels**: Some College, High School, and Less than High School

#### Step 3: Wage Gap Calculation
For each education level, we calculate the **real wage gap** between men and women. The wage gap is defined as:
'Wage Gap = Average Wage of Men - Average Wage of Women'

We calculate the wage gap for both higher and lower education levels over the entire period (2000–2022).

#### Step 4: Performing the Two-Sample T-Test
We perform a **two-sample t-test** to compare the wage gaps between higher education levels and lower education levels:

- **Null Hypothesis (H₀)**: There is no significant difference in the wage gap between men and women across the higher and lower education levels.
- **Alternative Hypothesis (H₁)**: The wage gap between men and women is significantly larger at higher education levels than at lower education levels.

We perform the t-test to compare the wage gaps for each group (higher and lower education levels). The t-test compares the means of the two groups and tells us if the difference is statistically significant.

#### Step 5: Interpreting the Results
The t-test returns two main values:
- **T-statistic**: A measure of the difference between the two groups.
- **P-value**: The probability that the observed difference in means is due to chance.

If the p-value is less than the significance level (usually 0.05), we reject the null hypothesis (H₀). This indicates that the wage gap between men and women is significantly different across the two groups (higher vs lower education levels).

If the p-value is greater than 0.05, we fail to reject the null hypothesis (H₀), meaning there is no significant difference in the wage gap between the two education levels.

### Results from the Hypothesis Test:
After performing the hypothesis test, we obtained the following results:
- **T-statistic**: 32.73
- **P-value**: 3.32e-32

The p-value is extremely small (much less than 0.05), which means that we reject the null hypothesis (H₀).

### Interpretation:
Since the p-value is much smaller than the significance level (0.05), we reject the null hypothesis (H₀). This means that the real wage gap between men and women is significantly larger at higher education levels (Bachelor’s + Advanced) compared to lower education levels (Some College + High School + Less than High School) over the period 2000–2022.

Thus, the alternative hypothesis (H₁) is supported by the data: the wage gap between men and women is indeed significantly larger at higher education levels.

### Conclusion:
There is strong evidence to suggest that the real wage gap between men and women has been more pronounced at higher education levels (Bachelor’s and Advanced Degrees) compared to lower education levels (Some College, High School, and Less than High School) over the period 2000–2022.
---
## Hypothesis 2: Wage Gap Between White and Black Individuals Across Time Periods

The second hypothesis proposed that the **real wage gap** between White and Black individuals has significantly changed across two time periods: **2000–2010** and **2011–2022**, for each education level.

### Null Hypothesis (H₀):
"There is no significant difference in the real wage gap between White and Black individuals across the two time periods (2000–2010 and 2011–2022) for each education level."

### Alternative Hypothesis (H₁):
"There is a significant difference in the real wage gap between White and Black individuals across the two time periods (2000–2010 and 2011–2022) for each education level."

### Step-by-Step Explanation of Hypothesis Testing:

#### Step 1: Data Preparation
We begin by loading the dataset containing **real wage information** for different education levels and time periods. The data spans **2000–2022**, with information on White and Black individuals in various education categories:
- **Lower Education Levels**: Less than High School, High School, Some College
- **Higher Education Levels**: Bachelor’s Degree, Advanced Degree

#### Step 2: Defining Education Levels
To test the hypothesis, we define two groups of education levels:
- **Higher Education Levels**: Bachelor’s Degree and Advanced Degree
- **Lower Education Levels**: Some College, High School, and Less than High School

#### Step 3: Wage Gap Calculation
For each education level, we calculate the **real wage gap** between **White** and **Black** individuals for both time periods (2000–2010 and 2011–2022). The wage gap is calculated as:
Wage Gap = Average Wage of White - Average Wage of Black

We calculate the wage gap for both higher and lower education levels across the two periods.

#### Step 4: Performing the Two-Sample T-Test
We perform a **two-sample t-test** to compare the wage gaps between 2000–2010 and 2011–2022 for each education level:

- **Null Hypothesis (H₀)**: There is no significant difference in the wage gap between White and Black individuals across the two periods.
- **Alternative Hypothesis (H₁)**: The wage gap between White and Black individuals is significantly different across the two periods.

The t-test compares the means of the wage gaps in both periods to determine if the difference is statistically significant.

#### Step 5: Interpreting the Results
The t-test produces two key values:
- **T-statistic**: A measure of the difference between the two groups.
- **P-value**: The probability of observing the data if the null hypothesis were true.

If the p-value is less than the significance level (usually 0.05), we reject the null hypothesis (H₀), indicating that there is a significant difference in the wage gap between the two periods. If the p-value is greater than 0.05, we fail to reject the null hypothesis (H₀), meaning there is no significant difference in the wage gap between the two periods.

### Results from the Hypothesis Test:
After performing the hypothesis test, we obtained the following results for each education level:

1. **Less than High School:**
   - **T-statistic**: -1.83
   - **P-value**: 0.085
   - **Result**: Fail to reject H₀. The wage gap between White and Black individuals for this education level has not changed significantly between 2000–2010 and 2011–2022.

2. **High School:**
   - **T-statistic**: 2.06
   - **P-value**: 0.054
   - **Result**: Fail to reject H₀. The wage gap between White and Black individuals for this education level has not changed significantly, though it is close to significance.

3. **Some College:**
   - **T-statistic**: 0.15
   - **P-value**: 0.886
   - **Result**: Fail to reject H₀. There is no significant change in the wage gap between White and Black individuals for this education level across the two periods.

4. **Bachelor’s Degree:**
   - **T-statistic**: 1.15
   - **P-value**: 0.261
   - **Result**: Fail to reject H₀. There is no significant change in the wage gap between White and Black individuals for this education level.

5. **Advanced Degree:**
   - **T-statistic**: 3.39
   - **P-value**: 0.0037
   - **Result**: Reject H₀. The wage gap between White and Black individuals for this education level may be changed significantly between the two periods.

### Interpretation and Conclusion:

#### Interpretation:
The results show that the wage gap between White and Black individuals has **not changed significantly** across most education levels (Less than High School, High School, Some College, and Bachelor’s Degree) between the two time periods (2000–2010 and 2011–2022). Therefore, for these education levels, we **fail to reject the null hypothesis (H₀)**.

However, for individuals with an **Advanced Degree**, there might be a significant difference in the wage gap between White and Black individuals across the two periods. Thus, we **reject the null hypothesis (H₀)** for this group and conclude that the wage gap for individuals with an Advanced Degree has significantly changed over time.

#### Conclusion:
Even though we reject the null hypothesis for **Advanced Degree** individuals, the general hypothesis (which applies to all education levels) is affected because there is one exception where the wage gap significantly changed. This exception leads us to conclude that **overall**, we cannot confidently say there was a consistent change in the wage gap across all education levels. The results for the **Advanced Degree** group suggest that for this higher education level, there has been a change in the wage gap between White and Black individuals over time. In conclusion, the hyppthesis is not true for all education levels.
---
## Important Note
While preparing this assignment, assistance was received from artificial intelligence (ChatGPT and Gemini) in the preprocessing, visualization and hypothesis testing sections.
