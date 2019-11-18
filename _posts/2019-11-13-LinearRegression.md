---
layout: post
title: Linear Regression
---
### Definition

As mentioned in the previous section, regression analysis is a statistical analysis to determine the relationship between the dependent variable and one or more independent variables. Linear regression is the most common form of regression analysis.

Linear regression is a linear approach to modeling the relationship between the dependent variable and one or more independent variables. The relationships are modeled using linear predictor function whose unknown model parameters are estimated(learned) from the data. Such models are called linear models. It attempts to model the relationship between two variables by fitting a linear equation to observed data.

### Model presentation for linear regression

A linear regression line has an equation of the form <strong>Y = a + bX</strong>, where <strong>X</strong> is the explanatory variable(independent variable) and <strong>Y</strong> is the dependent variable. The slope of the line is <strong>b</strong>, and <strong>a</strong> is the intercept(the value of <strong>y</strong> when <strong>x</strong> = 0 also called bias)

<strong>1. Hypothesis function</strong>

We will instead of the equation above Y = a + bX by the equation:

[<img src="{{ site.baseurl }}/images/LinearRegression/Hypothesis.png"/>]({{ site.baseurl }}/)

- Theta is the weight matrix of the model. This matrix contains parameters for estimating the label respect with features. It will be trained in models(parameters learning mentioned in the previous section). Theta_0 is called bias.
- X is a feature in the training data set(independent variables).
- The output of the equation is continuous values.

<strong>2. Cost function</strong>   
[<img src="{{ site.baseurl }}/images/LinearRegression/CostFunction.png"/>]({{ site.baseurl }}/)

We can see that the cost is calculated by getting square of the distant sum between the straight line of hypothesis function and data points(the observed values).
- J is a notation of the cost function. J is calculated base on the theta. At each theta, J will have different values.
- J divide m to deduct the value of the cost function.
- 1/2 is the coefficient to reduce when we derivate the cost function.

As the graph above, if data points (observed data) closer to the straight line(hypothesis), the lower the cost. 

<strong>3. Learning parameters</strong>

Our model has a weight matrix. And we need to train these parameters. We have two algorithms: gradient descent and the normal equation.    
<strong>Gradient descent:</strong>
Gradient descent is calculated base on the cost function derivation.

[<img src="{{ site.baseurl }}/images/LinearRegression/Gradient.png"/>]({{ site.baseurl }}/)

Recall derivation, derivation at a value, is used to find a direction that function the fastest growing. So we gradient the conjunction to find the direction that the cost function increases the fastest way. Then, we go back to the direction to make the cost function decrease the fastest way.

- J is calculated base on the theta parameters, so we will change the theta parameters to find the global minimum of the cost function. We derivation at the certain theta value, then we decrease the theta a range small according to the direction that we derivated the cost function. Each repeat, the cost will decrease a bit. And we will repeat until convergence(Get to the smallest value of the cost function). Alpha is the learning rate. This learning rate must be small enough to avoid convergence point exceeded.

<strong>Normal equation:</strong>    

[<img src="{{ site.baseurl }}/images/LinearRegression/NormalEquation.png"/>]({{ site.baseurl }}/)

<strong>Compare</strong>: <em>gradient descent</em> and <em>Normal equation</em>     
[<img src="{{ site.baseurl }}/images/LinearRegression/Compare.png"/>]({{ site.baseurl }}/)

### Particular problem

Suppose you are the CEO of the restaurant franchise and are considering the different cities for opening the new outlet. The chain already has trucks in various cities and you have data for profit and population from the cities. You would like to use this data to help you select which city to expand to next.

<strong>Dataset</strong>

[<img src="{{ site.baseurl }}/images/LinearRegression/Dataset.png"/>]({{ site.baseurl }}/)

- First column is the population of the cities(feature).
- Second column is the profit of the food truck in that city(label).

<strong>Visualize dataset</strong>        
[<img src="{{ site.baseurl }}/images/LinearRegression/VisData.png"/>]({{ site.baseurl }}/)

<strong>Hypothesis in this problem</strong>     
[<img src="{{ site.baseurl }}/images/LinearRegression/P_hypothesis.png"/>]({{ site.baseurl }}/)

<strong>The cost function</strong>      
[<img src="{{ site.baseurl }}/images/LinearRegression/CostFomular.png"/>]({{ site.baseurl }}/)

<strong>The gradient descent algorithm</strong>     
[<img src="{{ site.baseurl }}/images/LinearRegression/GradientFormula.png"/>]({{ site.baseurl }}/)

<strong>Visualize model</strong>    
[<img src="{{ site.baseurl }}/images/LinearRegression/GraphModel.png"/>]({{ site.baseurl }}/)

[<img src="{{ site.baseurl }}/images/LinearRegression/GraphCost.png"/>]({{ site.baseurl }}/)

[<img src="{{ site.baseurl }}/images/LinearRegression/GraphSurfaceCost.png"/>]({{ site.baseurl }}/)

[<img src="{{ site.baseurl }}/images/LinearRegression/GraphContourCost.png"/>]({{ site.baseurl }}/)