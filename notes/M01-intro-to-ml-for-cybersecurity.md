# M01 — Intro to Machine Learning for Cybersecurity (Mini Project)

> Module 1 was a **preview** of the ML workflow using a labeled login dataset.
> Everything here gets expanded in M02. Source: `modules/M01-miniproject/`.

## The big idea
Machine learning can analyze patterns in login activity and **automatically flag suspicious behavior**, so security analysts review a small high-risk subset instead of triaging thousands of routine logins.

## The dataset (`cybersecurity_login_dataset.csv`)
The same dataset is reused throughout M01 and M02.

| Column | Type | Meaning |
| --- | --- | --- |
| `login_attempts` | feature | total login attempts in a session |
| `failed_logins` | feature | failed attempts in that session |
| `unusual_login_hour` | feature (0/1) | 1 = odd hour (late night / early morning) |
| `new_ip_address` | feature (0/1) | 1 = unfamiliar IP |
| `suspicious` | **label** | 1 = suspicious, 0 = normal |

- **Features (X)** = inputs the model learns from.
- **Label (y)** = the value being predicted (`suspicious`).

## The 6-step supervised-learning workflow (memorize this)
1. **Load & explore** the data (`pd.read_csv`, `df.head()`, `df.info()`).
2. **Identify features and label** — split into `X` and `y`.
3. **Train/test split** — `train_test_split(..., test_size=0.2, random_state=42)`. Train on one part, evaluate on data the model has never seen.
4. **Train a model** — `LogisticRegression().fit(X_train, y_train)`.
5. **Predict** — `model.predict(X_test)`.
6. **Evaluate** — accuracy + confusion matrix, then interpret.

## Key concepts introduced
- **Why a train/test split?** Testing on data the model trained on would inflate the score. The test set estimates real-world performance.
- **Accuracy** = fraction of predictions that are correct. A useful headline number but *not* the whole story (see confusion matrix).
- **Confusion matrix** lays out correct vs. incorrect predictions per class — the foundation for everything in M02.

## Result we actually got
- Accuracy ≈ **0.84 (84%)**, confusion matrix `[[38, 12], [7, 63]]`.
- Interpretation: `failed_logins` is the strongest single signal (brute-force / credential stuffing), but **compounding signals** matter most — many failed logins + odd hour + new IP together is far more suspicious than any one feature alone.

## Takeaway
This is the *baseline mental model* for the whole course: data → split → train → predict → evaluate → interpret. M02 makes each step more rigorous (stratified splits, multiple models, precision/recall).

See also: [[M02-supervised-learning]]
