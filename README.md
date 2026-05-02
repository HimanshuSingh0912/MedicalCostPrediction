# Medical Cost Prediction using Linear Regression

## Project Overview
This project aims to predict individual medical costs billed by health insurance. Using a dataset of patient information (age, sex, BMI, etc.), we build a Linear Regression model to estimate the `charges` column. This is a classic regression problem useful for healthcare providers and insurance companies to estimate future costs.

## Dataset Description
The dataset used is the **Medical Cost Personal Dataset** (from Kaggle). It contains 1,338 rows and 7 columns:

* **AGE:** Age of primary beneficiary.
* **SEX:** Insurance contractor gender (female, male).
* **BMI:** Body mass index, providing an understanding of body weight relative to height.
* **CHILDREN:** Number of children covered by health insurance.
* **smoker:** Smoking status (yes, no).
* **region:** The beneficiary's residential area in the US.
* **charges:** Individual medical costs billed by health insurance (Target Variable).

## Key Steps Involved

### 1. Data Cleaning & Preprocessing
* **Label Encoding:** Converted categorical variables (sex, smoker, region) into numerical format using `LabelEncoder`.
* **Outlier Removal:** Applied the Interquartile Range (IQR) method to remove extreme values in numerical columns, improving model stability.
* **Split:** Divided the data into 80% Training and 20% Testing sets.

### 2. Exploratory Data Analysis (EDA)
* Visualized the distribution of medical charges using histograms.
* Generated a Correlation Heatmap to identify which features (like `smoker` and `age`) have the strongest impact on costs.

### 3. Machine Learning Model
* **Algorithm:** Linear Regression.
* **Library:** Scikit-Learn.

## Model Performance
After training, the model was evaluated on the test set with the following results:

* **Mean Absolute Error (MAE):** 2,591.12
* **Root Mean Squared Error (RMSE):** 4,732.82
* **R-squared (R²):** 0.3425

## Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn
* **Platform:** Google Colab / Jupyter Notebook

## How to Run
1. Clone this repository.
2. Upload `insurance.csv` to your environment.
3. Run the notebook cells sequentially.
