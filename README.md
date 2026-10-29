# Income Distribution Analysis: Excel and Power BI

A data analytics mini project that cleans and analyses the **UCI Adult (Census Income) dataset** using **Excel** for data pre-processing and **Power BI** for visualization.

## Project Overview

This project studies how education, occupation, age, gender and working hours relate to earning above or below **$50K** per year. Excel is used to clean and transform the raw data, and Power BI is used to build an interactive dashboard.

- **Domain:** Human Resources / Demographic income analysis
- **Tools:** Microsoft Excel, Power BI Desktop
- **Dataset source:** [UCI Machine Learning Repository: Adult](https://archive.ics.uci.edu/dataset/2/adult)

## Dataset

| Item | Detail |
|---|---|
| File used | `adult_test.txt` |
| Raw records | 16,281 |
| Records after cleaning | 16,276 |
| Raw columns | 15 (6 numerical, 9 categorical) |
| Target field | Income (`<=50K` or `>50K`) |

## Data Pre-processing in Excel

- **Imported and structured** the raw file, removing a junk first line and adding proper column headers.
- **Removed duplicates:** 5 duplicate records.
- **Handled missing values:** `?` in Workclass, Occupation and Native_Country (1,221 rows affected) replaced with **"Unknown"**, so no records were lost.
- **Standardized formats:** trimmed leading spaces and removed the trailing full stop from Income values.
- **Calculated fields:**
  - `Income_Group`: High Income / Low Income
  - `Income_Flag`: 1 or 0, used to calculate the percentage of high earners
  - `Age_Group`: 17-24, 25-34, 35-44, 45-54, 55-64, 65+
- **Filtering and sorting** to inspect the data.
- **Pivot tables:** income split, % high income by education, income by occupation, and average hours by sex and income.

## Power BI Dashboard

- **KPI cards:** Total Records, % High Income, Average Age, Average Hours per Week
- **Charts:** income distribution donut, % earning >50K by education level (bar), % earning >50K by age group (column), share of high earners by gender (pie)
- **Interactivity:** slicers for gender, race and income group
- **DAX measures:** Total Records, High Income Count, % High Income, Avg Age, Avg Hours per Week

## Key Insights

- About **23.6%** of people earn more than $50K.
- **Education** shows the strongest link to income: Prof-school (75.2%) and Doctorate (69.1%) have the highest share of high earners, compared with 15.7% for HS-grad.
- High earners work **longer hours** than low earners.
- The share of high earners rises with age, and is highest around ages 45 to 54.
- Findings describe patterns in the data and do not prove causation.



## Repository Contents

| Folder | Contents |
|---|---|
| `data/` | Raw and cleaned data, dataset source |
| `excel/` | Cleaned dataset with pivot tables |
| `powerbi/` | Power BI file (.pbix) and exported report (.pdf) |
| `docs/` | Project documentation |

## Limitations

- The data is from the **1994 US Census**, so it may not reflect current incomes.
- There is no date field, so time trends can't be analysed.
- Some values are capped in the source (for example Capital_Gain = 99,999).

## Author

**[Rishikesh Vinod]**: Data Analytics Mini Project
