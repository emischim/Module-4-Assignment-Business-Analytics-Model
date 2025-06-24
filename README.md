# Requirement Clarity Classification using NLP and Machine Learning

## 📘 Project Overview

This repository contains a business analytics project that focuses on evaluating and predicting the **clarity of software requirements** (issues) using **Natural Language Processing (NLP)** and **Machine Learning (ML)** techniques. The dataset comprises GitHub issues extracted from public repositories such as **Facebook**, **Stripe**, and **PayPal**, and is used to identify whether each issue is written in a *clear* or *unclear* manner.

## 🎯 Objective

To develop a predictive classification model that automatically labels GitHub issues as either **"clear"** or **"unclear"** based on the issue body text. This will assist teams (e.g., Flutterwave or similar tech companies) in early identification of vague software requirements, improving communication, reducing implementation delays, and enhancing overall software development efficiency.

---

## 📁 Repository Contents

| File/Folder                    | Description |
|-------------------------------|-------------|
| `Business_Analytics_Model.ipynb` | Main notebook for model development, training, and evaluation (Milestone 2). |
| `Capstone_Analysis.ipynb`  | Notebook from Milestone 1 with data exploration, cleaning, and preprocessing. |
| `README.md`                   | This file – overview of the project and instructions. |
| `requirements_data.csv`                       | The processed dataset. |

---

## 🔧 Key Steps in `Business_Analytics_Model.ipynb`

1. **Data Preparation**
   - Merged GitHub issues from multiple repositories.
   - Applied preprocessing steps (text cleaning, filtering).
   - Created `clarity_score` and derived binary label: `'clear'` or `'unclear'`.

2. **Feature Engineering**
   - Applied **TF-IDF Vectorization** on issue body text.
   - Generated embeddings using **BERT** for comparison.

3. **Class Imbalance Handling**
   - Used **SMOTE** and **class_weight** strategies to address class imbalance.

4. **Modeling Techniques**
   - Compared multiple models:
     - Logistic Regression
     - Random Forest
     - Naive Bayes
     - XGBoost
     - Logistic Regression with BERT embeddings

5. **Evaluation**
   - Evaluated using: **Accuracy**, **Precision**, **Recall**, **F1-Score**, and **Confusion Matrix**.
   - Focused on improving performance on **unclear** issues.

---

## 🧠 Final Recommendation

After testing all models, **XGBoost with SMOTE** was selected as the best performer.  
This model provided the **best balance between precision and recall for the 'unclear' class**, which is crucial for our goal of identifying vague or poorly defined software requirements. It outperformed others in recognizing the minority class, making it the most suitable for real-world deployment where early detection of unclear issues is essential.

---

## 📝 Conclusion

This project demonstrates the power of combining NLP techniques with structured ML models to automate requirement clarity assessment. Future improvements could include:

- Exploring deep learning models like BERT + XGBoost or LSTM.
- Fine-tuning hyperparameters using automated search.
  
---
