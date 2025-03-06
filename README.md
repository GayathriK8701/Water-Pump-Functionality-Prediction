# Water Pump Functionality Prediction 

## Overview
This project aims to predict the **functionality of water pumps** based on **technical, operational, and environmental factors**. The study applies **machine learning models** to generate insights that help identify failing pumps, enabling **efficient maintenance and resource allocation**. 

By leveraging **data mining techniques**, the project identifies key predictors such as **pump age, water source type, and payment methods** to assess pump functionality.

## Objectives
-  **Predict water pump functionality** using machine learning.
-  **Identify key factors** influencing pump failures.
-  **Improve resource allocation** for pump maintenance.
-  **Reduce downtime and optimize water infrastructure management**.

## Dataset 
- **Total Records**: 4,517
- **Features**: 12 (including **categorical** and **numerical** variables)
- **Target Variable**: `Functioning Status` (Functioning / Not Functioning)
- **Key Features**:
  - **Categorical**: Water Source Type, Payment Type, Funder
  - **Numerical**: Pump Age, Distance to Nearest Town, Population Served
- **Challenges**:
  - Missing values in categorical and numerical fields.
  - Class imbalance (more functioning pumps than non-functioning pumps).

## Data Preprocessing 
- **Handling Missing Values**:
  - Categorical features: Filled with the most frequent value.
  - Numerical features: Imputed with the median value.
- **Feature Encoding**:
  - Categorical features converted using **one-hot encoding**.
  - Numerical features **standardized** for uniform scaling.
- **Class Imbalance Handling**:
  - Applied **class weighting** to balance functionality labels.
- **Dataset Split**:
  - **80% Training (3,999 records)**
  - **20% Testing (1,000 records)**

## Exploratory Data Analysis (EDA) 
- **Key Insights**:
  - **Older pumps** and **pumps farther from towns** are more likely to fail.
  - **Motorized pumps** and **"Pay per use" systems** have higher functionality rates.
  - **Outliers detected** in pump age and distance features.

## Machine Learning Models 
- **Logistic Regression** (Baseline)
- **Random Forest**
- **Gradient Boosting**
- **Support Vector Machine (SVM)**
- **Decision Tree**
- **K-Nearest Neighbors (KNN)**

## Model Evaluation 
- **Evaluation Metrics**:
  - Accuracy, Precision, Recall, F1-Score (focused on `Not Functioning` pumps)
- **Best Performing Model**:
  - **Gradient Boosting**: Highest accuracy (**0.607**) but poor recall for non-functioning pumps.
  - **SVM**: Best balance of **recall (0.339)** and **F1-score (0.317)** for minority class.
  - **Random Forest**: Fair accuracy but struggled with class imbalance.

## Key Findings & Business Impact 
- **Predicting pump failures can improve maintenance scheduling.**  
- **Resource allocation can be optimized to prevent pump breakdowns.**  
- **Class imbalance remains a challenge for detecting failing pumps.**  
- **Hyperparameter tuning and advanced models (e.g., deep learning) may enhance prediction performance.**  
