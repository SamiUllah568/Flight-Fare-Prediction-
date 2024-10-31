# Flight Fare Prediction Project

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Models](#models)
- [Evaluation](#evaluation)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
The Flight Fare Prediction project aims to predict flight ticket prices based on various features such as the airline, source and destination, date of journey, and other related factors. This project utilizes machine learning techniques to build a predictive model, providing insights into how various factors affect flight prices.

## Dataset
The dataset used for this project contains information about flights, including ticket prices and various features. It can be found in the `data` folder of this repository. The dataset consists of:
- Train Dataset: 10,683 samples
- Test Dataset: 2,671 samples

## Features
The following features are included in the dataset:
- `Airline`: The name of the airline
- `Source`: The origin city
- `Destination`: The destination city
- `Date`: The date of the journey
- `Month`: The month of the journey
- `Stops`: Total stops between the source and destination
- `Arrival_hour`: Hour of arrival
- `Arrival_min`: Minute of arrival
- `Dep_hour`: Hour of departure
- `Dep_min`: Minute of departure
- `Duration_hour`: Duration of the flight in hours
- `Duration_min`: Duration of the flight in minutes
- `Route`: Routes taken by the flight

## Installation
To run this project locally, follow these steps:

1. Clone this repository:
   ```bash
   git clone https://github.com/SamiUllah568/Flight-Fare-Prediction.git
   cd Flight-Fare-Prediction

## **Models**
This project utilizes the following models:

   o   Decision Tree Regressor
   o   Random Forest Regressor
   o   Gradient Boosting Regressor
Hyperparameter tuning is performed using RandomizedSearchCV to optimize model performance.

## **Evaluation**
The models are evaluated using the following metrics:

Mean Squared Error (MSE)
Mean Absolute Error (MAE)
Root Mean Squared Error (RMSE)
R² Score
## **Results**
After evaluating the models, the Random Forest Regressor yielded the best performance with an R² score of approximately 0.89.
