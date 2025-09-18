# Medical Insurance Cost Prediction 🩺

## Overview

This project focuses on predicting individual medical insurance costs using a multiple linear regression model. The goal is to analyze a dataset of personal information and build a model that can accurately estimate annual insurance charges. This project demonstrates a complete data science workflow, from data exploration and cleaning to model building and evaluation.



---

## 📖 Problem Statement

The primary objectives of this project are:
1.  To build a machine learning model that can accurately predict medical insurance charges.
2.  To identify the key factors that have the most significant impact on insurance costs.
3.  To apply statistical analysis to validate the relationships discovered during exploratory data analysis.

---

## 💾 Dataset

The dataset used for this project is the "Medical Cost Personal Datasets" sourced from Kaggle. It contains 1,338 rows of data with the following features:

* **age:** Age of the primary beneficiary.
* **sex:** Gender of the contractor (female, male).
* **bmi:** Body mass index.
* **children:** Number of children covered by health insurance.
* **smoker:** Whether the person smokes or not (yes, no).
* **region:** The beneficiary's residential area in the US (northeast, southeast, southwest, northwest).
* **charges:** Individual medical costs billed by health insurance (this is our **target variable**).

---

## ⚙️ Project Workflow

The project followed a structured methodology to ensure robust analysis and modeling:

### 1. Exploratory Data Analysis (EDA)
* Loaded and inspected the dataset to understand its structure, data types, and summary statistics.
* Performed univariate and bivariate analysis to explore the relationships between features and the target variable (`charges`).
* Used **Matplotlib** and **Seaborn** to create visualizations like histograms, box plots, and scatter plots to uncover trends and patterns.

### 2. Feature Engineering & Preprocessing
* Checked for and handled any missing or inconsistent data.
* Converted categorical features (`sex`, `smoker`, `region`) into a numerical format using **one-hot encoding** (`pd.get_dummies`) to prepare them for the model.

### 3. Model Building
* The data was split into features (X) and the target variable (y).
* A **Multiple Linear Regression** model was built using the `LinearRegression` class from **Scikit-learn**.
* The model was trained on the preprocessed dataset to learn the coefficients for each feature.

### 4. Model Evaluation
* The model's performance was evaluated using standard regression metrics:
    * **R-squared (R²):** To measure the proportion of the variance in the target variable that is predictable from the independent variables.
    * **Mean Absolute Error (MAE):** To measure the average magnitude of the errors in a set of predictions, without considering their direction.

---

## 📊 Key Insights & Findings

The analysis revealed several key factors that significantly influence medical costs:

* **Smoking is the Strongest Predictor:** Smokers have drastically higher insurance charges compared to non-smokers. A t-test confirmed this difference is statistically significant.
* **Age and BMI are Significant Factors:** Charges show a strong positive correlation with age and a moderate positive correlation with BMI.
* **Combined Effects:** The effect of a high BMI on insurance charges is substantially more pronounced for smokers than for non-smokers.

---

## 📈 Model Performance

The final linear regression model achieved the following performance:

* **R-squared (R²):** Approximately **0.75**
    * This means our model can explain about 75% of the variability in the insurance charges, which is a strong result for a linear model.
* **Mean Absolute Error (MAE):** [Enter your MAE value here after running the model]

---

## 🛠️ Technologies Used

* **Programming Language:** Python
* **Libraries:**
    * NumPy
    * Pandas
    * Matplotlib
    * Seaborn
    * Scikit-learn
* **Development Environment:** Jupyter Notebook

---

## 🚀 How to Run

To replicate this project on your local machine, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Om-codex/Predicting-Medical-Insurance-Costs.git
    ```
2.  **Navigate to the project directory:**
    ```bash
    cd [Your-Repository-Name]
    ```
3.  **Install the required libraries:**
    *It is recommended to create a virtual environment first.*
    ```bash
    pip install -r requirements.txt
    ```
4.  **Run the Jupyter Notebook:**
    ```bash
    jupyter notebook Medical_Insurance_Cost_Prediction.ipynb
    ```
