# datasets/

Central store for **oversized datasets** that exceed GitHub's 100 MB file limit.

Everything in this folder is **gitignored** (except this README), so the files
live **locally only** and are not pushed. Notebooks reference them with a
relative path back to this folder, e.g. from a lab in `modules/M03/M03-L02/`:

```python
df = pd.read_csv("../../../datasets/creditcard.csv")
```

## Required files (download locally)

| File | Used by | Source |
| --- | --- | --- |
| `creditcard.csv` (~144 MB) | M03-L02 — Lab 3.2 Fraud & Anomaly Detection | [Kaggle: Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) |

> Small datasets (e.g. `cybersecurity_login_dataset.csv`) stay alongside their
> labs and are committed normally — only large files belong here.
