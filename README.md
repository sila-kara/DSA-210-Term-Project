# DSA210-Term-Project: "Analysis of the Impact of Education Level, Demographic Factors, and Inflation on Wage Trends (2000-2022)"
This project was prepared by Sıla Kara as a term project for the DSA 210 course at Sabancı University in the 2025 Spring semester. It examines the impact of education level and demographic factors on wage disparities, as well as compares how individuals with different education levels have been affected by inflation over the years from 2000 to 2022.

---

# Contents
- [Motivation](#motivation)
- [Project Goal](#project-goal)
- [Data Collection](#data-collection)
- [Data Sources](#data-sources)

---

## **Motivation**
As a university student, I have always been interested in the relationship between education, socioeconomic factors, and financial stability. Understanding how wages vary based on education level, gender, and ethnicity, and how inflation further affects these disparities, is not only important for academic research but also crucial for gaining a better understanding of the dynamics of professional life as a future employee. Through this analysis, I will have the opportunity to apply what I have learned in class and gain hands-on experience in data analysis, while also developing a deeper understanding of the socioeconomic factors underlying wage inequality.

---

## **Project Goal**
This project aims to shed light on the underlying factors of wage inequality over the years and examine the impact of inflation on this disparity. In this context, comparisons will be made regarding the wages of individuals from different groups over the years by considering factors such as education level, gender, and ethnicity. As a conclusion of this project it is aimed to identify long-term wage inequality trends and examine how education, demographics, and inflation impact economic mobility. The findings may help better understand income disparities and support future policies to reduce wage gaps.

---

### **Data Collection**

For this project, data was collected from multiple publicly available sources to ensure a comprehensive and reliable dataset. The main steps in the data collection process were as follows:

1. **Researching Available Datasets:** I explored various sources, including Kaggle, government economic databases, and academic repositories, to find relevant datasets on wages and inflation. Keywords such as "historical wage data," "inflation rates dataset," and "wage inequality statistics" were used to search for structured datasets.

2. **Selecting the Most Relevant Data:** After reviewing multiple datasets, I prioritized those that covered the years 2000-2022 and included necessary details such as wage levels by education, gender, and ethnicity, along with annual inflation rates. Datasets with missing critical information or inconsistencies were excluded.

3. **Downloading and Storing Data:** The chosen datasets were downloaded in CSV format from Kaggle. To keep the data organized, all files were stored in a structured directory, ensuring easy access during the preprocessing phase.

---

## **Data Sources**
### **1. Wage Data: Annual (1973-2022) wages categorized by education level, gender, and ethnicity**
- **Data:** `wages_by_education.csv` [https://github.com/sila-kara/DSA-210-Term-Project/blob/main/wages_by_education.csv]
- **Data Source:** [https://www.kaggle.com/datasets/asaniczka/wages-by-education-in-the-usa-1973-2022/data?select=wages_by_education.csv]

#### **Description**
The `wages_by_education.csv` file contains **annual median wages** categorized by education level, gender, and ethnicity. This dataset is used to analyze **wage disparities** across different demographic groups and education levels.

#### **Structure (Columns)**
| Column | Description |
|--------|------------ |
| `Year` | The recorded year (2000-2022). |
| `less_than_hs` | Median annual wage for individuals with less than a high school education. |
| `high_school` | Median annual wage for individuals with a high school diploma. |
| `some_college` | Median annual wage for individuals with some college education but no degree. |
| `bachelors_degree` | Median annual wage for individuals with a bachelor's degree. |
| `advanced_degree` | Median annual wage for individuals with an advanced degree (master's, PhD). |
| `men_less_than_hs` - `men_advanced_degree` | Median wages for men at each education level. |
| `women_less_than_hs` - `women_advanced_degree` | Median wages for women at each education level. |
| `white_men`, `black_men`, `hispanic_men` | Wage data segmented by ethnicity and gender. |
| `white_women`, `black_women`, `hispanic_women` | Wage data segmented by ethnicity and gender. |

#### **Usage in the Project**
- **Compare wage growth across different education levels**.
- **Analyze wage disparities between demographic groups** (gender and ethnicity).
- **Combine with inflation data to calculate real wages** and examine purchasing power changes over years across different groups.

---
### **2. Inflation Data: Monthly CPI indexes from 1913 to 2022, as a representation of inflation changes over the years**
- **Data:** `inflation.csv` [https://github.com/sila-kara/DSA-210-Term-Project/blob/main/inflation.csv]
- **Data Source:** [https://www.kaggle.com/datasets/neelgajare/usa-cpi-inflation-from-19132022/data]

#### **Description**
The `inflation.csv` file contains historical monthly inflation rates (Consumer Price Index - CPI) from 1913 onward. These inflation values are used to adjust nominal wages to real wages, allowing for a better analysis of purchasing power over years.

#### **Structure (Columns)**
| Column | Description |
|--------|-------------|
| `Year` | The year of the recorded inflation rates (from 1913 onward). |
| `Jan` - `Dec` | The monthly inflation rates for each month of the respective year. |
| `CPI` | The average Consumer Price Index for the given year (computed by averaging monthly values). |

#### **Usage in the Project**
- Used for **analyzing the relationship between inflation and wage growth**.
- Helps **demonstrate how inflation affects wage disparities across different educational backgrounds and demographic groups**.
