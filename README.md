# Covid-Vaccination-Prediction
Predicting Odds of Vaccination Status Using Logistic Regression


# Predicting COVID-19 Vaccination Status

## Overview
This project explores the demographic, political, and behavioral factors associated with COVID-19 vaccination uptake in the United States. Using a logistic regression model, I analyze how age, education, political affiliation, religious attendance, income, and trust in science and government influence an individual's likelihood of being vaccinated.

All data wrangling, modeling, and interpretation were conducted in **R**, with a focus on reproducibility, statistical rigor, and visual clarity.

## Dataset
The dataset is from the **Pew Research Center's American Trends Panel (ATP)**, collected in **September 2022**. It includes over 10,000 responses from a nationally representative sample of U.S. adults. The survey examines public trust in science, government, and attitudes related to COVID-19 policy and vaccination.

## Objective
To identify key **risk factors for non-vaccination** and understand how public confidence and demographics contribute to vaccine hesitancy.

## Methods

- **Data Cleaning**:
  - Replaced 98/99 placeholder codes with `NA`.
  - Removed unnecessary metadata columns.
  
- **Exploratory Analysis**:
  - Visualized vaccination rates by age, trust, confidence in science, education, and political affiliation.
  
- **Modeling**:
  - Logistic regression (`glm()` with binomial family) to predict `COVID_vaccinated` (1 = Yes, 0 = No).
  - Set reference groups for categorical predictors to reflect likely non-vaccinated segments.
  - Converted all categorical predictors to factors.

- **Model Diagnostics**:
  - Residuals vs. Fitted plot to assess model fit.
  - Pearson residuals for overdispersion check.
  - ROC curve and AUC to evaluate model accuracy.

## Key Findings

- **Age**: Younger individuals are significantly less likely to be vaccinated.
- **Education**: College graduates are more likely to be vaccinated than those with less education.
- **Political Affiliation**: Democrats are far more likely to be vaccinated than Republicans.
- **Religious Attendance**: Less frequent attendance is associated with higher vaccination rates.
- **Race**: Asian and Hispanic individuals show higher vaccination rates than White individuals.
- **Trust and Confidence**:
  - High confidence in science is strongly linked to vaccination.
  - When scientific confidence is low, trust in elected officials becomes a stronger predictor.

## Model Performance

- **AUC (Area Under Curve)**: 0.774 — indicating **moderate discriminative power**.
- **Overdispersion**: Not detected (dispersion parameter ≈ 0.99).
- **Most predictors are statistically significant**, with results interpretable via odds ratios.

## Tools

- **Language**: R
- **Libraries**: `dplyr`, `ggplot2`, `tidyverse`, `pROC`, `haven`, `reshape2`
- **Format**: R Markdown (`.Rmd`) and PDF report outputs

## Files

- `4211Final.Rmd`: Main analysis and model code
- `4211final.pdf`: Full project report
- `Predicting Covid Vaccination Status.pdf`: Presentation-style summary

## Author

**Calvin Kapral**

This project was completed independently as part of a final data science course. All work, including data cleaning, modeling, visualization, and interpretation, was done by me.
