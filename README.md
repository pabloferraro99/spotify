# 🎵 Songs Popularity Prediction Model

This repository presents a machine learning solution to predict the **popularity of songs** using a dataset of 2,300 tracks with audio features and metadata. The final model, a **Random Forest classifier**, achieved **73.41% accuracy** and **73% F1-score**, offering actionable insights for music producers and stakeholders.

---

## 📌 Executive Summary

- Dataset: 2,300 songs, 891 unique artists, covering years 2000–2022.
- Objective: Predict whether a song is "popular" (popularity score ≥ 72).
- Final model: Random Forest with optimized hyperparameters.
- Top predictors: **Artist popularity**, **popular genre presence**, and audio features like **speechiness**, **energy**, **valence**, **danceability**, and **tempo**.
- Insights: Songs that are **lyrical, happy, energetic, and danceable** tend to be more popular.

---

## ⚙️ Approach

### 1. Data Exploration
- Analysis of artist counts, genres (438 unique), and popularity score distribution.
- Detected data skew due to Spotify's algorithm favoring recent plays.

### 2. Pre-processing
- Removed missing/duplicate data (some directly in Excel).
- Transformed and normalized values for modeling.
- Engineered new features (e.g., `genre_score` based on genre frequency).
- Selected final features via correlation, domain logic, and PCA evaluation.

### 3. Model Training & Prediction
- Split data into train/test sets.
- Tested models: Logistic Regression, Decision Trees, KNN, Bagging, Boosting, Random Forest.
- Grid search performed (offline) to optimize each model's parameters.

### 4. Model Validation
- Evaluated with **Accuracy** and **F1 score**, especially important due to class imbalance.
- Chose optimal threshold balancing precision and recall on popular songs.

---

## 📈 Results

- ✅ Final Model: **Random Forest**
- 🎯 Accuracy: **73.41%**
- 📊 F1 Score: **73%**
- 📌 Best predictors: artist popularity, genre score, speechiness, energy, valence, danceability, tempo.

---

## 📦 Files Included

- `ultimate.ipynb`: Complete code and modeling pipeline.
- `Songs_2024.xlsx`: Cleaned dataset used for model training.


---

## 🛠️ Tech Stack

- Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)
- Jupyter Notebook
- Excel (initial preprocessing)

---

## 📘 References

- Spotify API documentation: [Spotify Web API](https://developer.spotify.com/documentation/web-api)

---

## ✉️ Contact

For more info or collaboration, connect via [LinkedIn](https://www.linkedin.com/in/pabloferraro99).
