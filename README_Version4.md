# 🛒 Purchase Case Study – Statistical Analysis & Machine Learning

This project is an end-to-end exploratory and statistical analysis of a large purchase dataset (similar to the Black Friday dataset). It demonstrates a typical **machine learning/data science pipeline** on structured transaction data, including data cleaning, EDA, preprocessing, and hypothesis testing.

---

## 📁 Dataset

- **Source:** `purchase_data.csv` (columns: User_ID, Product_ID, Gender, Age, Occupation, City_Category, Stay_In_Current_City_Years, Marital_Status, Product_Category_1/2/3, Purchase)
- **Size:** ~260,000 rows, 12 columns

---

## 🛠️ Key Steps & Methodology

### 1. **Data Loading & Inspection**
- Read CSV with pandas
- Initial exploration: `df.info()`, `df.head()`, checking unique values, datatypes

### 2. **Data Cleaning**
- Handling categorical values like "4+" for years (converted to int)
- Imputing/filling missing values for product categories
- Dropping rows with any remaining nulls
- Outlier detection and removal using IQR method
- Duplicates check

### 3. **Preprocessing**
- Label encoding for categorical columns (`Gender`, `Age`, `City_Category`, `Product_ID`)
- Ensured all columns are of appropriate types for analysis

### 4. **Exploratory Data Analysis (EDA)**
- Visualizations (boxplots, value counts, etc.)
- Distribution of key features
- Summary statistics

### 5. **Statistical Analysis / Hypothesis Testing**
- **One-sample t-test:** Is the average purchase by men aged 18-25 still ₹10,000?
- **Proportion z-test:** Is the % of women spending >₹10,000 still 35%?
- (Templates for more: group comparison by age/gender, etc.)

---

## 📈 Example Hypotheses Tested

- **a) Has the average purchase by men (18–25) changed from ₹10,000?**
    - Used a one-sample t-test.
- **b) Is the % of women who spend more than ₹10,000 still 35%?**
    - Used a one-proportion z-test.
- **More:** Templates for comparing means/proportions across ages and genders.

---

## 🔑 How to Run

1. Clone/download this repo.
2. Place your `purchase_data.csv` in the working directory.
3. Install requirements:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn scipy statsmodels
   ```
4. Open & run `Purchase_Case_Study.ipynb` in Jupyter/Colab.

---

## 📋 Notebook Structure

- **Section 1:** Data loading, cleaning, and preprocessing
- **Section 2:** EDA and visualization
- **Section 3:** Outlier removal, label encoding
- **Section 4:** Statistical tests (with explanations)
- **Section 5:** Result interpretation and conclusions

---

## 📝 Notes

- The code includes handling for common real-world dataset issues (missing/categorical values).
- All statistical tests are explained in markdown cells for clarity.
- Easily adaptable for further ML modeling or additional hypothesis testing.

---

## 📚 References

- [Pandas Documentation](https://pandas.pydata.org/)
- [Scipy Stats](https://docs.scipy.org/doc/scipy/reference/stats.html)
- [Statsmodels Proportion Z-Test](https://www.statsmodels.org/stable/generated/statsmodels.stats.proportion.proportions_ztest.html)

---

## 👤 Author

- [Your Name]  
- [Your Contact/LinkedIn/GitHub]

---

## 📄 License

For educational use only.

---