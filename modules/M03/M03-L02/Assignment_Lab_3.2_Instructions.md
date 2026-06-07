# Assignment Lab 3.2 — Unsupervised Learning for Fraud and Anomaly Detection

**Course 02 – Introduction to Machine Learning for Cybersecurity**

## 🎯 Lab Goal

In this assignment, you will apply unsupervised learning techniques to analyze real-world transaction data and identify possible anomalies using clustering methods.

You will use machine learning techniques to:

- Discover hidden patterns in transaction behavior
- Identify unusual or isolated records
- Visualize clusters and anomalies
- Interpret how unsupervised learning supports cybersecurity and fraud detection

This assignment builds on the clustering and dimensionality reduction concepts introduced in Guided Lab 3.1.

## 💡 Tips for Success

- Compare K-Means and DBSCAN results carefully
- Observe how DBSCAN identifies outliers differently from K-Means
- Pay attention to the class imbalance in the dataset
- Use PCA visualizations to better understand the clustering behavior
- Think about how anomaly detection supports real-world cybersecurity systems

## 📌 Important Notes

- Remember to update the dataset path to your local file location
- Use comments in your notebook to explain your workflow
- Focus on interpreting patterns and anomalies, not only model outputs
- Ensure all visualizations display correctly before submission

## 📁 Dataset

Use the provided dataset:

✅ `creditcard.csv`

### Dataset Description

This dataset contains anonymized credit card transaction records.

- `Class = 0` → Normal transaction
- `Class = 1` → Fraudulent transaction

For this lab:

⚠️ Do **NOT** use the `Class` column during clustering because unsupervised learning works without labels.

You may use the `Class` column later only for comparison and interpretation.

## 🛠️ Assignment Tasks

### Part 1 — Load and Explore the Dataset

**Tasks:**

- Load the dataset into Python
- Display the first few rows
- Review dataset shape and feature names
- Check for missing values
- Review summary statistics

**Questions to Consider:**

- How many features are included?
- Is the dataset balanced or imbalanced?

### Part 2 — Prepare the Data

**Tasks:**

- Remove the `Class` column from the feature set
- Scale the data using `StandardScaler`

**Example:**

You may use:

```python
X = df.drop("Class", axis=1)
```

### Part 3 — Apply K-Means Clustering

**Tasks:**

- Train a K-Means clustering model
- Create transaction clusters
- Display the number of records in each cluster

**Questions to Consider:**

- Which clusters appear larger or smaller?
- Do some clusters appear more unusual than others?

### Part 4 — Apply DBSCAN for Anomaly Detection

**Tasks:**

- Train a DBSCAN clustering model
- Identify records labeled as `-1`
- Interpret these records as possible anomalies

**Recommended Parameters:**

```python
dbscan = DBSCAN(eps=2.5, min_samples=5)
```

**Questions to Consider:**

- How many anomalies were detected?
- Why might these transactions appear unusual?

### Part 5 — Apply PCA for Visualization

**Tasks:**

- Reduce the dataset to two PCA components
- Create a scatter plot showing K-Means clusters
- Create a second scatter plot showing DBSCAN anomalies

**Questions to Consider:**

- Did PCA help reveal hidden patterns?
- Were anomalies visually separated from normal clusters?

### Part 6 — Compare Results with Fraud Labels

**Tasks:**

- Compare detected anomalies with the `Class` column
- Review whether some detected anomalies overlap with fraudulent transactions

**Important Note:**

The clustering models should not use the fraud labels during training. This comparison is only for interpretation after clustering is completed.

### Part 7 — Interpretation and Reflection

Answer the following questions in your notebook:

1. What patterns did you observe in the clusters?
2. Did DBSCAN identify unusual or isolated transactions?
3. How did PCA help visualize the dataset?
4. Were any detected anomalies associated with fraudulent transactions?
5. How can unsupervised learning support fraud detection and cybersecurity monitoring?
6. What are some limitations of unsupervised learning for anomaly detection?

## 📊 Example Cybersecurity and Fraud Interpretation

Suppose DBSCAN identifies several isolated transactions that:

- Occur at unusual times
- Have abnormal transaction patterns
- Differ significantly from most records

These transactions may represent:

- Fraudulent activity
- Stolen card usage
- Automated transaction attacks
- High-risk anomalies

Security analysts could investigate these anomalies further even if the transactions were not originally labeled as fraud.

## 📦 Submission Requirements

Submit:

✅ Completed Jupyter Notebook (`.ipynb`)

- ✅ All notebook cells executed with outputs visible
- ✅ At least two visualizations included
- ✅ Written responses to interpretation questions
