# SPACESHIP TITANIC
This notebook tackles the **Spaceship Titanic** Kaggle competition, where the task is to predict whether a passenger was transported to another dimension following a spacetime anomaly.

---

##  Problem Statement

Given data on passengers' demographics, onboard spending, and travel context, predict the binary target:  
**`Transported`** → `True` or `False`

---

##  Datasets

- `train.csv` – Used to train and validate the model

- `test.csv` – Final submission predictions made here

- `sample_submission.csv` – Format for submission

### Key Features Used
- `HomePlanet`, `CryoSleep`, `Cabin`, `Destination`, `Age`

- Luxury amenity spend: `RoomService`, `FoodCourt`, `ShoppingMall`, `Spa`, `VRDeck`

- `Name`, `PassengerId` used for engineering group features

---

##  Steps Covered

### 1. **EDA & Preprocessing**
- Missing value imputation using grouped medians, spending logic, and spatial reasoning

- Feature engineering: 
  - `CabinNum`, `Deck`, `Side`, `TotalSpend`, `AgeGroup`

  - Group features: `GroupId`, `FamilySize`, `IsAlone`, `SameCabinFlag`

  - `VIP_DeckCombo` interaction feature

- Categorical one-hot encoding

### 2. **Modeling**
- Base models: `Logistic Regression`, `Random Forest`

- Model comparison using stratified cross-validation

- Ensemble techniques:
  - **Voting Classifier (Soft Voting)**

  - **Stacking Classifier** (meta model: Logistic Regression)

### 3. **Threshold Tuning**
- Optimized probability threshold for classification using F1 Score

- Visualized trade-offs between precision, recall, F1

---

##  Best Model Performance (Voting Classifier + Tuned Threshold)

| Metric     | Score   |
|------------|---------|
| Accuracy   | ~0.9434 |
| F1 Score   | ~0.9422 |
| ROC AUC    | ~0.9436 |

> Final submission achieved **0.79658** on the public Kaggle leaderboard.

---

##  Requirements

All dependencies are listed in `requirements.txt`. Install using:

```bash

pip install -r requirements.txt

```

---
# Owner
```
Michael Bond  
bondpapi@yahoo.com  
https://github.com/bondpapi  
https://www.hackerrank.com/profile/bondpapi  
