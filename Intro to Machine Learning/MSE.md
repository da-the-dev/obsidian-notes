Full name: Mean Squared Error

MSE is calculated by taking the average of the squared differences between the predicted values and the actual values.

Pros & Cons
- It penalizes larger errors more than smaller ones due to squaring the errors.
- MSE is very sensitive to outliers compared to [[MAE]] because larger errors contribute more significantly to the overall error due to squaring.

$$
MSE = \dfrac{1}{n}\sum^{n}_{i=1}(y_{i}-\hat{y}_{i})^{2}
$$
^MSE