# Titanic Survival Prediction 
## Data Understanding & Visualization

## Project Overview
This project analyzes the **Titanic passenger dataset** to predict survival. The main focus is on **understanding the dataset** and exploring feature relationships using **visualization techniques**. 
After data exploration, a **Random Forest Classifier** is used to build a predictive model.

---

## Key Objectives
* Perform **Exploratory Data Analysis (EDA)** to understand:
   - Feature distributions
   - Relationships between variables
   - Missing data patterns
* Encode categorical features and handle missing values.
* Visualize patterns using:
   - **Bar plots**
   - **Histograms**
   - **Box plots**
   - **Heatmaps**
* Train a **Random Forest model** to predict survival and evaluate its performance.

---

## Dataset
- Columns used:
  - `Pclass`, `Sex`, `Age`, `SibSp`, `Parch`, `Fare`, `Embarked`, `Survived`
- Additional engineered features:
  - `FamilySize` = `SibSp + Parch + 1`

---

## Methodology

### 1. Data Cleaning
- Dropped irrelevant columns (`PassengerId`, `Name`, `Ticket`, `Cabin`)
- Filled missing values:
  - `Age` → median by passenger class
  - `Sex` → mode
  - `Embarked` → mode
- Encoded categorical variables:
  - `Sex`: male → 0, female → 1
  - `Embarked`: S → 1, C → 2, Q → 3

### 2. Exploratory Data Analysis & Visualization
- **Univariate Analysis**:
  - Count plots for `Survived` and `Sex`
  - Histograms for `Age`
- **Bivariate Analysis**:
  - Bar plots: Survival vs Gender, Survival vs Pclass
  - Box plots: Age vs Survival
- **Multivariate Analysis**:
  - Bar plots with `hue` for Pclass & Gender
  - Correlation heatmaps

### 3. Model Training
- Split dataset: `80% train`, `20% test`
- Trained **Random Forest Classifier**
- Evaluated performance using:
  - Accuracy
  - Confusion matrix
  - Classification report
- Visualized **feature importance** to identify key predictors.

---

## Key Findings
- **Females** had significantly higher survival rates.
- Important predictors of survival:
  - `Sex`, `Pclass`, `Title`, `FamilySize`
- Random Forest model achieved **high accuracy** and captured non-linear relationships.
