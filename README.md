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

### 🧠 **Modeling & Prediction (Phase 2)**

* **Objective:** Predict whether a movie's audience score is **positive** (>=50%) or **negative** (<50%).
* **Algorithms Used:**

  * XGBoost (primary model)
  * Random Forest
  * Voting Classifier (XGBoost + Random Forest + SVM)
  * Logistic Regression with TF-IDF
* **Text Features:**

  * TF-IDF vectors derived from movie synopsis
  * Sentiment analysis using TextBlob

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


