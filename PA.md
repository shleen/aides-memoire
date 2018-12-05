# Predictive Modeling I

## Linear Regression
Used to predict a **continuous** target variable. For example- salary, age, distance between two points, etc. Are also known as **estimators** or **regression models**. A linear regression is, essentially, the best fit linear equation that graphs the output of the target variable with respect to the input variable(s).

Regression models exhibit **supervised learning**, the facet of machine learning where models learn an algorithm by training with a set of data that forms the ground truth.

```
y = b₀ + b₁x₁ + b₂x₂ + ... + b𝑛x𝑛
```

### R-squared Value
A metric commonly used with linear regressions to determine the accuracy of the regression model. The r-squared value lies between 0 & 1, where an r-squared value of 0 indicates a lack of correlation whereas an r-squared value of 1 indicates a completely dependent relation.

Any r-squared value **.7 & above** is indicative of a **strong relationship**.


## Model Assessment
We can build models that attempt to predict certain target variables. Naturally, we want to have a set of features (that have been tried & tested) that can give us an accurate representation of our model's accuracy.

- **Predictive Accuracy**- A quantitative assessment that indicates a model's predictive ability.
- **Speed**- In model building as well as in making predictions.
- **Robustness**- Against missing/ noisy/ erroneous data.
- **Scalability**- How does the model handle large amounts of data?
- **Interpretability**- In terms of the ease of understanding of the model.

In this module, we focus on assessing a model through its predictive accuracy. To accomplish this, we make use of 2 specific **assessment methodologies**.

1. **Simple Split**- Split the data into 2 sets (a training set & a testing set). The split is typically a **70/30** split.
1. **k-fold Cross Validation**- Split the data into k (mutually exclusive) subsets. Conduct the training k times, rotating the subset to be used as the testing set. Then, attain predictive accuracy as an aggregation of the k sets of test results.
