# Assignment M08-L01: Intro to Machine Learning — Classification with Python

## Overview

In this assignment, you will apply the machine learning concepts introduced in Module 8 by completing a hands-on classification task using a simplified cybersecurity dataset. You will train a **logistic regression model** to predict whether an alert should be triggered based on user login behavior and location metadata.

This activity is designed to help you practice the full **ML workflow** using `scikit-learn`, from data preprocessing and model training to performance evaluation.

## Learning Objectives

By completing this assignment, you will:

- Understand how to structure a dataset for supervised learning
- Use `scikit-learn` to train and evaluate a logistic regression model
- Interpret accuracy, precision, and recall in a classification context
- Apply Python and ML skills to a cybersecurity dataset

## Steps to Complete

1. **Download and Open the Notebook**
   Download the Starter Notebook and open it in JupyterLab, Jupyter Notebook, or Google Colab.

2. **Explore the Dataset**
   - Load the `sample_cybersecurity_classification_data.csv` file
   - Review its structure and contents

3. **Preprocess the Data**
   - Define features (`X`) and target (`y`)
   - Split the dataset into training and test sets

4. **Train the Model**
   - Use `LogisticRegression` from `scikit-learn`
   - Fit the model to your training data

5. **Evaluate the Model**
   - Make predictions on the test set
   - Print and interpret:
     - Accuracy
     - Precision
     - Recall
     - Classification report

6. **Reflect** (add a markdown cell at the end)
   Write 3–4 sentences responding to the following:
   - How well did your model perform?
   - What do precision and recall mean in a cybersecurity context?
   - How might this model help in a real-world scenario?

7. **Submit Your Work**
   - Save your final `.ipynb` file with your name in the filename (e.g., `ml_assignment_yourname.ipynb`)
   - Upload your completed notebook to Canvas

## What to Submit

- Completed Jupyter Notebook (`.ipynb`)
- Your written reflection in the last cell of the notebook

## Grading Criteria

| Criteria | Points |
| --- | ---: |
| Correct use of ML workflow steps | 20 |
| Model evaluation and metrics | 20 |
| Code readability and comments | 10 |
| Written reflection | 10 |
| **Total** | **60** |
