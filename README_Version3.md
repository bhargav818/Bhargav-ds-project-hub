# Netflix Movie Recommendation System

This project implements a **movie recommendation system** for Netflix user ratings using collaborative filtering and the SVD (Singular Value Decomposition) algorithm from the `scikit-surprise` library. The overall workflow includes data preprocessing, exploratory data analysis, filtering, and building a predictive model to estimate user ratings for movies.

---

## 📂 Dataset

- **User Ratings Dataset:** Large dataset containing user ratings for Netflix movies.
- **Movies Metadata:** Contains movie IDs, titles, and genres.

---

## 📋 Project Workflow

1. **Data Loading**
   - Load raw Netflix rating data and movie metadata using pandas.

2. **Data Cleaning & Preprocessing**
   - Identify movie IDs and user IDs.
   - Remove rows with missing values.
   - Assign each rating to the correct movie using movie IDs.
   - Filter out movies with very few ratings to improve model performance.

3. **Exploratory Data Analysis**
   - Calculate statistics such as number of movies, number of users, and rating distributions.
   - Group and summarize ratings by movie.

4. **Data Filtering**
   - Filter out movies that do not meet a minimum number of ratings (using a quantile threshold).
   - Prepare a final dataset for model training.

5. **Recommendation Model**
   - Use the SVD algorithm from `scikit-surprise` for collaborative filtering.
   - Perform cross-validation to evaluate the model using RMSE and MAE metrics.
   - Predict ratings for a sample user and recommend movies.

6. **Personalized Recommendations**
   - Generate and display top movie recommendations for a specific user by merging predictions with movie metadata.

---

## 🛠️ Technologies Used

- **Python** (Pandas, NumPy, Seaborn, Matplotlib)
- **scikit-surprise:** For collaborative filtering and SVD.
- **Jupyter Notebook:** For interactive development and visualization.

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone <repo-url>
cd <repo-directory>
```

### 2. Install Dependencies

```bash
pip install pandas numpy seaborn matplotlib scikit-surprise
```

- Note: If you encounter `numpy` or `scikit-surprise` compatibility issues, ensure you are using compatible versions (e.g., numpy==1.26.4).

### 3. Run the Notebook

Open `NETFLIX_Project.ipynb` in Jupyter Notebook or Google Colab and follow the code cells step by step.

---

## 📊 Example Results

- **EDA:** Rating distribution, most/least rated movies, average ratings per movie.
- **Model Evaluation:** Shows cross-validation scores (RMSE/MAE) for SVD.
- **Sample Recommendation:** Displays a list of highly rated movies for a given user with predicted ratings and genres.

---

## 📝 Notes

- The dataset is very large; consider sampling or filtering for faster experimentation.
- The recommendation quality depends on data sparsity and filtering thresholds.

---

## 🙏 Acknowledgements

- **Netflix Prize Dataset** or similar open movie rating datasets.
- [scikit-surprise documentation](https://surprise.readthedocs.io/en/stable/)

---

## 📄 License

This project is for educational and research purposes only.

---