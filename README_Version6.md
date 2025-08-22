# CSGO Round Winner Prediction Project

This project leverages machine learning to predict the winner (CT or T) of a round in Counter-Strike: Global Offensive (CSGO) using in-game data. By applying feature selection and multiple classification algorithms, it aims to identify the most impactful features and the best-performing model for round outcome prediction.

---

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Project Workflow](#project-workflow)
- [Feature Selection](#feature-selection)
- [Modeling](#modeling)
- [Results](#results)
- [Requirements](#requirements)
- [How to Run](#how-to-run)
- [References](#references)

---

## Overview

The goal is to predict the outcome of a CSGO round (whether the Counter-Terrorists (CT) or Terrorists (T) win) given detailed round statistics, player information, and equipment data. The project demonstrates the complete ML workflow, including:

- Data loading and cleaning
- Label encoding and preprocessing
- Exploratory data analysis
- Feature importance via Linear Discriminant Analysis (LDA)
- Training and evaluating Logistic Regression, Decision Tree, Random Forest, and SVM classifiers
- Model comparison and insights

---

## Dataset

- **Input File:** `csgo.csv`
- **Rows:** ~122,000
- **Columns:** 97
- **Features:** 
  - Game state (time left, scores, map, bomb status, etc.)
  - Player stats (health, armor, helmets, money, weapons, grenades, etc.)
  - Target: `round_winner` (`CT` or `T`)

---

## Project Workflow

1. **Data Import and Initial Checks**
   - Load data with pandas
   - Inspect shape, types, missing values, and unique targets

2. **Preprocessing**
   - Encode categorical columns (`map`, `round_winner`)
   - Remove duplicates
   - Check for and confirm no missing values

3. **Feature Selection**
   - Use Linear Discriminant Analysis (LDA) to compute importance of each feature
   - Select top 20 features for modeling

4. **Data Splitting and Scaling**
   - Split data into training and test sets (80/20)
   - Scale features for improved model performance

5. **Model Training & Evaluation**
   - Train and test the following classifiers:
     - Logistic Regression
     - Decision Tree
     - Random Forest
     - Support Vector Machine (SVM)
   - Evaluate with accuracy, precision, recall, and F1-score

6. **Model Comparison and Insights**
   - Compare classification reports to determine the best model

---

## Feature Selection

- LDA was used to identify the top 20 most informative features (e.g., `t_armor`, `ct_armor`, `t_weapon_ak47`, `ct_weapon_m4a4`, health, alive players, etc.)
- These features were used for all downstream modeling to avoid overfitting and improve interpretability.

---

## Modeling

Four models were trained and evaluated:

| Model               | Test Accuracy | Notes                |
|---------------------|--------------|----------------------|
| Logistic Regression | ~76%         | Fast, interpretable  |
| Decision Tree       | ~81%         | Captures non-linearities, risk of overfitting |
| Random Forest       | ~86%         | Best performer; robust |
| SVM                 | ~78%         | Effective, slower on large data |

Random Forest achieved the best results in this pipeline.

---

## Results

- **Random Forest** achieved the highest accuracy and balanced precision/recall for both CT and T classes.
- Features such as armor, health, certain weapons, and bomb status are highly predictive of the round outcome.
- Reducing features via LDA improved performance and generalizability.

---

## Requirements

- Python 3.7+
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- Jupyter Notebook (recommended)

Install requirements via:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## How to Run

1. Place `csgo.csv` and the notebook in the same directory.
2. Open the notebook (`CSGO Project.ipynb`) in Jupyter.
3. Run cells sequentially to execute the workflow.
4. View model outputs and classification reports at the end of the notebook.

---

## References

- [scikit-learn Documentation](https://scikit-learn.org/stable/)
- [Pandas Documentation](https://pandas.pydata.org/)
- [CSGO Data Sources](https://www.kaggle.com/) (for similar datasets)

---

*Project by [Your Name]. For academic/learning purposes only.*