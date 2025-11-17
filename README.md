# MSCS_634_Lab_4: Regression Techniques and Regularization

## Lab Overview
This lab explores various regression techniques to predict diabetes disease progression using the **Diabetes dataset** from `sklearn.datasets`. The lab focuses on:

- Simple Linear Regression
- Multiple Regression
- Polynomial Regression
- Regularization techniques (Ridge and Lasso Regression)
- Model evaluation using MAE, MSE, RMSE, and R²
- Visualization and performance comparison of regression models

---

## Key Insights

- **Single-feature linear regression** (BMI only) performed poorly (R² = 0.23), highlighting the importance of using multiple predictors.  
- **Multiple regression** with all features improved accuracy (R² = 0.45), showing that multiple health indicators contribute to disease progression.  
- **Polynomial regression** on BMI alone did not improve predictions, indicating that polynomial transformations without additional features are insufficient.  
- **Regularization** techniques (Ridge and Lasso) slightly improved performance and helped reduce overfitting.  
- **Lasso Regression** achieved the highest R² (0.46) by performing feature selection, simplifying the model while maintaining accuracy.

---

## Model Performance Summary

| Model                         | MAE    | MSE      | RMSE   | R²    |
|-------------------------------|--------|----------|--------|-------|
| Linear Regression (BMI)       | 52.26  | 4061.83  | 63.73  | 0.23  |
| Multiple Regression           | 42.79  | 2900.19  | 53.85  | 0.45  |
| Polynomial Regression (Degree 2) | 52.38  | 4085.03  | 63.91  | 0.23  |
| Ridge Regression              | 42.81  | 2892.03  | 53.78  | 0.45  |
| Lasso Regression              | 42.80  | 2884.55  | 53.71  | 0.46  |

---

## Analysis and Key Observations

1. **Linear Regression with BMI (Single Feature):**  
   - Lowest performance (R² = 0.23), showing that a single feature cannot explain disease progression well.  
   - High errors (MAE ~52) indicate poor predictive capability.

2. **Multiple Regression (All Features):**  
   - Considerably better performance (R² = 0.45), showing that using multiple features improves prediction accuracy.  
   - Errors reduced compared to simple linear regression (MAE ~42.8, RMSE ~53.85).

3. **Polynomial Regression (Degree 2):**  
   - No significant improvement over linear regression (R² ~0.23).  
   - Demonstrates that a polynomial transformation of a single feature (BMI) does not necessarily enhance model performance.  

4. **Ridge Regression:**  
   - Slight improvement over multiple regression due to regularization.  
   - Helps prevent overfitting by shrinking coefficients, especially useful if features are correlated.

5. **Lasso Regression:**  
   - Marginally better than Ridge (R² = 0.46).  
   - Performs feature selection by setting less important coefficients to zero, simplifying the model while maintaining predictive power.

**Conclusions:**  
- Using multiple features significantly improves predictions compared to a single feature.  
- Polynomial regression of a single variable may lead to overfitting without improving performance.  
- Regularization (Ridge/Lasso) slightly improves performance and ensures model stability.  
- Insights: Key predictors for diabetes progression include BMI, blood pressure, and certain serum measurements.

---

## Challenges and Decisions

- Choosing appropriate features and regression models to prevent overfitting.  
- Deciding polynomial degree: higher degrees led to overfitting without improving performance.  
- Regularization parameters (alpha) were tuned to balance bias and variance.  
- Visualization helped identify model fit and prediction accuracy.

---

## Repository Files

- `Lab4_Regression.ipynb`: Jupyter Notebook with all code, analysis, and visualizations.  
- `README.md`: Lab summary, insights, and model performance.  

---

## Conclusion

This lab demonstrates the importance of multiple regression features, the limitations of single-variable polynomial regression, and the advantages of regularization in improving model stability and predictive performance. Diabetes progression is influenced by multiple health indicators, and careful model selection enhances predictive accuracy.
