# 🎓 Student Dropout Prediction

## 📌 Project Overview

**Student Dropout Prediction** is a Machine Learning project designed to analyze student engagement and academic-related information to identify students who may be at risk of dropping out.

The project uses an online education dataset containing student demographic, academic, engagement, performance, risk, and outcome information. Exploratory Data Analysis (EDA) is performed to understand the relationship between student engagement and academic outcomes.

A **Logistic Regression** model is implemented to analyze the relationship between **total clicks** and the student's **pass flag**.

---

## 🎯 Objectives

* Analyze student academic and engagement data.
* Identify patterns related to student performance.
* Study the relationship between engagement level and pass rate.
* Handle missing values in important numerical columns.
* Apply feature scaling using `StandardScaler`.
* Build a Logistic Regression model.
* Use the analysis to support early identification of students who may require academic assistance.

---

## 📊 Dataset

The project uses:

**`online_education_dataset.csv`**

The dataset contains **32,593 student records** and **14 features**.

### Main Features

| Feature             | Description                                         |
| ------------------- | --------------------------------------------------- |
| `id_student`        | Unique student identifier                           |
| `gender`            | Student gender                                      |
| `region`            | Student region                                      |
| `highest_education` | Highest education qualification                     |
| `studied_credits`   | Number of credits studied                           |
| `imd_band`          | Socio-economic/deprivation band                     |
| `total_clicks`      | Total number of online learning interactions/clicks |
| `avg_score`         | Average student score                               |
| `engagement_level`  | Student engagement level                            |
| `performance_level` | Student performance category                        |
| `risk_level`        | Student risk category                               |
| `pass_flag`         | Indicates whether the student passed                |
| `dropout_flag`      | Indicates whether the student dropped out           |
| `final_result`      | Final student result                                |

### Final Result Categories

The dataset contains the following final-result categories:

* Pass
* Withdrawn
* Fail
* Distinction

---

## 🔍 Exploratory Data Analysis

The project performs several exploratory analyses.

### 1. Final Result Distribution

The `final_result` column is analyzed using value counts to understand the distribution of student outcomes.

### 2. Engagement vs Pass Rate

The project calculates the average `pass_flag` for each `engagement_level`.

This helps examine whether students with different levels of online engagement have different pass rates.

### 3. Visualization

A bar chart is used to visualize:

**Engagement Level vs Pass Rate**

The engagement categories are:

* Low
* Medium
* High

This visualization helps identify the relationship between student engagement and academic success.

---

## 🧹 Data Preprocessing

Missing values are checked for important variables.

The notebook specifically checks:

* `total_clicks`
* `pass_flag`

Missing values in `total_clicks` are replaced with `0`.

Missing values in `pass_flag` are also replaced with `0`.

---

## 🤖 Machine Learning Model

### Logistic Regression

The project uses **Logistic Regression** from Scikit-learn.

The model uses:

```text
Feature: total_clicks
Target: pass_flag
```

Before training, the feature is standardized using:

```text
StandardScaler
```

The scaled feature is then provided to the Logistic Regression model.

### Model Configuration

```python
LogisticRegression(max_iter=1000)
```

The trained model's coefficient is also examined to understand the relationship between total clicks and the prediction target.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **Jupyter Notebook**
* **Machine Learning**
* **Logistic Regression**

---

## 📁 Project Structure

```text
Student-Dropout-Prediction/
│
├── Student_Dropout_Prediction.ipynb
├── online_education_dataset.csv
└── README.md
```

---

## ⚙️ Installation

Clone the repository:

```bash
git clone <your-github-repository-url>
```

Navigate to the project directory:

```bash
cd Student-Dropout-Prediction
```

Install the required Python libraries:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

---

## ▶️ How to Run

1. Download or clone this repository.
2. Make sure `online_education_dataset.csv` is in the same directory as the notebook.
3. Open Jupyter Notebook:

```bash
jupyter notebook
```

4. Open:

```text
Student_Dropout_Prediction.ipynb
```

5. Run the notebook cells sequentially.

---

## 🔄 Machine Learning Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Exploratory Data Analysis
   ↓
Missing Value Checking
   ↓
Data Preprocessing
   ↓
Feature Scaling
   ↓
Logistic Regression
   ↓
Model Coefficient Analysis
   ↓
Engagement & Pass Rate Visualization
```

---

## 📈 Key Analysis

The project focuses on understanding how **online engagement** relates to student outcomes.

In particular, `total_clicks` is used as an indicator of online learning activity, while `pass_flag` is used as the target variable for the Logistic Regression analysis.

The project also examines how pass rates vary across **Low, Medium, and High engagement levels**.

---
output:
<Figure size 640x480 with 1 Axes><img width="567" height="455" alt="image" src="https://github.com/user-attachments/assets/026a2376-66eb-4e65-9cc3-c098f2b4c7d3" />
<Figure size 640x480 with 1 Axes><img width="567" height="433" alt="image" src="https://github.com/user-attachments/assets/384872b2-3fa1-4170-91a4-f0d1f39d9c6b" />



## 📌 Conclusion

The **Student Dropout Prediction** project demonstrates how Machine Learning and Exploratory Data Analysis can be applied to online education data.

By analyzing student engagement and academic outcomes, the project provides a foundation for identifying patterns that can help educational institutions understand student performance and potentially identify students who need additional support.

---
<Figure size 640x480 with 1 Axes><img width="567" height="455" alt="image" src="https://github.com/user-attachments/assets/026a2376-66eb-4e65-9cc3-c098f2b4c7d3" />

## 👩‍💻 Author

**Pradeepa**

BCA Student

---

## ⭐ Project Status

**Completed – Machine Learning / Academic Project**

Future versions can extend the current implementation into a more comprehensive student dropout classification system using multiple student-related features.
