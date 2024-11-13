# crop-yields
Here's a `README.md` section for your GitHub project:

---

# Crop Yield Prediction with Synthetic Data and Model Comparison

This repository contains code to preprocess data, generate synthetic samples, and compare the performance of multiple regression models to predict crop yield. 

## Project Overview

The main steps in this project include:
1. **Data Preprocessing**: Converting units, grouping, and label encoding.
2. **Feature Scaling**: Standardizing features for model compatibility.
3. **Synthetic Data Generation**: Creating synthetic data using bootstrapping.
4. **Model Comparison**: Training and evaluating various regression models.

## Steps in Detail

### 1. Data Preprocessing

- **Unit Conversion**: Different pesticide unit measurements are converted to a common unit (`kg/tonne`).
- **Label Encoding**: Encoding categorical features such as `Item` using `LabelEncoder`.
- **Feature Selection**: Relevant features (`Item_Encoded`, `Pesticide`, `avg temperature`, `avg humidity`, `rainfall`, `Year`) are selected for predicting the target variable (`yield`).

### 2. Synthetic Data Generation

To enhance the dataset, synthetic samples are generated using bootstrapping:
- A bootstrapped sample mean is calculated across original samples to create each synthetic data point.
- The synthetic dataset is added to increase the training data size, improving model performance.

### 3. Model Comparison

The following regression models are trained and evaluated:
- **Linear Regression**
- **Random Forest Regressor**
- **Gradient Boosting Regressor**
- **XGBoost Regressor**
- **K-Nearest Neighbors (KNN) Regressor**
- **Decision Tree Regressor**
- **Bagging Regressor**
- **AdaBoost Regressor**

Each model’s performance is measured based on:
- **Training Accuracy**
- **Test Accuracy**
- **Mean Squared Error (MSE)**
- **R² Score**

### 4. Visualization and Results

For each model:
- A scatter plot of actual vs. predicted values is displayed, with a green line showing the ideal fit.
- A results table ranks models by accuracy, MSE, and R² score, highlighting best and worst values for easy comparison.

## Code Usage

1. **Dependencies**: Install necessary packages with:
   ```bash
   pip install matplotlib pandas scikit-learn xgboost
   ```
2. **Data Loading**: Load and preprocess your dataset to match the format of `df_pesticide` and `df_crop`.
3. **Run the Code**: Execute the script to see model performance, scatter plots, and a styled summary table of results.

## Example Output

- **Scatter Plots**: Visualize each model’s accuracy in predicting yield.
- **Results Table**: A sorted and styled DataFrame highlights model performance based on Accuracy, MSE, and R² score.

