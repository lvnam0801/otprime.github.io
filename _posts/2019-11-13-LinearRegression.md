---
layout: post
title: Linear Regression
---
### Definition

As mentioned in the previous section, regression analysis is a statistical analysis to determine the relationship between dependent variable and one or more independent variables. Linear regression is the most common form of regression analysis.

Linear regression is a linear approach to modeling the relationship between dependent variable and one or more independent variables. The relationships are modeled using linear predictor function whose unknown model parameters are estimated(learned) from the data. Such models are called linear models. It attempts to model the relationship between two variables by fitting a linear equation to observed data.

### Model presentation for linear regression

A linear regression line has an equation of the form <strong>Y = a + bX</strong>, where <strong>X</strong> is the explanatory variable(independent variable) and <strong>Y</strong> is the dependent variable. The slope of the line is <strong>b</strong>, and <strong>a</strong> is the intercept(the value of <strong>y</strong> when <strong>x</strong> = 0 also called bias)

<strong>1. Hypothesis function</strong>

We will instead the equation above Y = a + bX by the equation:

[<img src="{{ site.baseurl }}/images/LinearRegression/Hypothesis.png"/>]({{ site.baseurl }}/)

- Theta is weight matrix of the model. This matrix contains parameters for estimating the label respect with features. It will be trained in models(parameters learning that mentioned in previous section). Theta_0 is called bias.
- X is feature in the training data set(independent variables).
- Output of the equation is continuou values.

<strong>2. Cost function</strong>   
[<img src="{{ site.baseurl }}/images/LinearRegression/CostFunction.png"/>]({{ site.baseurl }}/)

We can see that the cost is calculated by geting square of distant sum between the straight line of hypothesis function and data points(the observed values).
- J is notation of the cost function. J is calculated base on the theta. At each theta, J will have difference values.
- J divide m to deduct the value of the cost function.
- 1/2 is coefficient to reduce when we derivate the cost function.

As the graph above, if data points (observed datas) closer the the straight line(hypothesis), the more lower the cost. 

<strong>3. Learning parameters</strong>

Our model have weight matrix. And we need to train this parameters. We have two algorithm: gradient descent and normal equation.    
<strong>Gradient descent:</strong>
Gradient descent is calcalated base on the cost function derivation.

[<img src="{{ site.baseurl }}/images/LinearRegression/Gradient.png"/>]({{ site.baseurl }}/)

Recall derivation, derivation at a value ,is used to find direction that function the fastest growing. So we gradient the confucntion to find the direction that the cost function increase the fastest way. Then, we go back the direction to make the cost function decrease the fastest way.

- J is calculated base on the theta parameters, so we will change the theta parameters to find the gobal minimum of the cost function. We derivation at the certain theta value, then we decrease the theta a range small according to the direction that we derivated the cost function. Each repeat, the cost will decrease a bit. And we will repeat untill convergence(Get to the smallest value of the cost function). Alphe is learning rate. This learning rate must be small enough to avoid convergenced point exceeded.

<strong>Normal equation:</strong>    

[<img src="{{ site.baseurl }}/images/LinearRegression/NormalEquation.png"/>]({{ site.baseurl }}/)

<strong>Compare</strong>: <em>gradient descent</em> and <em>Normal equation</em>     
[<img src="{{ site.baseurl }}/images/LinearRegression/Compare.png"/>]({{ site.baseurl }}/)

### Particular problem

Suppose you are CEO of the restaurant franchise and are cosidering the difference cities for opening the new outlet. The chain already has trucks in various cities and you has data for profit and population from the cities. You would like to use this data to help you select which city to expand to next.

<strong>Dataset</strong>

[<img src="{{ site.baseurl }}/images/LinearRegression/Dataset.png"/>]({{ site.baseurl }}/)

- First colum is population of the cities(feature).
- Second colum is profit of the food truck in that city(label).

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