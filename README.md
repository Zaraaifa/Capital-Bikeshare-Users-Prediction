# Optimizing Capital Bikeshare Operations: Predictive Modeling with Machine Learning

## Overview
This repository contains a capstone project focused on optimizing the operations of Capital Bikeshare, a leading bike-sharing service in the Washington, D.C. metropolitan area. The project utilizes machine learning regression techniques to predict the number of casual and registered users based on external factors such as weather, time, and day. The goal is to enhance operational efficiency, improve resource allocation, and develop targeted marketing strategies for user conversion from casual to registered segments.

## Table of Contents
- [Business Problem](#business-problem)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results](#results)
- [Recommendations](#recommendations)
- [Installation](#installation)
- [Usage](#usage)
- [Presentation](#presentation)
- [License](#license)
- [Contact](#contact)

## Business Problem
Capital Bikeshare faces challenges in predicting demand per user segment, implementing differentiated strategies, and efficiently allocating marketing resources. This project addresses:
1. Predicting the number of casual and registered users under various conditions.
2. Identifying key external factors influencing user behavior.
3. Leveraging conditions with high casual user proportions for conversion strategies.

## Dataset
The dataset is sourced from Capital Bikeshare and includes historical bike rental data with the following features:
- `dteday`: Date of rental
- `season`: Season (1: Winter, 2: Spring, 3: Summer, 4: Fall)
- `hr`: Hour (0-23)
- `holiday`: Binary (0: Weekday, 1: Holiday)
- `temp`: Normalized temperature (Celsius)
- `atemp`: "Feels-like" temperature (normalized)
- `hum`: Normalized humidity (0-1)
- `casual`: Number of non-member users
- `registered`: Number of member users
- `cnt`: Total bikes rented (casual + registered)
- `weathersit`: Weather condition (1: Clear, 2: Mist, 3: Light Rain, 4: Heavy Rain)

- **Rows**: 12,165
- **Source**: [Google Drive Link](https://drive.google.com/file/d/1lSbp2GTSgE8jwvA2K8rlLRZIUTWNNfXe/view?usp=share_link)

## Methodology
The project follows these steps:
1. **Data Preparation**: Cleaning, handling missing values, and feature engineering.
2. **Model Development**: Implementing regression models (e.g., CatBoost, LightGBM, XGBoost) with hyperparameter tuning using GridSearchCV and cross-validation.
3. **Model Evaluation**: Assessing performance using MAE, RMSE, and R² metrics on both train and test sets.
4. **Visualization**: Creating plots to compare true vs. predicted values.
5. **Model Saving**: Storing the best models for future use.

## Results
- **Casual Users**: RMSE = 13.03, MAE = 8.06, R² = 0.93
- **Registered Users**: RMSE = 33.59, MAE = 20.30, R² = 0.95
- The model performs well with high R² values, indicating strong explanatory power. Registered users show more predictable patterns, while casual users exhibit higher variability, especially during peak recreational times.

## Recommendations
- **Operational Optimization**: Adjust bike stock and staff scheduling based on peak hours (e.g., 07:00-09:00 and 17:00-18:00 for registered users, 12:00-14:00 for casual users on weekends).
- **Marketing Strategies**: Launch targeted campaigns during weekends and favorable weather (15-25°C) to convert casual users, offering discounts or loyalty points.
- **Model Improvement**: Explore ensemble methods (e.g., stacking CatBoost with LightGBM/XGBoost) and add feature importance analysis using SHAP values.

## Installation
To run this project locally, ensure you have the required dependencies installed. Use the following commands:

```bash
# Clone the repository
git clone https://github.com/username/capital-bikeshare-optimization.git

# Navigate to the project directory
cd capital-bikeshare-optimization

# Install dependencies
pip install -r requirements.txt
```

## Usage
1. Download the dataset from the provided Google Drive link and place it in the project directory as data_bike_sharing.csv.
2. Run the Jupyter Notebook Capstone3_Bike_Sharing.ipynb to execute the data preparation, modeling, and visualization steps.
3. Adjust parameters or models as needed in the notebook cells.

## Presentation
For a detailed presentation of the project findings, refer to the Canva presentation [here](https://www.canva.com/design/DAGmfL3KjqE/-SaDMl5UVGpRySKXgcMooA/edit).

## Contact
For questions and contributions, please contact:
- Email : abdillah.zaraa@gmail.com
- LinkedIn : [abdillah zaraaifa al farisa](https://www.linkedin.com/in/abdillah-zaraaifa-al-farisa)
- GitHub : Zaraaifa
