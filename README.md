# Medical Cost Prediction - Linear Regression Model

This project builds a predictive model to estimate individual medical costs billed by health insurance. By leveraging patient demographics and health-related data, the model provides insights into the primary factors driving insurance costs.

## Key Improvements
*   **Log Transformation:** Applied `np.log()` to the target variable (`charges`) to handle skewness and improve model linearity.
*   **Feature Engineering:** Created an interaction feature `bmi_smoker` to capture the significant synergy between BMI and smoking status on insurance costs.
*   **Data Preprocessing:** Utilized `get_dummies` for categorical encoding and the **IQR method** for robust outlier handling in numerical features.

## Dataset
*   **Source:** Medical Cost Personal Dataset (Kaggle).
*   **Features:** Age, BMI, Children, Sex, Smoker status, Region.
*   **Target:** `charges` (Medical costs).

## Model Performance
The model was trained using **Linear Regression** via `scikit-learn`. After preprocessing and feature engineering, the model achieved the following results on the test set:

| Metric | Value |
| :--- | :--- |
| **Mean Absolute Error (MAE)** | 0.01 |
| **Root Mean Squared Error (RMSE)** | 0.02 |
| **R-squared (R²)** | 0.7438 |

*Note: The MAE and RMSE values are low due to the log-transformation of the target variable.*

## Tech Stack
*   **Language:** Python
*   **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn
*   **Environment:** Google Colab / Jupyter Notebook

## Visualizations
*   **Correlation Heatmap:** Identified strong relationships between `smoker_yes`, `bmi`, and `charges`.
*   **Actual vs. Predicted:** A regression plot demonstrates the model's high accuracy in predicting insurance costs.

---
*Created by Himanshu Singh | B.Tech CSE (AI)*
