# Assignment Lab 4.2 — Model Evaluation, Cross-Validation, and Hyperparameter Tuning

**Course 02 – Introduction to Machine Learning for Cybersecurity**

**Module 04: Model Evaluation and Tuning**

## 🎯 Lab Goal

In this assignment, you will evaluate and improve the performance of a machine learning classification model using the Credit Card Fraud Detection dataset.

You will:

- Train and evaluate machine learning models
- Interpret classification metrics
- Analyze confusion matrices
- Apply cross-validation
- Experiment with hyperparameter tuning
- Compare model performance

This assignment builds on the concepts introduced in Guided Lab 4.1.

## 💡 Summary

- Accuracy alone is not enough for imbalanced datasets
- Pay close attention to precision and recall
- False negatives are especially important in fraud detection
- Cross-validation helps test model reliability
- Hyperparameter tuning can improve model performance and stability

## 📌 Important Notes

- Remember to update the dataset path to your local file location
- Use comments in your notebook to explain your workflow
- Focus on interpreting evaluation metrics, not only generating them
- Ensure all graphs and outputs display correctly before submission

## 📁 Dataset

Use the provided dataset:

✅ `creditcard.csv`

### Dataset Description

- `Class = 0` → Normal transaction
- `Class = 1` → Fraudulent transaction

This dataset is highly imbalanced, making it useful for understanding why metrics such as precision, recall, and F1 score are important.

> The large `creditcard.csv` lives in the gitignored central `datasets/` folder. This lab's notebook loads it via `../../../datasets/creditcard.csv`.

---

## 🛠 Assignment Tasks

### Part 1 — Load and Explore the Dataset

**Tasks:**

- Load the dataset into Python
- Display the first few rows
- Review dataset shape and column names
- Check for missing values
- Review class distribution

**Questions to Consider:**

- Is the dataset balanced or imbalanced?
- Why might imbalance affect model evaluation?

### Part 2 — Prepare the Data

**Tasks:**

- Define features (`X`) and target (`y`)
- Split the dataset into training and testing sets
- Scale numerical features using `StandardScaler`

### Part 3 — Train a Classification Model

**Tasks:**

- Train at least one supervised learning model

**Recommended Models:**

- Logistic Regression
- Decision Tree
- Random Forest

**Questions to Consider:**

- Why is the model appropriate for this dataset?
- What challenges may occur with fraud detection data?

### Part 4 — Evaluate Model Performance

**Tasks:**

- Generate predictions
- Calculate:
  - Accuracy
  - Precision
  - Recall
  - F1 Score
- Generate a classification report
- Create and interpret a confusion matrix

**Questions to Consider:**

- Did the model detect fraudulent transactions effectively?
- Were there many false positives or false negatives?

### Part 5 — ROC Curve and AUC-ROC

**Tasks:**

- Generate an ROC curve
- Calculate the AUC-ROC score
- Interpret model performance

**Questions to Consider:**

- Did the ROC curve suggest strong model performance?
- Why is AUC-ROC useful for fraud detection?

### Part 6 — Apply Cross-Validation

**Tasks:**

- Use K-Fold Cross-Validation
- Calculate average cross-validation scores
- Compare validation performance to testing performance

**Questions to Consider:**

- Did cross-validation produce stable results?
- Why is cross-validation important?

### Part 7 — Hyperparameter Tuning

**Tasks:**

- Experiment with at least one hyperparameter

**Example:**

- For Logistic Regression: adjust `C`
- For Decision Trees: adjust `max_depth`
- For Random Forest: adjust number of trees

**Suggested Tool:**

- `GridSearchCV`

**Questions to Consider:**

- Did tuning improve performance?
- Which parameters produced the best results?

### Part 8 — Final Comparison and Reflection

**Tasks:**

- Compare the original and tuned models
- Summarize evaluation results
- Reflect on strengths and weaknesses of the model

---

## 🧠 Interpretation Questions

Answer the following questions in complete sentences:

1. What was the model accuracy?
2. Why might accuracy alone be misleading for this dataset?
3. What do precision and recall tell us in fraud detection?
4. What does the confusion matrix show about the model's predictions?
5. Did cross-validation improve confidence in the model's reliability?
6. Did hyperparameter tuning improve model performance?
7. How can evaluation metrics support cybersecurity and fraud detection systems?
8. What are some limitations of machine learning models in cybersecurity environments?

---

## 📦 Submission Requirements

Submit:

- [ ] Completed Jupyter Notebook (`.ipynb`)
- [ ] All notebook cells executed with outputs visible
- [ ] Confusion matrix visualization included
- [ ] ROC curve visualization included
- [ ] Cross-validation results included
- [ ] Hyperparameter tuning results included
- [ ] Written responses to interpretation questions
