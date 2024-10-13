# Cricket Score and Win/Loss Prediction

## Overview
This project aims to predict the final score and the win/loss outcome of a cricket match using machine learning models. It cleanses and processes historical cricket match data, filling in missing values, removing duplicates, and handling outliers like infinite values, before applying predictive modeling techniques.

## Data Preprocessing
The project involves several preprocessing steps to prepare the data for machine learning:
- **Handling Missing Values:** Missing values in the "Overs," "Bowling_EconomyRate," and "Bowling_Strike_Rate" columns were filled with the mean values of the respective columns. Missing "Target" values were predicted using a linear regression model based on the "Score," "Wicket," and "Overs" columns.
- **Removing Infinite Values:** Infinite values in the "Batting_Average_Main_Team" and "Bowling_Strike_Rate" columns were identified and removed.
- **Dropping Duplicates:** Duplicate rows in the dataset were removed to ensure the integrity of the data.
- **Date Conversion:** The "Start Date" column was converted to `datetime` format for further analysis.

## Dataset
The dataset includes the following features:
- **Score**: The score of the team.
- **Overs**: Overs bowled.
- **RPO**: Run rate (Runs per Over).
- **Target**: Target score.
- **Inns**: Innings number.
- **Result**: Win/loss outcome.
- **Opposition**: The opposing team.
- **Ground**: The venue of the match.
- **Start Date**: Date of the match.
- **Team name**: Name of the team.
- **Wicket**: Number of wickets lost.
- **Batting_Average_Main_Team**: Batting average of the main team.
- **Bowling_EconomyRate**: Economy rate of the bowlers.
- **Strike_Rate**: Batting strike rate.
- **Bowling_Strike_Rate**: Bowling strike rate.

The dataset contains **9184 rows** and **15 columns** after preprocessing.

## Correlation Analysis
A heatmap was generated to visualize the correlation between different numerical features in the dataset. This helps in understanding the relationships between variables like "Score," "Overs," and "Target."

## Model Implementation
The project uses a **Linear Regression** model to predict the "Target" score when missing, based on other features like "Score," "Wicket," and "Overs."
