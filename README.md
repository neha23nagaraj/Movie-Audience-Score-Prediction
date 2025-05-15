## 🎬 Movie Audience Score Prediction

**Project Duration:** January 2025 - May 2025

### 📑 **Project Overview**

This project aims to predict the **audience score** of movies based on various features scraped from **Rotten Tomatoes**. The audience score is binarized as **positive (>=50%)** or **negative (<50%)**. The project consists of two phases:

1. **Data Scraping:** Collecting data from Rotten Tomatoes using Selenium and BeautifulSoup.
2. **Model Training & Prediction:** Building and evaluating machine learning models to predict audience score.

---

### 📂 **Data Collection (Phase 1)**

* **Source:** Rotten Tomatoes
* **Tools:** Selenium, BeautifulSoup
* **Features Collected:**

  * Movie Title
  * Rating (e.g., PG, R)
  * Release Date
  * Duration
  * Director
  * Cast
  * Synopsis
  * Genre
  * Critic Score
  * Critic Review Count
  * Audience Review Count
  * Audience Score

The collected data is stored in a structured **CSV file** for easy processing.

---

### Phase 2: Modeling & Prediction

#### 🧠 Objective

Predict whether a movie's audience score is positive (>=50%) or negative (<50%).

#### 🛠️ Data Preprocessing

* Converted movie duration from hours and minutes to total minutes.
* Encoded Rating using LabelEncoder.
* One-hot encoded Genre.
* Extracted top 10 directors and categorized others as "Other".
* Extracted presence of numbers in movie titles as a binary feature.
* Applied TF-IDF vectorization on movie synopsis.
* Multiplied Audience Review Count by 1000 for accurate representation.

#### 🚀 Modeling Approaches: Primary Model

**XGBoost Classifier**

* Achieved **80% accuracy** after tuning hyperparameters and handling class imbalance using `scale_pos_weight`.

#### 💡 Other Models Tried:

* Logistic Regression with TF-IDF
* XGBoost without TF-IDF

#### 📊 Best Accuracy:

**XGBoost with:**

* n\_estimators = 400
* max\_depth = 6
* learning\_rate = 0.05
* scale\_pos\_weight = 0.35/0.65

---

### 💡 **Key Results:**

* Achieved **80% accuracy** using XGBoost with optimized hyperparameters and balanced class weights.
* Implemented ensemble methods to further improve accuracy.
* Identified important features like **Genre, Critic Score, and Duration** as key predictors.

---

### 📊 **Visualization:**

* **Confusion Matrices** for performance evaluation.
* **Feature Importance** plots to highlight significant features.

---

### 🚀 **How to Run the Code:**

1. Clone the repository:

   ```bash
   git clone https://github.com/neha23nagaraj/movie-audience-score-prediction.git
   ```
2. Install the required libraries:

   ```bash
   pip install -r requirements.txt
   ```
3. Run the data scraping script (Phase 1):

   ```bash
   python scrape_movies.py
   ```
4. Run the prediction script (Phase 2):

   ```bash
   python predict_score.py
   ```
5. View results in the **output CSV** or plots generated.

---

### 📚 **Future Improvements:**

* Add **sentiment analysis** for audience reviews.
* Explore **deep learning models** for textual data.
* Implement **streaming data scraping** for continuous updates.


