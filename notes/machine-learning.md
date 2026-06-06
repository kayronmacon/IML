# Machine Learning — Core Concepts

> Foundational notes on what ML is and the main types of ML systems.
> Source: [Google — Intro to ML: Supervised Learning](https://developers.google.com/machine-learning/intro-to-ml/supervised)

## What is Machine Learning?

Machine learning is the practice of **training a piece of software, called a model, to make useful predictions or generate content from data**.

- Training a model takes enormous amounts of data.
- A common starting technique is **linear regression**.

## Types of ML Systems

ML systems fall into one or more of the following categories, based on **how they learn** to make predictions or generate content:

- Supervised learning
- Unsupervised learning
- Reinforcement learning
- Generative AI

---

## Supervised Learning

Supervised models can make predictions after seeing **lots of data with the correct answers**, discovering the connections between the elements in the data that produce those answers.

These systems are "supervised" in the sense that **a human gives the model data with the known correct results**.

The two most common use cases are **regression** and **classification**.

### Regression

A regression model predicts a **numeric value**.

- *Example:* a weather model that predicts the amount of rain, in inches or millimeters.

### Classification

A classification model predicts the **likelihood that something belongs to a category**.

Classification models are divided into two groups:

| Type | Meaning |
| --- | --- |
| **Binary classification** | 2 possible classes |
| **Multiclass classification** | multiple possible classes |

---

## Unsupervised Learning

An unsupervised model aims to **identify meaningful patterns in a dataset** without being given correct answers. Many such models rely on **clustering** to organize similar data into groups.

**How it differs from classification:** the categories aren't defined by you. The model creates the clusters on its own, and you then use your own expertise to **interpret and name them**.

---

## Reinforcement Learning

A reinforcement learning model makes predictions by **getting rewards or penalties** based on actions it performs within an environment.

- The system generates a **policy** that defines the best strategy for earning the most rewards.
- *Common use:* training robots.

---

## Generative AI

**How does it work?** At a high level, generative models learn patterns in data with the goal of **producing new but similar data**.

Analogies for how generative models learn:

- **Comedians** who learn to imitate others by observing people's behaviors and speaking styles.
- **Artists** who learn to paint in a particular style by studying many paintings in that style.
- **Cover bands** that learn to sound like a specific group by listening to lots of their music.

**How they're trained:**

1. Initially trained with an **unsupervised** approach, where the model learns to mimic the data it's trained on.
2. Sometimes trained further using **supervised or reinforcement learning** on task-specific data — for example, summarizing an article or editing a photo.

Generative AI is evolving quickly, with new use cases constantly being discovered. For example, generative models help businesses refine ecommerce product images by automatically removing distracting backgrounds or improving the quality of low-resolution images.

---

See also: [[M02-supervised-learning]] · [[M01-intro-to-ml-for-cybersecurity]]
