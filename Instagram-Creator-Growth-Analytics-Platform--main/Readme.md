# 📈 Insta-Insight: Instagram Creator Growth Analytics

- **Dataset:** [View on Kaggle](https://www.kaggle.com/datasets/amankumarkharwal/instagram-reach-data)
- **Notebook:** [View Analysis](<Instagram Reach Analysis.ipynb>)

## 📌 Overview

What actually drives an Instagram creator's viral success? Is it strictly hashtag usage, or do hidden factors like Explore page distribution and profile conversion rates play a bigger role?

**Instagram Creator Growth Analytics** is a machine learning pipeline built to answer that question. It analyzes engagement variables and traffic sources to predict a post's total impressions. More importantly, it translates those predictions into actionable advice—helping content creators understand which metrics, such as saves and profile visits, influence reach.

---

## 🚀 Visual Analytics & Distributions

Machine learning shouldn't be a black box. Understanding where traffic comes from is the first step toward optimizing content performance.

### 1. The Home Feed Baseline

Most baseline impressions originate from the home feed, representing reach from existing followers.

![Distribution of Impressions From Home](<images/Screenshot 2026-08-09 001328.png>)

### 2. The Hashtag Catalyst

Hashtag reach exhibits a right-skewed distribution, indicating that successful hashtag optimization can significantly increase visibility beyond the core audience.

![Distribution of Impressions From Hashtags](<images/Screenshot 2026-08-09 001340.png>)

### 3. The Explore Page Jackpot

Explore reach shows substantial variation, highlighting the potential of Explore distribution to drive large increases in impressions.

![Distribution of Impressions From Explore](<images/Screenshot 2026-08-09 001352.png>)

---

## 🧠 Approach & Key Findings

### Phase 1: Exploratory Data Analysis (EDA)

Before training the models, we analyzed the dataset to uncover patterns in traffic sources, engagement, and follower conversion.

**Key Insights:**

- **The Explore Factor:** Explore impressions show the strongest correlation with overall impressions (**0.89**), making Explore distribution a major driver of reach.

- **The Conversion Rate:** The profile shows a **41.00% follower conversion rate** (`Follows / Profile Visits`), indicating strong conversion of profile visitors into followers.

- **Engagement Disparities:** Likes show a strong positive correlation with reach (**0.85**), while comments have a negligible and slightly negative correlation (**-0.03**).

### Phase 2: Model Training & Evaluation

To forecast post reach, we trained regression models to estimate total impressions using engagement signals such as:

- Likes
- Saves
- Comments
- Shares
- Profile Visits
- Follows

**Model Performance:**

- **SGD Regressor (Passive Aggressive Tuning): 90.17% R² 🏆**

The final model used `SGDRegressor` with an epsilon-insensitive loss function, no regularization penalty, and a passive-aggressive learning schedule. It achieved an **R² score of approximately 90.17%** on the evaluation data.

---

## 🛠️ Tech Stack

- **Core:** Python, Pandas, NumPy
- **Machine Learning:** Scikit-Learn
- **Statistical Analysis:** Statsmodels
- **Visualization:** Matplotlib, Seaborn, Plotly
- **Dependencies:** `requirements.txt`

---

## 📊 Project Highlights

- Analyzed **50,000+ user interactions** to identify engagement and reach patterns.
- Identified **Explore reach** as the strongest predictor of overall impressions.
- Achieved a **90.17% R² score** using an optimized SGD Regressor.
- Analyzed relationships between engagement, profile visits, follows, and impressions.
- Built interactive visualizations using **Plotly** and **Seaborn**.

---

## 📞 Let's Connect

- **LinkedIn:** [Rahul Kumar Srivastava](https://www.linkedin.com/in/rahulkumarsrivastava/)
- **Email:** [rahulkumarsrivastava90@gmail.com](mailto:rahulkumarsrivastava90@gmail.com)

---

*If you found these insights or the code structure helpful, feel free to drop a ⭐ on the repository!*
