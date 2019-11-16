---
layout: post
title: Model presentation of supervised learning
---

The purpose of the problem of the problem is to find the relationship between independent variables and dependent variable. Hence, the value of the unknown dependent variable is predicted based on the value of its respective independent variables.

### Model presentation

To discribe the supervised learning problem slightly more formally, given a <strong>traning set</strong>, to learn a function h: X -> Y so h(x) is "good" predictor for the corresponding value of y. This function h is called a <strong>hypothesis</strong>.

[<img src="{{ site.baseurl }}/images/RegressionModel.png" alt="Constructocat by https://github.com/jasoncostello" style="width: 800px;"/>]({{ site.baseurl }}/)

When the target variable that we're trying to predict is continuous, we call the learning problem is a regression learning. When y can take on only a small number of discrete values.

### So what do we need to pay attention to?
<strong>1. Training data set:</strong>   
- Training data set for the supervised learning problem is a data set that is provided with both independent(X) and dependent(Y) variables. In this particular model, I would like to call the independent variables as features and dependent variables as labels. Each of these data pairs is called a training examples.
Training example(x, y) is a feature and label data pair.
    - Features(x) are the characteristic that are input variables of the models.
    - Labels(y) is the observed value(the exact value corresponds to its input varibles).   
    [<img src="{{ site.baseurl }}/images/traindata.png" alt="Constructocat by https://github.com/jasoncostello" style="width: 800px;"/>]({{ site.baseurl }}/)

<strong>2. Hypothesis function:</strong>     
- As the model above, h(x) is hypothetical function that maps the values of X to the corresponding Y value. This Y value is the predicted value of the hypothesis function based on the input variables. This value may be equal to or different from the observed value a distance. This distance is used to calculate the cost of the model.    
[<img src="{{ site.baseurl }}/images/hypothesis.png" alt="Constructocat by https://github.com/jasoncostello" style="width: 800px;"/>]({{ site.baseurl }}/)

<strong>3. Cost function:</strong>   
- From the distance that we mentioned in the part 2, we will calculate the cost of the model through the cost function. This cost function is determined based on the hypothesis function. We will explore the specific fomular of cost function in the following sections. In general, the cost of the hypothesis on the data set is calculated based on the <strong>output values</strong> of the hypothesis function and the <strong>observed values</strong>.     
- The purpose of the cost function to measure the accuracy of the hypothesis function. The lower the cost of the hypothesis function, the higher the reliability.

<strong>4. Parameter learning:</strong>     
- So we have our hypothesis and we have cost function to measure how well it fits into the data. Now we need to estimate the parameters of the hypothesis function. The parameters are the number that affects directly to output of the model.
- There are currently many algorithms for learning these parameters. Here I will mention two algorithms, gradient descent, and normal equation. We will learn more about it later.

### Conclusion

We build the model to predict labels from features available. Using training data set to train the model, it means to make the model learn its parameters. The accuracy of the model will measure by the cost function. The cost of the model on the test dataset lowers the models, the more reliable the model. To train the model, we can use either gradient descent or normal equation algorithms.

Reference:
1. [Course](https://www.coursera.org/learn/machine-learning/home/week/1)