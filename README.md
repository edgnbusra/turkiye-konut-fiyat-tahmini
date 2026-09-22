# Turkey Real Estate Price Prediction

A regression project in two parts: a machine learning fundamentals exercise on a classic built-in dataset, followed by a real-world price prediction model built on actual Turkish real estate listings.

## Part 1: California Housing Price Prediction

**Goal:** build the fundamentals of classic machine learning and understand linear regression using Scikit-learn's built-in dataset.

**Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn.

**Steps:**
- Loaded the `fetch_california_housing` dataset.
- Explored the data structure (column names translated for readability).
- Split the data 80/20 into train/test sets with `train_test_split`.
- Trained a Linear Regression model.
- Evaluated performance with MSE and R2 score, with results plotted.

**Result:** R2 = 0.5758, MSE = 0.5559.

## Part 2: Real Turkish Real Estate Price Prediction

**Goal:** go beyond a toy dataset and work with real Turkish real estate market data, handling categorical features (province, district, seller type, etc.) to make them model-ready.

**Libraries:** Pandas, Scikit-learn.

**Steps:**
- Pulled a real Turkish real estate dataset (`real-estate-prices-in-turkey-2025`) from Kaggle.
- Cleaned the free-text `Oda_Sayisi` (room count) column (e.g. "3+1") into a numeric `Toplam_Oda` (total rooms) column.
- One-hot encoded categorical columns (province, district, seller type) into numeric form.
- Trained the model on 12,220 rows (test set: 3,056 rows) and computed the R2 score.
- Built an interactive prediction panel that takes a province, district, square meters, and room count as input and returns a price estimate in Turkish Lira (TL).

**Result:** R2 = 0.4057, MSE = 6,179,937,398,045.79 (the large MSE reflects raw TL-price-squared units - housing prices in Turkey range from the hundreds of thousands to tens of millions of TL, so squared errors at that scale are naturally very large numbers; R2 is the more interpretable metric here).

## Tech stack

Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn.

## Data

The Turkish real estate dataset is not included in this repo - it's pulled from Kaggle (`real-estate-prices-in-turkey-2025`) via the Kaggle API inside the notebook.
