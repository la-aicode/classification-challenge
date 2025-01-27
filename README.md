# Spam Detection Project

## Overview
This project focuses on building machine learning models to detect spam emails based on various word and character frequency features. Two models were trained and evaluated for this task: **Logistic Regression** and **Random Forest Classifier**. The objective is to compare their performance and determine the most suitable model for different use cases.

---

## Dataset
The dataset contains 4,601 rows and 58 columns. Each row represents an email, and the columns include:
- **Features**: Word and character frequency metrics (e.g., `word_freq_make`, `char_freq_!`).
- **Target (spam)**: A binary variable where:
  - `1` indicates the email is spam.
  - `0` indicates the email is not spam.

---

## Models Trained
### 1. Logistic Regression
- **Pros**:
  - Simple and interpretable.
  - Computationally efficient.
  - Suitable for real-time systems.
- **Cons**:
  - Assumes a linear relationship between features and the target variable.
  - Less effective in capturing complex patterns.

### 2. Random Forest Classifier
- **Pros**:
  - Handles non-linear relationships.
  - Robust to noise and irrelevant features.
  - Provides feature importance insights.
- **Cons**:
  - Computationally intensive.
  - Less interpretable compared to Logistic Regression.

---

## Results
### Accuracy Scores:
- **Random Forest Classifier**: 93.92%
- **Logistic Regression**: 92.94%

### Key Observations:
- Random Forest Classifier outperforms Logistic Regression in terms of accuracy due to its ability to model complex, non-linear patterns.
- Logistic Regression, while slightly less accurate, is faster and easier to interpret, making it a better choice for medium-sized companies with limited computational resources or a need for transparency.

---

## Technical Steps
1. **Data Loading**:
   - The dataset was loaded and analyzed for label balance.
2. **Data Splitting**:
   - The data was split into training and testing sets using an 80-20 split.
3. **Feature Scaling**:
   - A `StandardScaler` was used to normalize the features for improved model performance.
4. **Model Training**:
   - Logistic Regression and Random Forest Classifier models were trained on the scaled training data.
5. **Evaluation**:
   - Models were evaluated using accuracy scores on the test set.
6. **Prediction Output**:
   - Predictions for the test set were saved to a CSV file for further analysis.

---

## Conclusion
- **Best Performing Model**: Random Forest Classifier (Higher accuracy).
- **Recommendation**: 
  - For tasks where **accuracy and robustness** are critical: Use **Random Forest Classifier**.
  - For tasks where **speed and simplicity** are prioritized: Use **Logistic Regression**.


