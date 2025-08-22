# Purchase Data Analysis & Statistical Inference

This project explores purchase behavior using a large retail dataset, focusing on data cleaning, preprocessing, exploratory data analysis (EDA), feature engineering, and hypothesis testing with Python.

---

## Dataset Overview

The dataset contains anonymized records of customer purchases with the following key columns:

- **User_ID**: Unique identifier for each user
- **Product_ID**: Unique identifier for each product
- **Gender**: Gender of the purchaser (encoded)
- **Age**: Age group of the purchaser (encoded)
- **Occupation**: Occupation code
- **City_Category**: Category of the user's city (encoded)
- **Stay_In_Current_City_Years**: Number of years the user has stayed in their current city
- **Marital_Status**: Marital status (binary)
- **Product_Category_1/2/3**: Product category codes
- **Purchase**: Purchase amount

There are ~263,000 rows and 12 columns.

---

## Project Workflow

### 1. Data Loading & Initial Checks

- Read CSV data into a pandas DataFrame.
- Inspect shape, data types, sample values, and check for missing values.
- Handle outliers, duplicates, and inconsistent values.

### 2. Data Cleaning

- Convert categorical columns to consistent types.
- Replace or impute missing values (e.g., fill NAs in categories with 0).
- Encode categorical variables using `LabelEncoder` for ML compatibility.

### 3. Feature Engineering

- Transform columns (e.g., map `Stay_In_Current_City_Years` to integer).
- Create new features if necessary for analysis.

### 4. Exploratory Data Analysis (EDA)

- Use `matplotlib` and `seaborn` to visualize purchase distributions, boxplots for outlier detection, and categorical breakdowns.
- Analyze purchase behavior by gender, age group, city, etc.

### 5. Outlier Handling

- Apply IQR method to remove outliers from the `Purchase` column.

### 6. Statistical Analysis & Hypothesis Testing

- **One-sample t-test:** Test if the average purchase amount for men aged 18-25 is still 10,000.
- **Proportion z-test:** Test if the percentage of women spending more than 10,000 is still 35%.
- Prepare samples, set null/alternative hypotheses, run the appropriate test, and interpret p-values.

### 7. Results & Interpretation

- State statistical findings and business implications.
- Example: The average purchase for 18-25 men is **not** 10,000; the percentage of women spending >10,000 is **not** 35%, etc.

---

## Notebooks & Code

All steps are in [Purchase_Case_Study.ipynb](./Purchase_Case_Study.ipynb).  
The code uses Python 3, pandas, numpy, matplotlib, seaborn, scikit-learn, and statsmodels.

---

## How To Run

1. Clone this repository and place the data file (e.g., `purchase_data.csv`) alongside the notebook.
2. Open the notebook with Jupyter or Google Colab.
3. Run step by step to reproduce results or adapt for new analyses.

---

## Requirements

- Python 3.7+
- pandas, numpy, matplotlib, seaborn, scikit-learn, statsmodels

Install requirements (if needed):

```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels
```

---

## Key Learnings

- Practical data cleaning and feature engineering for real-world datasets.
- Label encoding for ML pipelines.
- EDA for understanding business questions.
- Robust hypothesis testing (t-test, z-test) directly on real purchase data.

---

## Author

- [Your Name]
- [Your GitHub profile or contact]

---

**Feel free to use, adapt, or extend this template for your own retail or statistical analysis projects!**