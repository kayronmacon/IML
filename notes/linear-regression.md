# Linear Regression

**Linear regression** is a statistical technique used to find the relationship between variables. In an ML context, linear regression finds the relationship between **features** and a **label**.

We can take features, plot them on a graph, and draw a *"best fit line."*

## The model

A linear regression model with a single feature is:

$$y' = b + w_1 x_1$$

where:

- $y'$ — the predicted label (the output).
- $b$ — the **bias** of the model. Bias is the same concept as the y-intercept in the algebraic equation for a line. In ML, bias is sometimes referred to as $w_0$. Bias is a parameter of the model and is calculated during training.
- $w_1$ — the **weight** of feature $x_1$. Like bias, weight is a parameter calculated during training.
- $x_1$ — a feature (the input).

## Multiple features

A model that relies on multiple features extends naturally:

$$y' = b + w_1 x_1 + w_2 x_2 + \dots + w_n x_n$$
