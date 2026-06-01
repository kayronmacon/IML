# M02 — Supervised Learning with Scikit-learn

> Module 2 formalizes the workflow from [[M01-intro-to-ml-for-cybersecurity]].
> Guided Lab 2.1 (`modules/M02/M02-L01/`) walks the workflow step by step;
> Assignment 2.2 (`modules/M02/M02-L02/`) does it independently and compares models.

## What supervised learning is
You train on **labeled** examples (inputs paired with the correct answer) so the model learns a mapping from features → label, then apply it to new data. Two flavors:
- **Classification** — predict a category (e.g., `suspicious` = 0/1). ← what these labs do.
- **Regression** — predict a continuous number (e.g., a price). Covered conceptually via the Google ML crash course reading.

Knowing **regression vs. classification** is a stated focus of the module.

## Models seen this module
| Model | Notes |
| --- | --- |
| **Logistic Regression** | Linear, **interpretable** (coefficients show feature influence). Good realistic baseline for binary classification. |
| **Decision Tree** | Splits data on feature thresholds; can overfit easily. |
| **Random Forest** | Many trees averaged; usually strong, gives feature importances. |
| **Support Vector Machine (SVM)** | Finds the max-margin boundary between classes. |

## Evaluation — beyond accuracy
The **confusion matrix** (sklearn layout, rows = actual, cols = predicted):

```
              Predicted 0   Predicted 1
Actual 0   [   TN            FP        ]
Actual 1   [   FN            TP        ]
```

- **TP / TN** = correct. **FP** = false alarm. **FN** = missed detection.
- **Precision** = TP / (TP + FP) — "when it flags, how often is it right?"
- **Recall** = TP / (TP + FN) — "of all real threats, how many did it catch?"
- **In security, false negatives (missed threats) are the costliest error**, so recall on the suspicious class often matters more than raw accuracy.

## Results we actually got (same dataset, stratified split)
- **Logistic Regression:** accuracy ≈ **0.88**, confusion matrix `[[43, 4], [10, 63]]`.
  - Only 4 false alarms, but **10 missed suspicious logins** (false negatives) — the number to worry about.
  - Coefficients ranked: `unusual_login_hour` (~2.82) > `new_ip_address` (~2.28) > `login_attempts` (~0.32) > `failed_logins` (~0.16).
- **Model comparison:** Decision Tree & Random Forest = **100%**, SVM ≈ 0.867.

## ⚠️ Most important lesson: 100% accuracy is a red flag, not a trophy
The tree models scoring a perfect 100% almost certainly means the dataset is **small, synthetic, and easily separable** — or that there's data leakage / overfitting. On real-world data you'd expect those models to drop. **Always be suspicious of "perfect" results** and prefer the more honest, interpretable estimate (logistic regression here).

## Practical gotchas
- **`stratify=y`** in `train_test_split` keeps the class balance the same in train and test sets — important when classes are uneven. (M01 omitted it; M02 added it.)
- **`LogisticRegression(max_iter=1000)`** avoids convergence warnings on some data.
- Different models tell **complementary stories**: logistic regression weighted `unusual_login_hour` highest, while Random Forest ranked `login_attempts` most important — look across models, don't trust one ranking blindly.

## Why ML helps cybersecurity monitoring
Learns detection patterns directly from labeled history, scores new logins in real time, prioritizes the riskiest for analyst review, reduces alert fatigue, and adapts as new attack examples arrive — with the caveats above (validate carefully, weight false negatives).

## Resources (from `modules/M02/resources/resources.md`)
- scikit-learn Supervised Learning guide
- Google ML Crash Course — Linear Regression
- StatQuest: Support Vector Machines Part 1
