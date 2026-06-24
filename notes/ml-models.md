Linear regression - is a statistical technique used to find the relationship between variables. In an ML
context, linear regression finds the relationship between features and a label.

We can take features, plot them on a graph and draw a "best fit line"

Linear regression model y1 = b + w1x1 where:

y1 is the predicted label- the output

b is the bias of the model. Bias is the same concept as the y-intercept in the algebraic equation for a line.
In ML, bias is sometimes referred to as w0. Bias is a parameter of the model and is calculated during training.

w1 is the weight of the feature. Weight is the same concept as the slope m in the algebraic equation for a line.
Weight is a parameter of the model and is calculated during training.

x1 is a feature-the input

During training, the model calculates the weight and bias that produce the best model

Models with multiple features: a more sophisticated model might rely on multiple features, each having a seperate weight.
For example, a model that relies on five features would be written as follows: y1 + b + w1x1 + w2x2 + w3x3 + w4x4 + w5x5

For example, a model that predicts gas milegale could additionally use features such as the following:

- Engine displacement
- Acceleration
- Number of cylinders
- Horsepower


Linear Regression: Loss

Loss - is a numerical metric that describes how wrong a model's predictions are. Loss measures the distance
between the model's predictions and the actual labels. The goal of training a model is to minimize the loss.

Distance of loss

loss measure the distance between the predicted and actual values. Loss focuses on the distance between the values, not
the direction. 

The two most common methods to remove the sign are the following:
- Take the absolute value of the difference between the actual value and the prediction
- Square the difference between the actual value and the prediction.

Types of loss: In linear regression, there are five main types of loss

L1 loss - The sum of the absolute values of the difference between the predicted values and the actual values E| actual value - predicted value
Mean absolute error (MAE) -  The average of l1 lossess across a set of N examples  1/n E| actual value - predicted value

L2 loss - the sum of the squared difference between the predicted values and the actual values E(actual value - predicted value)^2

Mean squared error (MSE) - The average of L2 losses across a set of N examples - 

Root mean squared error (RMSE) The square root of the mean squared error (MSE)

https://developers.google.com/machine-learning/crash-course/linear-regression/loss

(if claude can fill in the above algorithms that would be tits)


