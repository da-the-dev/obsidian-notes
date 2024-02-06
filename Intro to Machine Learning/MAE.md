Full name: Mean Absolute Error

MAE is calculated by taking the average of the absolute differences between the predicted values and the actual values.

Pros & Cons:
- It measures the average magnitude of errors in a set of predictions, without considering their direction (positive or negative).
- MAE is less sensitive to outliers compared to [[MSE]] because it doesn't square the errors.
- The derivative of MAE is the same everywhere
$$
MAE = \dfrac{1}{n}\sum^{n}_{i=1}|y_{i}-\hat{y}_{i}|
$$
^MAE