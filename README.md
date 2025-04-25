# DSA210-Term-Project: "Analysis of the Impact of Education Level, Demographic Factors and Inflation on Wage Disparities (2000-2022)"

This project was prepared by Sıla Kara as a term project for the DSA 210 course at Sabancı University in the 2025 Spring semester. It examines the impact of education level and demographic factors on real wage disparities over the years from 2000 to 2022.

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

1. **Wages by Education (wages_by_education)**
   - This dataset contains **average wages by education level and gender** for the years **2000-2022**. The data includes:
     - Education levels: Less Than High School, High School, Some College, Bachelor's Degree, Advanced Degree.
     - Gender-based wages for each education level.
   - This dataset provides information on the **average wages by education level** and serves as the foundation for our wage gap analysis.

2. **Inflation Data (inflation)**
   - The inflation dataset includes **annual inflation rates** for the years **2000-2022**.
   - Inflation rates are critical for adjusting the nominal wages to real wages. We use this data to **adjust for inflation** and make the wage data comparable across years.

---

### Preprocessing

### Objective:
The goal of preprocessing was to merge the wage data with inflation data in order to calculate **real wages**. Real wages are adjusted for inflation, providing a more accurate representation of the actual purchasing power over time.

#### Steps:

1. **Inflation Adjustment:**
   - To obtain the **real wages**, we adjusted the **nominal wages** using the **annual inflation rates**.
   - The real wage calculation formula is:
     ```
     Real Wage = Nominal Wage / (1 + Inflation Rate)
     ```
   - This allows us to **compare wages over time** without the influence of inflation, giving us the **true value** of the wages in terms of purchasing power.

2. **Data Merging:**
   - We merged the **wages_by_education** dataset with the **inflation** dataset.
   - The merging step aligned **yearly wage data** (by education level and gender) with the corresponding **inflation rates** for each year, allowing us to adjust the wages accurately.

3. **Real Wages Cleaned Dataset:**
   - Using the merged data, we created the **real_wages_cleaned** dataset, which contains **real wages** adjusted for inflation.
   - This dataset includes:
     - Real wages for each year, education level, and gender.
     - The data is now **comparable across years**, providing a true picture of wage changes over time.

---

### Why Was the Data Merged?
The merging process was essential to calculate the **real wages**, which are adjusted for inflation. Without adjusting for inflation, nominal wage differences across years would not be meaningful. By incorporating inflation rates, we ensure that the **wage comparisons** reflect the **true economic impact** over time, providing more accurate insights into the wage gap across different education levels and genders.

The final **real_wages_cleaned** dataset allowed for more accurate comparisons of **wage gaps** by **education level** and **gender**, providing a reliable foundation for hypothesis testing and further analysis.

---

## Data Analysis

### 1. Data Preprocessing

As mentioned in the **Data Sources and Preprocessing** section, we used two primary datasets:
- **Wages by Education**: This dataset contains wage information segmented by **education level** and **gender** for the years **2000–2022**.
- **Inflation Data**: This dataset includes **annual inflation rates** for the same period.

We merged these datasets to adjust the nominal wages for inflation, resulting in the **real_wages_cleaned** dataset. This dataset contains **real wages** for each year, education level, and gender, allowing for accurate comparisons over time.

---

### 2. Exploratory Data Analysis (EDA)

We analyzed the **wage gap** between **men and women** for each education level over the two time periods: **2000–2010** and **2011–2022**. The findings showed that **high education levels** had a **larger wage gap** compared to **low education levels**. Over time, the gap increased for high education levels, while low education levels remained relatively stable.

---

### 3. Visualization

We used **Bar Charts**, **Boxplots**, and **Line Charts** to visualize the **wage gap trends** and **distributions** across education levels and time periods. These visualizations helped in understanding the patterns and changes in the wage gap between men and women over the years.

---
