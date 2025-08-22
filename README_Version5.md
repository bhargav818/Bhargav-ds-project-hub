# Census Income Project

This project is a Machine Learning workflow built to analyze and predict annual income levels (<=50K or >50K) using the U.S. Census Income dataset. The project guides you through the end-to-end Data Science process, including data loading, cleaning, exploratory data analysis, outlier handling, and is set up for building predictive models.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Project Steps](#project-steps)
- [Requirements](#requirements)
- [How to Run](#how-to-run)
- [Notebook Structure](#notebook-structure)
- [Results & Insights](#results--insights)
- [References](#references)

---

## Overview

The goal of the project is to predict whether a person’s annual income exceeds $50K based on census data. The workflow includes:

- Data Loading and Inspection
- Data Cleaning (handling missing values, duplicates)
- Exploratory Data Analysis (EDA) and Visualization
- Outlier Detection and Handling
- Feature Engineering (if extended)
- Model Building and Evaluation (Logistic Regression, etc.)

## Dataset

The dataset used is the U.S. Census Income dataset (`census_income.csv`), which contains 15 columns and over 32,000 rows. The target variable is `annual_income`.

**Key Features:**
- Demographics: Age, Sex, Race, Education, Marital Status, Native Country
- Work: Workclass, Occupation, Hours-per-week, Capital-gain/loss, etc.
- Target: `annual_income` (<=50K or >50K)

## Project Steps

1. **Import Libraries**  
   Standard Python ML libraries (NumPy, Pandas, Matplotlib, Seaborn, scikit-learn).

2. **Data Loading**  
   Load the CSV dataset and inspect its structure.

3. **Data Cleaning**  
   - Handle missing values by replacing "?" with `np.nan` and dropping or imputing as needed.
   - Remove duplicate rows.
   - Convert data types as needed.

4. **Exploratory Data Analysis (EDA)**  
   - Visualize distributions, boxplots, and check for outliers.
   - Explore categorical and numerical features.

5. **Outlier Detection & Handling**  
   - Visualize and optionally remove outliers using IQR.
   - Decide which outliers to keep based on domain knowledge and EDA.

6. **(Next Steps)**  
   - Encode categorical variables for ML.
   - Split data into training and testing sets.
   - Build and evaluate classification models.

## Requirements

- Python 3.7+
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- Jupyter Notebook or any compatible notebook environment

## How to Run

1. Clone the repository or download the notebook and dataset.
2. Make sure the dataset (`census_income.csv`) is in the same directory as the notebook.
3. Install the required Python libraries if not already present.
   ```
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
4. Open the notebook:
   ```
   jupyter notebook Census\ Income\ Project.ipynb
   ```
5. Run each cell in sequence to execute the workflow.

## Notebook Structure

- **Section 1:** Import Libraries
- **Section 2:** Data Loading and Inspection
- **Section 3:** Data Cleaning
- **Section 4:** EDA and Visualization
- **Section 5:** Outlier Detection and Handling
- **Section 6:** (To be added) Feature Engineering & Modeling

## Results & Insights

- Proper data cleaning significantly improved data quality.
- Outlier removal was considered, but >30% of data were outliers, so most were retained.
- The dataset is now ready for encoding and predictive modeling.

## References

- [UCI Machine Learning Repository: Adult Data Set](https://archive.ics.uci.edu/ml/datasets/adult)
- [scikit-learn documentation](https://scikit-learn.org/stable/documentation.html)
- [Pandas documentation](https://pandas.pydata.org/)

---

*Project by [Your Name]. For academic and learning purposes.*