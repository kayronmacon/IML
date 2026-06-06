# Supervised Learning — In Depth

> A deep dive into supervised learning, expanding on the core notes.
> Source basis: [Google — Intro to ML: Supervised Learning](https://developers.google.com/machine-learning/intro-to-ml/supervised)
> See also: [[machine-learning]]

## What "Supervised" Really Means

A supervised model learns by seeing **lots of examples that already include the correct answer**. From these examples it discovers the connections (patterns) between the input data and the answers, so it can predict the answer for **new data it has never seen**.

It is called "supervised" because a human acts as the supervisor: you provide the data **labeled** with the known correct results, and the model is effectively graded against those labels while it learns.

### Key vocabulary

| Term | Meaning |
| --- | --- |
| **Feature** | An input variable the model uses to make a prediction (e.g., temperature, humidity). |
| **Label** | The correct answer the model is trying to predict (e.g., inches of rain). |
| **Example** | A single row of data — one set of features, often paired with its label. |
| **Labeled example** | An example that includes the label. Used for **training**. |
| **Unlabeled example** | An example with features but no label. The model predicts the label for these. |
| **Model** | The function the training process produces, mapping features → prediction. |

---

## How Training Works (the loop)

Supervised learning is fundamentally a feedback loop:

1. **Predict** — the model makes a prediction from the input features.
2. **Compare** — the prediction is compared to the true label using a **loss** function (a measure of how wrong it was).
3. **Adjust** — the model updates its internal parameters (weights) to reduce that loss.
4. **Repeat** — over many examples and many passes, the loss shrinks and predictions improve.

> The goal is **generalization**: doing well on *new* data, not just memorizing the training data.

### Train / test split

To check whether a model actually generalizes, you split your labeled data:

- **Training set** — used to fit the model.
- **Test set** — held back and used only to evaluate performance on unseen data.
- (Often a **validation set** too, for tuning settings before the final test.)

---

## The Two Main Use Cases

Supervised learning splits into two of the most common tasks: **regression** and **classification**. The difference is simply *what kind of answer* you're predicting.

### Regression — predicting a number

A **regression** model predicts a **continuous numeric value**.

- *Example:* a weather model predicting the amount of rain in inches or millimeters.
- *Other examples:* predicting a house price, a person's age from a photo, or tomorrow's stock value.

The simplest and most common starting technique is **linear regression**, which fits a straight-line relationship between the features and the numeric target.

### Classification — predicting a category

A **classification** model predicts the **likelihood that something belongs to a category**.

Classification models come in two groups:

| Type | Meaning | Example |
| --- | --- | --- |
| **Binary classification** | Exactly **2** possible classes | spam vs. not spam |
| **Multiclass classification** | **More than 2** possible classes | classifying an email as *primary*, *social*, or *promotions* |

> Under the hood, a classifier usually outputs a **probability** (e.g., 0.92 = "spam"). A **threshold** (often 0.5) turns that probability into a final class decision.

### Regression vs. Classification at a glance

| | Regression | Classification |
| --- | --- | --- |
| Predicts | A numeric value | A category / class |
| Output | Continuous (e.g., 3.7 in) | Discrete (e.g., "cat") |
| Example | How much rain? | Will it rain — yes or no? |

---

## Measuring How Good a Model Is

You can't improve what you don't measure. Different tasks use different metrics:

**Regression metrics** (how far off the numbers are):
- **MAE** (Mean Absolute Error) — average size of the errors.
- **MSE / RMSE** (Mean Squared / Root Mean Squared Error) — punishes large errors more heavily.

**Classification metrics** (how often the category is right):
- **Accuracy** — fraction of predictions that are correct.
- **Precision** — of the items predicted positive, how many truly were.
- **Recall** — of the truly positive items, how many were caught.
- **F1 score** — balances precision and recall.

---

## Common Pitfalls

- **Overfitting** — the model memorizes the training data (including its noise) and fails on new data. Signs: great training score, poor test score.
- **Underfitting** — the model is too simple to capture the real pattern; it does poorly on *both* training and test data.
- **Bad / biased labels** — supervised learning is only as good as its labeled answers. Wrong or skewed labels teach the model the wrong thing.
- **Data leakage** — accidentally letting answer-related information into the features, giving falsely high scores.

---

## Where It Fits Among ML Systems

Supervised learning is one of several categories of ML systems, distinguished by **how the model learns**:

- **Supervised learning** — learns from labeled data (this note).
- **Unsupervised learning** — finds patterns/clusters in *unlabeled* data.
- **Reinforcement learning** — learns from rewards and penalties.
- **Generative AI** — produces new data similar to its training data.

> Notably, generative models are often **pre-trained unsupervised**, then refined further with **supervised** (or reinforcement) learning on task-specific data — so supervised learning shows up even inside modern generative AI.

---

See also: [[machine-learning]] · [[M02-supervised-learning]] · [[M01-intro-to-ml-for-cybersecurity]]
