# Happiness Score Prediction Project

This project aims to predict the **Happiness Score** of countries or regions using various features such as **GDP per capita**, **Social Support**, **Healthy Life Expectancy**, **Freedom to Make Life Choices**, **Generosity**, and **Perceptions of Corruption**. The project applies different regression models to find the best fit and prediction accuracy.

---

## Project Overview

In this project, we perform data analysis and predictive modeling on a dataset that contains information on various factors influencing happiness. We focus on the following tasks:

1. **Data Preprocessing**: Clean and prepare the data.
2. **Feature Engineering**: Create new features, including polynomial features, to improve model performance.
3. **Model Training**: Train multiple regression models, including **Linear Regression**, **Polynomial Regression**, **Ridge Regression**, and **Ridge Regression with Polynomial Features**.
4. **Model Evaluation**: Compare model performance using evaluation metrics like **Adjusted R²**, **Mean Absolute Error (MAE)**, **Mean Squared Error (MSE)**, and **Root Mean Squared Error (RMSE)**.

---

## Steps Taken in the Project

1. **Data Preprocessing**: 
   - The dataset was cleaned by handling missing values, encoding categorical features, and scaling numerical features.
   - Features like **Country/Region** were replaced with latitude for better model interpretation.

2. **Model Comparison**:
   - We started with a **Regular Linear Regression** model.
   - Next, we used **Polynomial Regression** with Linear Regression to explore the impact of adding polynomial features.
   - Then, we applied **Ridge Regression**, a regularized linear model, to control overfitting.
   - Finally, we performed **Ridge Regression with Polynomial Features** to get the best possible model by tuning the alpha parameter.

---

## Models Evaluated

Here are the results of the models evaluated:

### 1. **Regular Linear Regression (LR)**

- **Adjusted R²**: 0.7309  
  - The basic linear model with one feature (no regularization) provides a decent fit, but the performance is limited.

### 2. **Polynomial Regression with Linear Model (Poly + LR)**

- **Adjusted R²**: 0.7309  
  - Adding polynomial features (degree 2) did not significantly improve the model's performance over the regular linear regression.

### 3. **Ridge Regression (Regularized Linear Model)**

- **Adjusted R²**: 0.8018  
  - Ridge regression improved the model’s performance by reducing overfitting, with a higher Adjusted R² score compared to the regular LR.

### 4. **Ridge Regression with Polynomial Features (Poly + Ridge)**

- **Adjusted R²**: 0.8286  
  - The best model, with **polynomial features** and **Ridge Regression** with an **alpha value of 0.001**, showed the best performance and highest Adjusted R², explaining 82.86% of the variance in the target variable.

---

## Model Evaluation Metrics

For each model, we used the following evaluation metrics:

- **Mean Absolute Error (MAE)**: The average magnitude of errors in predictions.
- **Mean Squared Error (MSE)**: The squared average of errors, penalizing larger errors.
- **Root Mean Squared Error (RMSE)**: The square root of MSE, showing the error in the same units as the target variable.
- **R² Score (Coefficient of Determination)**: Measures the proportion of variance in the target variable explained by the model.
- **Adjusted R²**: Adjusted for the number of predictors in the model, showing how well the model fits the data with respect to the number of features.

---

## Best Model

The **Ridge Regression with Polynomial Features** (**Adjusted R² = 0.8286**) outperforms all other models, making it the best choice for predicting the Happiness Score. This model achieves a strong fit and accurately captures the relationships between features and the target variable.

---

## Conclusion

This project demonstrates how different regression models can be used to predict the Happiness Score based on various socio-economic and psychological factors. By using **Ridge Regression with Polynomial Features**, we were able to achieve the best model performance, with an **Adjusted R²** of **0.8286**, suggesting that this model is the most reliable for predicting happiness scores.
