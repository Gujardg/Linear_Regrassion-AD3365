# 💰 Salary Prediction Using Simple Linear Regression

An end-to-end Machine Learning project demonstrating **Simple Linear Regression** to predict employee salaries based on years of work experience using Python, Pandas, NumPy, Matplotlib and Scikit-Learn.

---

## 📋 Overview

This project implements a Simple Linear Regression model to analyze and predict employee salaries based on their years of professional experience.

Using historical salary data, the model learns the mathematical relationship between years of experience and salary. It then uses this relationship to estimate salaries for new experience values.

The project covers the complete Machine Learning workflow, including data loading, data exploration, visualization, feature selection, model training, prediction, performance evaluation and model serialization using Pickle.

---

## 📊 Dataset: Salary Data

The project uses the **Salary_Data_Linear_Regression.csv** dataset.

The dataset contains **30 records** and **2 columns**, representing employee experience and their corresponding salaries.

### Dataset Features

| Feature | Description |
| :--- | :--- |
| **`YearsExperience`** | Number of years of professional work experience |
| **`Salary`** | Corresponding employee salary |

### Dataset Information

| Property | Value |
| :--- | :--- |
| Total Records | 30 |
| Total Features | 1 |
| Target Variables | 1 |
| Missing Values | 0 |
| Input Feature | YearsExperience |
| Output Feature | Salary |

### Target Variable

- **`Salary`**: The employee's salary, which is the dependent variable predicted by the trained Machine Learning model.

---

## 🧠 Methodology: Simple Linear Regression

Simple Linear Regression is a supervised Machine Learning algorithm that establishes a linear relationship between one independent variable (X) and one dependent variable (Y).

The mathematical equation is:

\[
Y = mX + c
\]

Where:

- **Y** = Predicted salary
- **X** = Years of experience
- **m** = Slope or regression coefficient
- **c** = Intercept

The model learns the best-fitting regression line by minimizing the sum of squared prediction errors using the Ordinary Least Squares method.

### Learned Model Parameters

Based on the trained model:

- **Coefficient (m):** `9346.9036`
- **Intercept (c):** `26536.2371`

The resulting regression equation is:

\[
Salary = 9346.9036 \times Experience + 26536.2371
\]

This indicates that the predicted salary increases by approximately 9,346.90 units for each additional year of experience, according to the fitted model.

---

## 📈 Project Pipeline

The complete workflow is implemented in [`Linear_Regrassion.ipynb`](./Linear_Regrassion.ipynb).

1. **Library Importing:** Imported NumPy, Pandas, Matplotlib and Scikit-Learn libraries.
2. **Data Loading:** Uploaded and loaded the salary dataset using Pandas.
3. **Data Exploration:** Examined the first five rows, last five rows, dataset information and statistical summary using `head()`, `tail()`, `info()` and `describe()`.
4. **Data Cleaning:** Checked for missing values using `isnull().sum()`. No missing values were found.
5. **Data Visualization:** Created a scatter plot to understand the relationship between years of experience and salary.
6. **Feature and Target Selection:** Selected `YearsExperience` as the independent variable (X) and `Salary` as the dependent variable (y).
7. **Train-Test Split:** Divided the dataset into training (80%, 24 records) and testing (20%, 6 records) sets using `train_test_split(test_size=0.2, random_state=42)`.
8. **Model Creation:** Initialized the `LinearRegression()` algorithm.
9. **Model Training:** Trained the model using `model.fit(X_train, y_train)`.
10. **Salary Prediction:** Predicted salaries using the testing dataset.
11. **Actual vs Predicted Comparison:** Compared actual salary values with predicted salary values using Pandas.
12. **Regression Visualization:** Plotted the training data and fitted regression line.
13. **Model Evaluation:** Evaluated model performance using MAE, MSE, RMSE and R² Score.
14. **New Data Prediction:** Predicted salaries for employees with 5 and 7 years of experience.
15. **Model Saving:** Saved and loaded the trained model using Python Pickle.

---

## 📊 Performance Results

The model was evaluated using the testing dataset containing 6 unseen records.

### Evaluation Metrics

| Metric | Value | Interpretation |
| :--- | :--- | :--- |
| **MAE** | `1725.96` | Average absolute prediction error |
| **MSE** | `4620853.53` | Average squared prediction error |
| **RMSE** | `2149.62` | Root mean squared prediction error |
| **R² Score** | `0.99298` | Approximately 99.30% of target variance explained on the test set |

### Model Parameters

| Parameter | Value |
| :--- | :--- |
| Regression Coefficient | `9346.9036` |
| Intercept | `26536.2371` |

### Actual vs Predicted Salary

| Actual Salary | Predicted Salary |
| :---: | :---: |
| 126756 | 129352.18 |
| 81363 | 81682.97 |
| 116969 | 115331.82 |
| 91738 | 90095.18 |
| 57189 | 61119.78 |
| 63218 | 62989.16 |

### New Salary Predictions

The trained model was tested with new experience values.

| Years of Experience | Predicted Salary |
| :---: | :---: |
| 5 Years | 73,270.76 |
| 7 Years | 91,964.56 |

**Key Result:** The model achieved an R² score of approximately **99.30%** on the test dataset, demonstrating a strong linear relationship between years of experience and salary in this dataset.

---

## 🛠️ Tech Stack

| Technology | Purpose |
| :--- | :--- |
| **Python 3.x** | Programming language |
| **NumPy** | Numerical calculations |
| **Pandas** | Data manipulation and analysis |
| **Matplotlib** | Data visualization |
| **Scikit-Learn** | Machine Learning model training and evaluation |
| **Pickle** | Saving and loading the trained model |
| **Google Colab / Jupyter Notebook** | Development environment |

---

## 📦 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY-NAME.git

cd YOUR-REPOSITORY-NAME
```

### 2. Install Required Libraries

```bash
pip install numpy pandas matplotlib scikit-learn notebook
```

### 3. Dataset Setup

Place the `Salary_Data_Linear_Regression.csv` file in the project directory.

### 4. Run the Notebook

```bash
jupyter notebook Linear_Regrassion.ipynb
```

You can also open the notebook directly using Google Colab.

---

## 📁 Project Structure

```text
Salary-Prediction-Linear-Regression/
│
├── Linear_Regrassion.ipynb
│
├── Salary_Data_Linear_Regression.csv
│
├── linear_regression_model.pkl
│
└── README.md
```

**Note:** The Pickle model file is generated when you execute the model-saving section of the notebook.

---

## 🎯 Learning Outcomes

Through this project, I learned:

- Fundamentals of Supervised Machine Learning.
- Implementation of Simple Linear Regression.
- Data exploration and preprocessing.
- Data visualization using Matplotlib.
- Training and testing Machine Learning models.
- Understanding regression coefficients and intercepts.
- Evaluating models using MAE, MSE, RMSE and R² Score.
- Making predictions using new input data.
- Saving and loading trained models using Pickle.

---

## 📝 Conclusion

This project successfully demonstrates the implementation of Simple Linear Regression for salary prediction using years of experience.

The trained model achieved an R² score of approximately 99.30% on the test dataset. The results indicate that years of experience is a strong predictor of salary in the given dataset.

This project helped develop a practical understanding of the Machine Learning pipeline, from importing and exploring data to model training, prediction, evaluation and deployment preparation.

---

## 👩‍💻 GitHub Submission

**Faculty GitHub ID:** [complexiota](https://github.com/complexiota)

**Student GitHub Repository:** [View My Project](https://github.com/Gujardg/Linear_Regrassion-AD3365)

**Project:** Salary Prediction Using Simple Linear Regression

**Algorithm:** Simple Linear Regression

**Domain:** Machine Learning

---

## 📄 License

This project is created for educational and academic purposes.
