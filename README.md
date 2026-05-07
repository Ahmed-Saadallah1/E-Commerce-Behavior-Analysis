# E-Commerce Behavior Analysis

Exploratory data analysis and data preparation on the **Online Shoppers Purchasing Intention** dataset, built as part of the **Introduction to Data Science** course at **German International University (GIU)**, Spring 2026.

## Dataset

**Online Shoppers Purchasing Intention** — [Kaggle Link](https://www.kaggle.com/datasets/henrysue/online-shoppers-intention)

The dataset contains 12,330 sessions from an e-commerce website. The target variable is `Revenue` — a boolean indicating whether a session ended in a purchase.

## Project Structure

The notebook covers 5 parts:

### Part 1 — Dataset Understanding & Exploration
- First/last 12 rows display
- Rows, columns, data types
- Full dataset summary
- Target variable (`Revenue`) class distribution
- Categorical feature analysis (`VisitorType`)
- Descriptive statistics (mean, median, std, percentiles)
- Missing value detection
- Duplicate record removal

### Part 2 — Data Preparation
- Meaningful filtering (sessions with zero PageValues AND zero ProductRelated_Duration)
- Categorical encoding (Label + One-Hot)
- Normalization using StandardScaler
- Binning `PageValues` into 5 equal-width bins
- Missing value handling (median/mode)
- Feature selection via correlation analysis and chi-square test
- Class imbalance handling via stratified sampling

### Part 3 — Data Visualization
- Histogram of `PageValues`
- Boxplot of `ExitRates` by `Revenue`
- Scatterplot of `PageValues` vs `ProductRelated_Duration`
- Correlation heatmap

### Part 4 — Insight Discovery
- `PageValues > 0` sessions are dramatically more likely to result in purchase
- Returning visitors convert at a higher rate than new visitors
- Weekend sessions have a lower conversion rate than weekdays (counter-intuitive)
- Business recommendation: reduce exit rates on high-PageValue pages

### Part 5 — Feature Engineering
- `Engagement_Score` — combines total page visits and total duration
- `PageValue_per_Page` — average value generated per page visit
- `Bounce_Exit_Ratio` — ratio of BounceRates to ExitRates

## Technologies

- Python 3
- Pandas, NumPy
- Scikit-learn (StandardScaler, chi-square, train_test_split)
- Matplotlib, Seaborn
- Google Colab / Jupyter Notebook


**Course:** Introduction to Data Science — GIU, Spring 2026
