# Supply Chain Product Data Analysis

This project presents a comprehensive data analysis and preprocessing pipeline on a large supply chain product dataset (27,555 rows × 10 columns) using Python, pandas, NumPy, Matplotlib, and Seaborn. The dataset contains information on various products, their categories, brands, prices, ratings, and descriptions.

## Contents

- Data loading and initial exploration
- Data cleaning: Handling missing values, duplicates, and outliers
- Feature engineering: Discount calculation, rating categorization, etc.
- Exploratory Data Analysis (EDA): Visualizations and insights
- Brand and category analysis
- Data preparation for downstream ML tasks

## Dataset Overview

The dataset contains the following columns:

- `index`: Unique product ID
- `product`: Product name
- `category`: Product's main category
- `sub_category`: Subcategory within main category
- `brand`: Brand name
- `sale_price`: Sale price of the product
- `market_price`: Market price of the product
- `type`: Product type
- `rating`: Customer rating (float, may have missing values)
- `description`: Product description

## Notebooks & Workflow

All steps are documented in a Jupyter notebook (`Supply Chain Project.ipynb`):

### 1. Data Loading and Exploration

- Import libraries and suppress warnings
- Load dataset and display basic info and sample rows
- Check for nulls, data types, duplicated records, and unique values

### 2. Data Cleaning

- Identify and fill missing values for `product`, `brand`, and `description` with 'unknown'
- Impute missing `rating` values using category-wise mean, then overall mean if still missing
- Drop unnecessary columns (like `description` when not needed for analysis)

### 3. Feature Engineering

- Create a `discount` and `discount_%` feature
- Categorize ratings into bins (e.g., 0-1, 1-2, etc.)
- Visualize rating distributions and discount statistics

### 4. Exploratory Data Analysis (EDA)

- Bar plots for highest-rated categories
- Pie chart for distribution of discounted vs. undiscounted products
- Brand-level average discount and rating analysis
- Product count per category and brand
- Trend visualizations for market price and other numerical columns

### 5. Insights

- Which categories and brands have the highest ratings?
- Which brands offer the highest/lowest average discounts?
- Distribution of ratings and discounts across the dataset
- Product mix across categories and brands

## Key Libraries Used

- **numpy** & **pandas**: Data manipulation and preprocessing
- **matplotlib.pyplot** & **seaborn**: Data visualization
- **Jupyter Notebook**: Interactive development and documentation

## How to Run

1. Clone this repository and place the dataset CSV file (`BBData -Ashwin.csv`) in the root directory.
2. Open `Supply Chain Project.ipynb` in Jupyter Notebook or JupyterLab.
3. Run the notebook cells in order to reproduce the data cleaning, analysis, and visualizations.

## Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- jupyter

You can install the required packages using pip:
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

## Notes

- The dataset is assumed to be anonymized and free of sensitive information.
- For large datasets, some visualizations may take time or require more memory.

## Author

- [Your Name]
- [Contact or GitHub link]

---

Feel free to use and adapt this notebook for your own supply chain or product data analytics and ML projects!