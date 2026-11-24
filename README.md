# 👩‍💼 Employee Attrition Risk Prediction Using Multiple Linear Regression

An end-to-end Machine Learning project demonstrating **Multiple Linear Regression** to estimate employee attrition-risk scores using employee information with Python, Pandas, NumPy, Matplotlib, Seaborn and Scikit-Learn.

---

## 📋 Overview

This project implements a Multiple Linear Regression model to analyze employee information and estimate employee attrition-risk scores.

Using employee HR data, the model learns the relationship between employee features such as age, monthly income, job satisfaction, years at the company and work-life balance.

The project covers the complete Machine Learning workflow, including data loading, data exploration, data cleaning, visualization, feature selection, model training, prediction, performance evaluation and model saving using Joblib.

---

## 📊 Dataset: IBM HR Analytics Employee Attrition Dataset

The project uses the **IBM HR Analytics Employee Attrition & Performance Dataset**.

**Dataset file:** `HR-Employee-Attrition.csv`

**Dataset download link:**

[Download IBM HR Employee Attrition Dataset](https://raw.githubusercontent.com/OmerFarukMerey/IBM-HR-Analytics-Employee-Attrition-Performance/main/HR-Employee-Attrition.csv)

The original dataset contains **1,470 employee records and 35 columns**.

### Dataset Features Used

| Feature | Description |
| :--- | :--- |
| **Age** | Age of the employee |
| **MonthlyIncome** | Monthly salary of the employee |
| **JobSatisfaction** | Employee job satisfaction level |
| **YearsAtCompany** | Number of years the employee has worked at the company |
| **WorkLifeBalance** | Employee work-life balance level |

The `MonthlyIncome` column is renamed to `Salary` in the project code for convenience.

### Dataset Information

| Property | Value |
| :--- | :--- |
| Dataset Name | IBM HR Analytics Employee Attrition |
| Original Records | 1,470 |
| Original Columns | 35 |
| File Format | CSV |
| Input Features Used | 5 |
| Target Variable | RiskScore |
| Missing Values | Checked during preprocessing |
| Dataset Source | IBM HR Analytics practice dataset |

### Target Variable

- **`RiskScore`**: A numerical demonstration score created using employee information.
- The score is calculated using job satisfaction, work-life balance, salary and years at the company.
- A higher score represents a higher estimated risk according to the project's scoring formula.

**Note:** RiskScore is a calculated demonstration target, not an actual employee attrition label from the original dataset.

---

## 🧠 Methodology: Multiple Linear Regression

Multiple Linear Regression is a supervised Machine Learning algorithm that predicts a numerical output using two or more independent variables.

The mathematical equation is:

\[
Y = b_0+b_1X_1+b_2X_2+\cdots+b_nX_n
\]

Where:

- **Y** = Predicted Risk Score
- **X₁, X₂, ... Xₙ** = Independent employee features
- **b₀** = Intercept
- **b₁, b₂, ... bₙ** = Regression coefficients

The model learns the relationship between the selected employee features and the calculated RiskScore using the Ordinary Least Squares method.

### Input Features

- Age
- Salary
- JobSatisfaction
- YearsAtCompany
- WorkLifeBalance

### Output Feature

- RiskScore

---

## 📈 Project Pipeline

The complete workflow is implemented in [`Linear_Regrassion.ipynb`](./Linear_Regrassion.ipynb).

1. **Library Importing:** Imported Pandas, NumPy, Matplotlib, Seaborn and Scikit-Learn libraries.
2. **Data Loading:** Uploaded and loaded the IBM HR employee dataset using Pandas.
3. **Data Exploration:** Examined the first five rows, dataset shape, column names, information and statistical summary using `head()`, `shape`, `columns`, `info()` and `describe()`.
4. **Feature Selection:** Selected Age, Salary, JobSatisfaction, YearsAtCompany and WorkLifeBalance.
5. **Data Cleaning:** Removed duplicate records and missing values using `drop_duplicates()` and `dropna()`.
6. **Target Creation:** Created a numerical RiskScore using selected employee features.
7. **Data Visualization:** Created histograms, a correlation heatmap, a box plot and a scatter plot.
8. **Feature and Target Selection:** Selected five employee features as independent variables (X) and RiskScore as the dependent variable (Y).
9. **Train-Test Split:** Divided the available cleaned dataset into training (80%) and testing (20%) sets using `train_test_split(test_size=0.2, random_state=42)`.
10. **Model Creation:** Initialized the `LinearRegression()` algorithm.
11. **Model Training:** Trained the model using `model.fit(X_train, Y_train)`.
12. **Prediction:** Predicted RiskScore values using the testing dataset.
13. **Actual vs Predicted Comparison:** Compared actual and predicted risk scores using Pandas.
14. **Model Evaluation:** Evaluated model performance using MAE, MSE, RMSE and R² Score.
15. **New Employee Prediction:** Predicted the risk score for a new employee using sample employee details.
16. **Risk Classification:** Displayed Low Risk, Medium Risk or High Risk based on the predicted score.
17. **Model Saving:** Saved the trained model using Joblib.

---

## 📊 Performance Evaluation

The model is evaluated using the testing dataset.

### Evaluation Metrics

| Metric | Description |
| :--- | :--- |
| **MAE** | Mean Absolute Error |
| **MSE** | Mean Squared Error |
| **RMSE** | Root Mean Squared Error |
| **R² Score** | Measures how well the model fits the target values |

The actual evaluation values are generated when the Google Colab notebook is executed.

### Visualizations

The project includes:

- Employee Data Distribution Histogram
- Correlation Heatmap
- Employee Data Box Plot
- Salary vs Risk Score Scatter Plot
- Actual vs Predicted Risk Score Graph

---

## 🛠️ Tech Stack

| Technology | Purpose |
| :--- | :--- |
| **Python 3.x** | Programming language |
| **NumPy** | Numerical calculations |
| **Pandas** | Data manipulation and analysis |
| **Matplotlib** | Data visualization |
| **Seaborn** | Statistical data visualization |
| **Scikit-Learn** | Machine Learning model training and evaluation |
| **Joblib** | Saving and loading the trained model |
| **Google Colab** | Development environment |

---

## 📦 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Gujardg/Linear_Regrassion-AD3365.git

cd Linear_Regrassion-AD3365
```

### 2. Install Required Libraries

```bash
pip install numpy pandas matplotlib seaborn scikit-learn joblib
```

### 3. Dataset Setup

Download the `HR-Employee-Attrition.csv` file from the dataset link provided above.

Upload the CSV file to Google Colab when prompted.

The original `MonthlyIncome` column must be renamed to `Salary` before selecting the project features.

### 4. Run the Notebook

Open the notebook:

```bash
jupyter notebook Linear_Regrassion.ipynb
```

You can also open the notebook directly using Google Colab.

---

## 📁 Project Structure

```text
Employee-Attrition-Risk-Prediction/
│
├── Linear_Regrassion.ipynb
│
├── HR-Employee-Attrition.csv
│
├── Employee_Attrition_Dataset.csv
│
├── Employee_Attrition_Model.pkl
│
└── README.md
```

**Note:** The processed dataset and trained model files are generated after executing the corresponding notebook cells. The model is saved using Joblib.

---

## 🎯 Learning Outcomes

Through this project, I learned:

- Fundamentals of Supervised Machine Learning.
- Implementation of Multiple Linear Regression.
- Loading and exploring CSV datasets.
- Data cleaning and preprocessing.
- Data visualization using Matplotlib and Seaborn.
- Selecting independent and dependent variables.
- Training and testing Machine Learning models.
- Understanding regression coefficients and intercepts.
- Evaluating models using MAE, MSE, RMSE and R² Score.
- Making predictions using new employee information.
- Saving and loading trained models using Joblib.

---

## 📝 Conclusion

This project demonstrates the implementation of Multiple Linear Regression using the IBM HR Analytics Employee Attrition Dataset.

The model uses five employee features to estimate a numerical attrition-risk score. It includes data preprocessing, visualization, model training, prediction and performance evaluation.

This project helped develop a practical understanding of the Machine Learning workflow, from loading and exploring employee data to training, evaluating and saving a regression model.

**Important:** The RiskScore used in this project is generated using a predefined formula. Therefore, the model demonstrates regression techniques but does not establish actual employee resignation predictions.

---

## 👩‍💻 GitHub Submission

**Faculty GitHub ID:** [complexiota](https://github.com/complexiota)

**Student GitHub Repository:** [View My Project](https://github.com/Gujardg/Linear_Regrassion-AD3365)

**Project:** Employee Attrition Risk Prediction

**Algorithm:** Multiple Linear Regression

**Dataset:** IBM HR Analytics Employee Attrition Dataset

**Domain:** Machine Learning

---

## 📄 License

This project is created for educational and academic purposes.
