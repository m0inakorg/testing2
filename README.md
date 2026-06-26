# 🚢 Titanic Survival Prediction

## 📌 Project Overview

The Titanic Survival Prediction project is a supervised machine learning classification problem that predicts whether a passenger survived the Titanic disaster based on passenger information such as age, gender, ticket class, fare, and family size.

This project demonstrates a complete end-to-end Machine Learning pipeline including:

* Data Collection
* Data Cleaning
* Exploratory Data Analysis (EDA)
* Feature Engineering
* Data Preprocessing
* Model Training
* Model Evaluation
* Prediction on New Data

The goal is to understand which factors influenced passenger survival while building a highly accurate predictive model.

---

# 📊 Problem Statement

On April 15, 1912, the RMS Titanic sank after colliding with an iceberg. Out of over 2,200 passengers and crew, more than 1,500 lost their lives.

The objective of this project is to predict whether a passenger survived based on historical passenger information.

This is a **binary classification problem**.

Target Variable:

* **0 → Did Not Survive**
* **1 → Survived**

---

# 🎯 Objectives

The main objectives of this project are:

* Understand the Titanic dataset
* Perform Exploratory Data Analysis
* Handle missing values
* Encode categorical variables
* Scale numerical features
* Train multiple Machine Learning models
* Compare model performance
* Select the best performing model
* Predict survival for unseen passengers

---

# 📂 Dataset Information

The dataset is obtained from the famous Kaggle Titanic Competition.

Files used:

```
train.csv
test.csv
gender_submission.csv
```

### Features

| Feature     | Description                       |
| ----------- | --------------------------------- |
| PassengerId | Unique Passenger ID               |
| Survived    | Target Variable                   |
| Pclass      | Passenger Class (1st, 2nd, 3rd)   |
| Name        | Passenger Name                    |
| Sex         | Male/Female                       |
| Age         | Passenger Age                     |
| SibSp       | Number of siblings/spouses aboard |
| Parch       | Number of parents/children aboard |
| Ticket      | Ticket Number                     |
| Fare        | Ticket Fare                       |
| Cabin       | Cabin Number                      |
| Embarked    | Port of Embarkation               |

---

# 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* Jupyter Notebook

---

# 📁 Project Structure

```
Titanic-Survival-Prediction/
│
├── data/
│   ├── train.csv
│   ├── test.csv
│   └── gender_submission.csv
│
├── notebooks/
│   └── Titanic_EDA.ipynb
│
├── models/
│   └── best_model.pkl
│
├── images/
│   ├── survival_distribution.png
│   ├── age_distribution.png
│   └── correlation_heatmap.png
│
├── app.py
├── requirements.txt
├── README.md
└── LICENSE
```

---

# 🔍 Exploratory Data Analysis (EDA)

Several visualizations were performed to better understand the data.

### Survival Distribution

* Percentage of survivors
* Percentage of non-survivors

---

### Gender vs Survival

Observation:

* Female passengers had significantly higher survival rates than males.

---

### Passenger Class vs Survival

Observation:

* First-class passengers had the highest survival probability.
* Third-class passengers had the lowest survival probability.

---

### Age Distribution

Observation:

* Younger passengers showed slightly higher survival rates.
* Missing age values were imputed using the median.

---

### Fare Distribution

Observation:

Passengers who paid higher fares generally had better survival chances.

---

### Correlation Heatmap

Used to identify relationships between numerical variables.

---

# 🧹 Data Preprocessing

Several preprocessing techniques were applied.

### Missing Values

Age

* Filled using Median

Cabin

* Dropped due to excessive missing values

Embarked

* Filled using Mode

---

### Encoding

Categorical features were converted into numerical values.

Example:

```
Male → 0

Female → 1
```

Embarked:

```
S → 0

C → 1

Q → 2
```

---

### Feature Engineering

New features were created such as:

Family Size

```
FamilySize = SibSp + Parch + 1
```

Is Alone

```
1 if passenger is alone

0 otherwise
```

Title extracted from passenger names.

Example:

```
Mr
Mrs
Miss
Master
Dr
```

---

### Feature Scaling

Numerical features such as:

* Age
* Fare

were standardized using StandardScaler.

---

# 🤖 Machine Learning Models

The following algorithms were trained:

* Logistic Regression
* Decision Tree
* Random Forest
* Support Vector Machine
* K-Nearest Neighbors
* Gradient Boosting
* XGBoost (Optional)

---

# ⚙ Model Training

Dataset Split

```
Training Data : 80%

Testing Data : 20%
```

Cross-validation was also used for more reliable evaluation.

---

# 📈 Model Evaluation

Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC Score
* Confusion Matrix

Example Results

| Model               | Accuracy |
| ------------------- | -------- |
| Logistic Regression | 80.4%    |
| Decision Tree       | 78.1%    |
| Random Forest       | 84.3%    |
| SVM                 | 82.6%    |
| Gradient Boosting   | 85.1%    |

*(Replace these values with your actual results.)*

---

# 🏆 Best Performing Model

Random Forest Classifier achieved the highest accuracy.

Example:

```
Accuracy : 85.1%

Precision : 84%

Recall : 83%

F1 Score : 83.5%
```

---

# 📉 Confusion Matrix

The confusion matrix was used to visualize:

* True Positives
* False Positives
* True Negatives
* False Negatives

This helped understand where the model made mistakes.

---

# 🔮 Prediction Example

Input

```
Passenger Class : 1

Gender : Female

Age : 28

Fare : 80

Family Size : 1
```

Prediction

```
Survived
```

---

# 📸 Sample Visualizations

Include screenshots like:

```
images/

survival_distribution.png

age_distribution.png

heatmap.png

feature_importance.png

confusion_matrix.png
```

These make the README more attractive.

---

# 🚀 Installation

Clone the repository

```bash
git clone https://github.com/yourusername/Titanic-Survival-Prediction.git
```

Move into the project directory

```bash
cd Titanic-Survival-Prediction
```

Install dependencies

```bash
pip install -r requirements.txt
```

Run the notebook

```bash
jupyter notebook
```

Or run the application

```bash
python app.py
```

---

# 📦 Requirements

```text
Python >= 3.10

pandas

numpy

matplotlib

seaborn

scikit-learn

joblib

jupyter
```

---

# 📚 Machine Learning Workflow

```
Dataset

↓

Data Cleaning

↓

Exploratory Data Analysis

↓

Feature Engineering

↓

Encoding

↓

Scaling

↓

Train-Test Split

↓

Model Training

↓

Model Evaluation

↓

Prediction
```

---

# 🔍 Key Insights

* Female passengers had much higher survival rates than males.
* First-class passengers were more likely to survive than third-class passengers.
* Younger passengers showed a slightly better chance of survival.
* Larger ticket fares correlated with higher survival rates.
* Traveling alone reduced survival probability in many cases.

---

# 🔮 Future Improvements

* Hyperparameter tuning using GridSearchCV or RandomizedSearchCV.
* Experiment with advanced ensemble methods such as XGBoost, LightGBM, or CatBoost.
* Deploy the model using Flask, FastAPI, or Streamlit.
* Add SHAP or LIME for model explainability.
* Automate the training pipeline and integrate CI/CD for deployment.

---

# 🤝 Contributing

Contributions are welcome! If you'd like to improve this project:

1. Fork the repository.
2. Create a new feature branch.
3. Commit your changes.
4. Push to your fork.
5. Open a Pull Request.

---

# 📜 License

This project is licensed under the MIT License. Feel free to use, modify, and distribute it in accordance with the license terms.


A README of this quality is well-suited for a portfolio project and demonstrates a complete understanding of the machine learning workflow, making it appealing to recruiters and collaborators.
