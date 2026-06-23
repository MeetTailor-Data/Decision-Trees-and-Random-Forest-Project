# Decision Trees and Random Forest Project

## Project Description

This project implements Decision Tree and Random Forest classification algorithms on a loan dataset to predict whether a borrower will fully repay a loan.

The project includes exploratory data analysis, categorical feature encoding, model training, and performance evaluation using classification metrics.

---

## Dataset

Dataset: `loan_data.csv`

Target Variable:

* `not.fully.paid`

Features used in the dataset include:

* credit.policy
* purpose
* int.rate
* installment
* log.annual.inc
* dti
* fico
* days.with.cr.line
* revol.bal
* revol.util
* inq.last.6mths
* delinq.2yrs
* pub.rec

---

## Project Workflow

### Exploratory Data Analysis (EDA)

The notebook includes:

* Dataset information using `info()`
* Statistical summary using `describe()`
* FICO score distribution based on `credit.policy`
* FICO score distribution based on `not.fully.paid`
* Count plot of loan purpose with respect to `not.fully.paid`
* Joint plot of `fico` and `int.rate`
* Linear model plot of `fico` and `int.rate` using:

  * `credit.policy`
  * `not.fully.paid`

---

## Data Preprocessing

The following preprocessing steps are performed:

* Identified categorical feature:

  * `purpose`
* Applied one-hot encoding using `pd.get_dummies()`
* Used `drop_first=True` to avoid multicollinearity.

---

## Train-Test Split

* Features (`X`): All columns except `not.fully.paid`
* Target (`y`): `not.fully.paid`
* Test Size: 30%
* Random State: 101

---

## Machine Learning Models

### Decision Tree Classifier

Algorithm:

* `DecisionTreeClassifier`

Steps:

1. Train the model on the training dataset.
2. Predict loan repayment status on the test dataset.
3. Evaluate model performance.

### Random Forest Classifier

Algorithm:

* `RandomForestClassifier`

Parameters:

* `n_estimators = 300`

Steps:

1. Train the Random Forest model.
2. Predict loan repayment status on the test dataset.
3. Compare performance with the Decision Tree model.

---

## Model Evaluation

The models were evaluated using:

* Classification Report
* Confusion Matrix

The notebook concludes that neither model performed particularly well and that additional feature engineering is required.

---

## Concepts Used

* Exploratory Data Analysis (EDA)
* Histograms
* Count Plots
* Joint Plots
* Linear Model Plots
* Categorical Feature Encoding
* One-Hot Encoding
* Train-Test Split
* Decision Tree Classification
* Random Forest Classification
* Classification Report
* Confusion Matrix

---

## Project Structure

```text
Decision-Trees-and-Random-Forest-Project/
│
├── 02-Decision Trees and Random Forest Project.ipynb
├── loan_data.csv
└── README.md
```

---

## Requirements

* Python 3.x
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## How to Run

1. Clone this repository.
2. Place `loan_data.csv` in the project folder.
3. Open `02-Decision Trees and Random Forest Project.ipynb`.
4. Run all cells from top to bottom.

---

## Author

Meet Tailor — Data Science Learner

GitHub: https://github.com/MeetTailor-Data

---

## License

Created for learning and educational purposes only.
