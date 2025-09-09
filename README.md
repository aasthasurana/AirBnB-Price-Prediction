# 🏡 Airbnb Price Prediction

This project develops a **machine learning model** to predict Airbnb listing prices using structured data on property attributes, host characteristics, and reviews. The goal is to help **hosts, guests, and Airbnb** make informed, data-driven pricing decisions.

---

## 📌 Project Overview
- **Problem Statement**  
  - *For Hosts:* Set competitive yet profitable rates, improving occupancy and revenue.  
  - *For Guests:* Increase transparency in pricing for informed decisions.  
  - *For Airbnb:* Optimize pricing to enhance competitiveness and user satisfaction.  

- **Motivation**  
  Pricing in the sharing economy is highly dynamic. This study explores factors influencing Airbnb prices by analyzing attributes like location, property type, amenities, and reviews.

- **Objectives**  
  1. Identify key determinants of Airbnb pricing.  
  2. Build robust predictive models to estimate log-transformed prices.  
  3. Provide actionable insights and recommendations for hosts and Airbnb.  

---

## 📊 Dataset
- **Source:** [Inside Airbnb](https://insideairbnb.com/get-the-data/) and [Kaggle Dataset](https://www.kaggle.com/datasets/stevezhenghp/airbnb-price-prediction)  
- **Entries:** 74,111 listings  
- **Features:** 29 (property details, host info, reviews, location)  
- **Cities Covered:** New York, Washington DC, San Francisco, Los Angeles, Chicago, Boston  
- **Target Variable:** `log_price` (log-transformed listing price)  

---

## ⚙️ Methodology
1. **Data Cleaning**  
   - Handled missing values in bedrooms, bathrooms, reviews, and host attributes.  
   - Dropped irrelevant columns (`id`, `description`, `thumbnail_url`).  
   - Imputed missing values using medians and logical assumptions.  

2. **Exploratory Data Analysis (EDA)**  
   - Distribution of log prices  
   - Price trends across **cities, property types, and room types**  
   - Correlations between numerical features  

3. **Feature Engineering**  
   - Created `host_since_year`, `response_rate_range`  
   - Target encoding for categorical variables  
   - Scaled numerical features  

4. **Modeling & Evaluation**  
   - Models tested: Linear Regression, Ridge, SVR, Gradient Boosting  
   - Cross-validation with RMSE and R²  
   - Hyperparameter tuning: Randomized Search, Grid Search, Bayesian Optimization  

---

## 🚀 Results
- **Best Model:** Gradient Boosting Regressor  
  - **RMSE:** 0.34  
  - **R²:** 0.73 (test set)  
- **Top Predictors:**  
  - `room_type`, `bathrooms`, `longitude`, `accommodates`, `bedrooms`, `latitude`, `city`, `review_scores_rating`  

---

## 💡 Recommendations
1. **Hosts:** Highlight location and room type (entire homes/private rooms attract higher prices).  
2. **Airbnb:** Provide dynamic pricing tools that factor in seasonality and competition.  
3. **Guests:** Use transparent pricing indicators for fair comparisons.  
4. **Future Work:**  
   - Sentiment analysis of reviews  
   - External data (local events, safety scores, attractions)  
   - Time-series demand modeling  

---

## 🛠️ Tech Stack
- **Python**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `category_encoders`, `scikit-optimize`  
- **Colab Notebook** for cloud execution  
- **Plotly** for interactive visualizations  

