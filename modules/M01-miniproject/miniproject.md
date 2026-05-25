# Mini Project: Machine Learning for Cybersecurity

## Overview

This optional mini project introduces a simple machine learning workflow using a labeled cybersecurity dataset. The goal is to help students understand how machine learning models can support cybersecurity monitoring and threat detection.

In this project, you will apply a basic machine learning model to analyze login activity data and identify potentially suspicious behavior.

This activity provides a preview of machine learning workflows and prepares you for **Course 02 – Machine Learning**, where these concepts will be explored in greater depth.

## Learning Objectives

By completing this mini project, you will be able to:

- Identify features and labels in a dataset
- Train a basic machine learning model using Python and `scikit-learn`
- Generate predictions using the trained model
- Evaluate model performance using basic metrics
- Interpret how machine learning can support cybersecurity monitoring

## Dataset Description

**File:** `cybersecurity_login_dataset.csv`

This dataset contains simulated login activity records used to detect suspicious login behavior.

### Features

| Feature | Description |
| --- | --- |
| `login_attempts` | Total number of login attempts made during a session |
| `failed_logins` | Number of failed login attempts during that session |
| `unusual_login_hour` | `1` = unusual login time (late night/early morning), `0` = normal |
| `new_ip_address` | `1` = new IP address, `0` = known IP address |

### Label

| Label | Description |
| --- | --- |
| `suspicious` | `1` = suspicious behavior, `0` = normal behavior |

The goal of the machine learning model is to predict whether a login activity should be flagged as suspicious.

## Project Tasks

### Task 1 — Load the Dataset

Load the dataset using the `pandas` library. Explore the dataset by examining:

- The first few rows of data
- The dataset structure
- Feature distributions

```python
import pandas as pd

df = pd.read_csv("cybersecurity_login_dataset.csv")
df.head()
```

### Task 2 — Identify Features and Labels

Separate the dataset into:

**Features (X)** — the variables used by the model to make predictions:
`login_attempts`, `failed_logins`, `unusual_login_hour`, `new_ip_address`

**Label (y)** — the value the model will predict: `suspicious`

```python
X = df[['login_attempts', 'failed_logins', 'unusual_login_hour', 'new_ip_address']]
y = df['suspicious']
```

### Task 3 — Split the Dataset

Divide the dataset into training data and testing data. Training data is used to train the model, while testing data is used to evaluate model performance.

```python
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
```

### Task 4 — Train a Machine Learning Model

Train a basic machine learning model using `scikit-learn`. Suggested model: **Logistic Regression**.

```python
from sklearn.linear_model import LogisticRegression

model = LogisticRegression()
model.fit(X_train, y_train)
```

### Task 5 — Generate Predictions

Use the trained model to predict suspicious login activity in the testing dataset.

```python
predictions = model.predict(X_test)
```

### Task 6 — Evaluate Model Performance

Evaluate the model using performance metrics such as:

- Accuracy
- Confusion Matrix

```python
from sklearn.metrics import accuracy_score, confusion_matrix

accuracy = accuracy_score(y_test, predictions)
cm = confusion_matrix(y_test, predictions)

print("Accuracy:", accuracy)
print("Confusion Matrix:", cm)
```

### Task 7 — Interpret the Results

Write a short explanation answering the following questions:

- How accurate was the model?
- Which features appear to be strong indicators of suspicious login behavior?
- How could a machine learning model like this support a cybersecurity monitoring system?

Example interpretations might include:

- Detecting brute-force login attempts
- Flagging unusual login behavior
- Supporting automated threat detection systems

## Deliverables

Submit the following:

1. Completed Python Notebook
2. Short written explanation (3–5 sentences) describing how machine learning can help detect suspicious login activity

## Key Takeaway

Machine learning models can analyze patterns in login activity data and help security systems automatically detect suspicious behavior. This project introduces the basic workflow used in many real-world security analytics systems.

The concepts practiced in this mini project will be expanded in **Course 02 – Machine Learning**, where you will learn how to build more advanced predictive models and evaluate them using more sophisticated techniques.
