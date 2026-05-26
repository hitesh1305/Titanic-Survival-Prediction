# 🚢 Titanic Survival Prediction using Machine Learning

This project focuses on predicting whether a passenger survived the Titanic disaster using supervised machine learning techniques. The Titanic dataset is one of the most widely used beginner-to-intermediate ML datasets and provides a good opportunity to practice a complete machine learning workflow.

The project covers the end-to-end process:

- Data exploration and visualization
- Data cleaning and preprocessing
- Feature engineering
- Model building
- Model evaluation and comparison
- Hyperparameter tuning

---

## 📊 Dataset Information

**Dataset Source:** Kaggle Titanic Dataset  
**Problem Type:** Binary Classification  

Target variable:

```text
Survived
0 → Did not survive
1 → Survived
```

Dataset contains **891 passenger records** with multiple attributes.

Features used:

- Passenger Class (`Pclass`)
- Name
- Gender (`Sex`)
- Age
- Number of siblings/spouses (`SibSp`)
- Number of parents/children (`Parch`)
- Ticket Number
- Fare
- Cabin
- Port of Embarkation (`Embarked`)

---

## 📁 Project Structure

```text
Titanic-Survival-Prediction/
│
├── data/
│   └── titanic.csv
│
├── 01-eda.ipynb
├── 02-data_preprocessing.ipynb
├── 03-model_training.ipynb
│
├── utils.py
├── requirements.txt
└── README.md
```

---

## 📘 Notebook Workflow

### 01 — Exploratory Data Analysis

Topics covered:

- Dataset overview
- Missing value analysis
- Univariate analysis
- Bivariate analysis
- Correlation heatmaps
- Survival analysis based on:
  - Gender
  - Passenger class
  - Age
  - Fare
  - Family size

---

### 02 — Data Preprocessing & Feature Engineering

Tasks performed:

- Handling missing values
- Median and mode imputation
- Creating new features:

```text
Title
FamilySize
IsAlone
AgeGroup
FareCategory
HasCabin
```

- Encoding categorical variables
- Preparing dataset for model training

---

### 03 — Model Building & Evaluation

Models trained:

- Logistic Regression
- K-Nearest Neighbors
- Decision Tree
- Random Forest
- Support Vector Machine
- Naive Bayes
- Gradient Boosting

Additional steps:

- Train/Test split
- Feature scaling
- Cross-validation
- Hyperparameter tuning using GridSearchCV
- Performance comparison

---

## 📈 Model Performance

Performance comparison between multiple classification algorithms:

| Model | Accuracy |
|---|---:|
| Logistic Regression | 83.8% |
| SVM | 82.6% |
| Random Forest | 81.5% |
| Gradient Boosting | 81.5% |
| Decision Tree | 79.8% |
| Naive Bayes | 77.6% |
| KNN | 77.0% |

Best tuned parameters for Random Forest:

```python
{
'max_depth':10,
'min_samples_leaf':1,
'min_samples_split':10,
'n_estimators':200
}
```

---

## 🔍 Key Insights from Analysis

Some interesting observations from the dataset:

### Gender strongly influenced survival

- Female survival rate ≈ 74%
- Male survival rate ≈ 19%

---

### Passenger class had significant impact

Survival rates:

```text
1st Class → ~63%

2nd Class → Moderate

3rd Class → ~24%
```

---

### Ticket fare showed relationship with survival

Average fare:

```text
Survivors → ~$48

Non-survivors → ~$22
```

Passengers paying higher fares generally had higher survival chances.

---

### Age patterns

Observed:

- Children had relatively better survival rates
- Adults and elderly passengers had lower survival probability

---

### Family size effect

Passengers travelling:

```text
2–4 members
```

showed better survival compared with:

- solo travelers
- very large families

---

### Feature Engineering helped performance

Features such as:

```text
Title
HasCabin
FamilySize
```

improved prediction quality.

---

## 🛠️ Tech Stack

Programming Language:

- Python

Libraries:

- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

Algorithms:

- Logistic Regression
- KNN
- Decision Tree
- Random Forest
- SVM
- Naive Bayes
- Gradient Boosting

---

## 🚀 Running the Project

### Step 1: Clone Repository

```bash
git clone https://github.com/hitesh1305/Titanic-Survival-Prediction.git
```

---

### Step 2: Install dependencies

```bash
pip install -r requirements.txt
```

---

### Step 3: Start Jupyter Notebook

```bash
jupyter notebook
```

Run notebooks in sequence:

```text
01-eda.ipynb

↓

02-data_preprocessing.ipynb

↓

03-model_training.ipynb
```

---

## 🎯 Learning Outcomes

Through this project I strengthened understanding of:

- Exploratory Data Analysis
- Missing value handling
- Feature engineering
- Data preprocessing
- Classification algorithms
- Model evaluation metrics
- Hyperparameter tuning
- End-to-end ML workflow

---

## 🧠 Final Note

This project was built as part of my Machine Learning learning journey and focuses on understanding the complete ML pipeline rather than only achieving high accuracy.
