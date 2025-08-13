# Final-Project - Titanic

## 1. Project Overview
The goal of this project is to predict which kinds of people were more likely to survive the Titanic disaster using Kaggle’s Titanic dataset.

We explored the data, cleaned and preprocessed it, engineered new features, trained different models, and compared their performance to find the best approach.

## 2. Dataset
Source: [Kaggle — Titanic Competition](https://www.kaggle.com/c/titanic)

The dataset is split into:
- **train.csv** → contains passenger details and the target variable (`Survived`)
- **test.csv** → contains passenger details without the survival outcome
- **gender_submission.csv** → sample submission file

**Key Features:**
- Pclass: Passenger class (1, 2, 3)
- Sex: Gender
- Age: Age in years
- SibSp: Number of siblings/spouses aboard
- Parch: Number of parents/children aboard
- Fare: Ticket price
- Embarked: Port of embarkation (C, Q, S)
- Cabin, Ticket, Name: New features

**Target:**
- Survived: 1 = Survived, 0 = Did not survive

## 3 Exploratory Data Analysis (EDA)
- Checked missing values
- Visualized survival rates by gender, class, and age.
- Observed:
  - Women had a much higher survival rate than men.
  - First-class passengers survived more often than lower classes.
  - Higher ticket prices were linked to better survival.

## 4. Data Cleaning
- Filled missing **Age** with the median.
- Filled missing **Embarked** with the most frequent port.
- Filled missing **Cabin** with the most common deck.
- Checked and treated outliers for **Age** and **Fare**.

## 5. Feature Engineering
- Converted categorical variables (Sex, Embarked, Pclass) to numeric.
- Created:
  - **FamilySize** = SibSp + Parch + 1
  - **IsAlone** = 1 if passenger traveled alone, else 0
- Dropped irrelevant features like Name, Ticket, and PassengerId for modeling.

## 6. Modeling & Evaluation
We split the data into: 80% training and 20% testing

Trained the following models:
- Logistic Regression
- Decision Tree
- Support Vector Machine (SVM)
- Random Forest
- K-Nearest Neighbors (KNN)

**Evaluation metric:** Accuracy score on the test set.

| Model               | Accuracy |
|---------------------|----------|
| Logistic Regression | 0.82     |
| Decision Tree       | 0.81     |
| SVM                 | 0.81     |
| Random Forest       | 0.79     |
| KNN                 | 0.77     |

## 7. Conclusion
For this project, **Logistic Regression** performed the best with an accuracy of **82%**, slightly outperforming Decision Tree and SVM (both 81%).  

The results align with historical accounts — survival chances were higher for:
- Women  
- First-class passengers  
- People who paid higher ticket fares  
- Passengers traveling in small family groups 
