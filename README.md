# Flight Price Prediction

This project aims to predict the prices of flight tickets based on several features such as airline, journey date, source, destination, number of stops, and more. The dataset contains historical flight data, which is used to build a machine learning model to estimate the ticket price.

## Project Overview

The project involves:
- Data preprocessing and cleaning
- Exploratory Data Analysis (EDA)
- Feature engineering
- Model selection and training
- Model evaluation and hyperparameter tuning

## Dataset

The dataset used for training contains the following features:
- **Airline**: Name of the airline (Categorical)
- **Date_of_Journey**: Date when the journey starts
- **Source**: Departure airport (Categorical)
- **Destination**: Arrival airport (Categorical)
- **Route**: The route taken (Categorical)
- **Dep_Time**: Departure time
- **Arrival_Time**: Arrival time
- **Duration**: Flight duration (Numeric)
- **Total_Stops**: Number of stops (Categorical)
- **Additional_Info**: Additional flight details (Categorical)
- **Price**: The target variable (Numeric) – Ticket price

The dataset contains 10,683 entries for training and 2,671 entries for testing.

## Steps Involved

### 1. Data Preprocessing and Cleaning
- **Handling Missing Values**: Removed columns with a high percentage of missing values (e.g., `Additional_Info`).
- **Duplicate Removal**: Eliminated duplicate entries to avoid skewed results.
- **Feature Removal**: Dropped irrelevant features like `Year` (as all data belonged to the same year).

### 2. Exploratory Data Analysis (EDA)
- Analyzed the relationship between features and the target variable (price).
- Visualized the distribution of ticket prices, correlations with features like `Number of Stops`, `Airline`, `Duration`, and more.
- Identified strong correlations between the number of stops and ticket price.

### 3. Feature Engineering
- **Date_of_Journey**: Extracted day and month from the date.
- **Duration**: Split the duration into hours and minutes for better granularity.
- **Categorical Variables**: Used OneHotEncoding for variables like `Airline`, `Source`, and `Destination`.

### 4. Model Selection and Training
- **Primary Model**: Random Forest Regressor
  - Random Forest was chosen for its ability to handle non-linear relationships and its robustness against overfitting.
  - Hyperparameter tuning was done using **GridSearchCV** to optimize parameters such as `n_estimators` and `max_depth`.
  
- **Other Models Tested**: Linear Regression, Gradient Boosting Regressor.
  - Random Forest outperformed other models in terms of accuracy.

### 5. Model Evaluation
- Evaluated model performance using **Root Mean Squared Error (RMSE)**.
- The final model was saved using **joblib** for future predictions.

## Installation

To run this project, you need to have Python 3.x installed along with the following libraries:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- joblib
