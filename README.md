# NHL Goalie Performance Modeling

## Project Overview
This project analyzes how NHL team defensive systems influence traditional goalie statistics, with save percentage used as the primary response variable. The goal was to evaluate whether team-level defensive context helps explain variation in goalie save percentage.

## Research Question
How do NHL team defensive systems influence traditional goalie statistics?

## Data
The final dataset combined MoneyPuck goalie data, MoneyPuck team data, and NHL Edge goalie data from the 2008-09 through 2024-25 NHL seasons. Each row represents a goalie-team-season observation. The final cleaned dataset contained 1,230 observations and 151 variables.

Raw data files are not included in this repository. The `data/README.md` file documents the sources and cleaning process.

## Tools Used
- R
- tidyverse
- tidymodels
- ggplot2
- glmnet
- broom
- GGally
- car
- ggcorrplot
- janitor
- readxl
- stringr

## Methods
- Cleaned and standardized player names, team abbreviations, and season formats across multiple data sources
- Engineered per-game and rate-based team defensive variables
- Filtered low-sample goalie observations to improve reliability
- Conducted exploratory data analysis on save percentage, GAA, team defense metrics, league trends, and correlations
- Fit multiple linear regression, lasso regression, principal component regression, and ridge regression models
- Evaluated multicollinearity, regression diagnostics, and train/test performance
- Compared models using RMSE, R-squared, and MAE

## Key Results
The lasso-informed regression explained a moderate amount of variation in save percentage, with training R-squared of 0.472 and adjusted R-squared of 0.460. On the test set, PCR, lasso-selected regression, and penalized lasso performed similarly, with RMSE values around 0.0121.

Overall, the results suggest that team defensive context is meaningfully related to goalie save percentage, but it does not fully explain goalie performance. Traditional goalie statistics should be interpreted alongside team defensive context rather than as purely individual measures.

## Reproducibility Note
Raw data files are not included in this public repository. The R Markdown files document the full cleaning, exploratory analysis, modeling, diagnostics, and validation workflow. Files are organized in the order they were used:

1. `01_data_cleaning.Rmd`
2. `02_eda.Rmd`
3. `03_modeling_diagnostics_validation.Rmd`

## Repository Structure
- `scripts/`: R code for data cleaning, EDA, modeling, diagnostics, and validation
- `docs/`: data dictionary and supporting documentation
- `outputs/`: selected model summaries and results
- `report/`: final written capstone report
- `data/`: data source documentation only

## Business and Analytics Relevance
This project demonstrates an end-to-end analytics workflow, including data cleaning, feature engineering, model comparison, validation, diagnostics, and communication of findings. The workflow is relevant to data analyst roles involving ETL-style data preparation, predictive modeling, performance evaluation, and data-informed decision support.
