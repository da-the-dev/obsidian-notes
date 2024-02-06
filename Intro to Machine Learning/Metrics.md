After we have trained our model we would like to know how well this model performs. We measure that with different metrics.
# Accuracy
Accuracy gives an overall idea of how often the classifier is correct.
$$
Acc = 1 - \dfrac{\text{\# of missclassified examples}}{\text{\# of samples}}
$$
If the classes are not balanced, accuracy is not a good metric to use to measure performance of machine learning models.
# Precision
Precision focuses on the relevant instances among the retrieved instances. It is concerned with the accuracy of the positive predictions. 
$$
\text{Precision} = \dfrac{\text{True positives}}{\text{True postives + False positives}}
$$
Precision is a good metric when the cost of false positives is high.
# Recall
Recall measures the ability of the classifier to find all the relevant cases within a dataset.
$$
\text{Recall} = \dfrac{\text{True positives}}{\text{True postives + False negatives}}
$$
Recall is important when the cost of false negatives is high. For example, in medical diagnosis, it's crucial to detect all cases of a disease, even if it means classifying some healthy individuals as diseased.
# F1 score
The F1-score is the harmonic mean of precision and recall. It provides a balance between precision and recall, especially when classes are imbalanced.
$$
\text{F1 score} = 2 \times  \dfrac{\text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}}
$$
# Additional info
https://www.youtube.com/watch?v=4jRBRDbJemM
[[Confusion matrix]]