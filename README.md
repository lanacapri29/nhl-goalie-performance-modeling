# NHL Goalie Performance Modeling

## Project Overview
This project analyzes how NHL team defensive context influences traditional goalie performance metrics across multiple seasons. The goal was to evaluate whether team-level defensive environment helps explain variation in goalie outcomes such as save percentage.

## Tools Used
- R
- tidymodels
- tidyverse
- ggplot2
- glmnet
- broom

## Methods
- Cleaned and combined multi-season NHL goalie and team-defense data
- Engineered standardized per-game and rate-based variables
- Removed outcome-leakage variables to protect model validity
- Compared LASSO, principal component regression, and ridge regression models
- Evaluated model performance using RMSE and R²
- Interpreted model results in the context of goalie performance and team defensive environment

## Key Results
Top models achieved test RMSE around 0.0121 and test R² around 0.41. Results suggest that team defensive context helps explain variation in traditional goalie performance metrics.

## Business and Analytics Relevance
This project demonstrates an end-to-end analytics workflow, including data preparation, feature engineering, model comparison, validation, and communication of findings. The workflow is relevant to data analyst roles involving performance evaluation, predictive modeling, and data-informed decision support.

## Repository Structure
- `scripts/`: R scripts for data cleaning, feature engineering, modeling, and evaluation
- `outputs/`: selected model results and visualizations
- `report/`: final capstone report or summary
- `data/`: data documentation or sample data only
