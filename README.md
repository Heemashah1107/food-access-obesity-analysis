# Food Access & Adult Obesity Rates in Chicago

A data analysis project examining whether living in a food desert is linked to higher adult obesity rates across Chicago.

## Overview

This project merges two public health datasets to study the relationship between food access and obesity at the neighborhood level. The analysis covers 840 Chicago census tracts and finds that tracts classified as food deserts have a statistically significant 8.3 percentage point higher adult obesity rate than tracts with better food access.

This was completed as a group project for DSC 510 (Health Data Science) at DePaul University, with Anas Kapadia. My contributions covered the data work and statistical analysis: merging and cleaning the datasets, running the descriptive statistics and regression, and building the visualization.

## Data Sources

- **[CDC PLACES](https://data.cdc.gov/500-Cities-Places/PLACES-Local-Data-for-Better-Health-Census-Tract-D/cwsq-ngmh/about_data)** — model-based local health outcome estimates, including adult obesity prevalence by census tract
- **[USDA Food Access Research Atlas](https://www.ers.usda.gov/data-products/food-access-research-atlas/download-the-data)** — food desert (LILA: Low-Income, Low-Access) classification by census tract

Raw source files aren't included in this repo since they're large public datasets — they can be downloaded directly from the links above.

## Method

1. Matched the two datasets on Census Tract FIPS codes, converting codes to a consistent numeric format
2. Merged using XLOOKUP in Excel and isolated the obesity indicator from the broader CDC dataset
3. Removed rows with missing values, leaving a clean analysis set of 840 Chicago census tracts
4. Ran descriptive statistics on adult obesity rates
5. Ran a linear regression to test whether food desert (LILA) status predicts adult obesity prevalence
6. Built a scatter plot with a fitted regression line to visualize the relationship
7. Proposed an interactive dashboard concept for public health policymakers to monitor obesity and food access by tract

## Key Findings

**Descriptive statistics:** Mean adult obesity rate across the 840 tracts was 25.23%, ranging from 1.4% to 92.2% (SD = 23.56) — obesity is far from evenly distributed across Chicago neighborhoods.

**Regression results:**

| Variable | Coefficient | p-value |
|---|---|---|
| Intercept | 24.739 | — |
| Food Desert (LILA = 1) | 8.307 | 0.015 |

Model fit: R² = 0.007

Adults living in food deserts had obesity rates **8.3 percentage points higher** than adults in areas with better food access, and the relationship was statistically significant (p = 0.015 < 0.05). The low R² is expected — obesity is shaped by many factors beyond food access alone (income, physical activity, healthcare access, built environment) — but the result confirms food access is one measurable, significant contributor to obesity disparities in Chicago.

## Why It Matters

In Chicago, more than 500,000 residents, concentrated on the South and West sides, live in food deserts. This analysis turns that into a measurable health outcome and supports two proposed interventions aligned with the CDC's HI-5 framework: a Healthy Corner Store Initiative and a Mobile Produce Market Program, targeting the census tracts identified as highest-risk in this dataset.

## Tools Used

Microsoft Excel (XLOOKUP, descriptive statistics, linear regression, data visualization)

## Files

- `descriptive_and_regression.xlsx` — cleaned dataset, descriptive statistics, and regression analysis
- `chart1.xlsx` — scatter plot source data and chart
- `scatter_plot.png` — final visualization of the food access / obesity relationship
- `analysis_and_regression.pdf` — written breakdown of methodology and results
- `Final_Written_Project_DSC_510__group_8.pdf` — full final project paper, including literature review and proposed intervention

## About

DSC 510: Health Data Science, DePaul University — March 2026
Instructor: Prof. Casey Bennett
Group 8: Heema Shah, Anas Kapadia

**Heema Shah** — MS Health Informatics, DePaul University
[LinkedIn](https://www.linkedin.com/in/heemashah1107/)  

