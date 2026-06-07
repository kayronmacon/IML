# Guided Lab 4.1 — Model Evaluation and Tuning

**Course 02 – Introduction to Machine Learning for Cybersecurity**

**Module 04: Model Evaluation and Tuning**

## 🎯 Lab Goal

In this guided lab, students will evaluate the performance of supervised machine learning models using common classification metrics and model evaluation techniques.

Students will:

- Train a machine learning classification model
- Generate predictions
- Interpret confusion matrices
- Calculate evaluation metrics
- Explore cross-validation techniques
- Understand how model evaluation supports cybersecurity and fraud detection systems

## 💡 Important Lab Note

A model with high accuracy may still perform poorly on fraud detection tasks if fraudulent transactions are rare.

This lab focuses on understanding:

- Precision
- Recall
- False positives
- False negatives
- Model reliability

in cybersecurity and fraud detection systems.

## 📁 Dataset

For this lab, we will use the:

✅ **Credit Card Fraud Detection Dataset** (`creditcard.csv`)

### 📊 Dataset Information

| Column | Description |
| --- | --- |
| V1–V28 | Anonymized transaction features |
| Time | Transaction time |
| Amount | Transaction amount |
| Class | Target label (0 = Normal, 1 = Fraud) |

> The large `creditcard.csv` lives in the gitignored central `datasets/` folder. This lab's notebook loads it via `../../../datasets/creditcard.csv`.

---

## 🛠 Guided Lab Activities

### Part 1 — Load and Explore the Dataset

Students will:

- Load the dataset
- Review class distribution
- Explore dataset structure

### Part 2 — Prepare the Data

Students will:

- Define features and labels
- Split training and testing data
- Scale features if needed

### Part 3 — Train a Classification Model

Students will:

- Train a supervised learning model
- Generate predictions

**Example Models:**

- Logistic Regression
- Decision Tree
- Random Forest

### Part 4 — Evaluate Model Performance

Students will:

- Calculate accuracy
- Generate confusion matrices
- Calculate precision, recall, and F1 score
- Interpret model performance

### Part 5 — ROC Curves and AUC-ROC

Students will:

- Generate ROC curves
- Interpret AUC-ROC values
- Compare model effectiveness

### Part 6 — Cross-Validation

Students will:

- Apply K-Fold Cross-Validation
- Compare cross-validation results
- Understand model generalization

### Part 7 — Introductory Hyperparameter Tuning

Students will:

- Adjust basic model settings
- Compare performance changes
- Observe how tuning affects results

---

## 📦 Submission Requirements

Submit:

- [ ] Completed Jupyter Notebook (`.ipynb`)
- [ ] All code cells executed with outputs visible
- [ ] Evaluation metrics and visualizations included
- [ ] Written interpretation of results
