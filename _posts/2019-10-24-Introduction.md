---
layout: post
title: Introduction of machine learning 
---
### Definitions
Two definition machine learning are offered. Arthur Samuel described it as: "the field of study that give computers the ability to learn without being explicitly programmed." This is an older, infomal definition.

Tom Mitchell provides a more moderm definition:"A computer program is said to learn from experience E with respect to some class of task T and performance measure P, if performance at task in T, as measured by P, improve with experience E". 

- Example: playing chekers
    - E = the experience of playing many game of checkers
    - T = the task of playing checkrs
    - P = the probability that program will win next game

According to definition of Wikipedia: Machine learning is the subfield of computer science that "gives computers the ability to learn without being explicitly programed". 

In general, any machine learning problem can be assign to one of two broad classification:
> Supervised learning and Unsupervised learning

### Supervised learning
In supervised learning, we are given a data set(training set) and already know what our correct ouput should look like, having the idea that there is a relationship between the input and the output.

Supervised learning problem are categorized into <strong><em>regression</em></strong> and <strong><em>classification</em></strong>. In a regression problem, we are trying to predict results with a continuous ouput, meaning that we are trying to map input variables to some continuous function. In a classification problem, we are instead trying to predict results in a discrete output. In the words, we are trying to map input variable into discrete categories.

- Example 1:
    - Give data about size of houses on the read estate market, try to predict their price. Price as function of size is continuous output, so this is a regression problem.
    - We could turn this example into a classification problem by instead making our output about whether the house "sell for more or less than the asking price". Here we are classifying the houses base on price into two discrete categories.
- Example 2:
    - Regression - Given a picture of a person, we have to predict their age on the basis of the given picture.
    - Classification - Given a patient with a tumor, we have to predict whether the tumor is maligant or begin.

### Unsupervised learning
Unsupervised learning allow us approach problem with little or no idea what our results should look like. We can derive(suy ra) structure from data where we don't necessarily know effect of the variables.

We can derive this structure by clustering the data base on relationships among the variables in the data.

With unsupervised learning there is no feedback base on the prediction results.

- Example:
    - Clustering: Take a collection 1,000,000 different gens, and find a way to autumatically group into groups that somehow similar or related by different variables, such as lifespan, location, roles, and so on. 
    - Non-clustering: The "Cocktail Party Algorithm", allows you to find structure in chaotic environment.(i.e identifying individual voices and music from a mesh sounds at [a cocktail](https://en.wikipedia.org/wiki/Cocktail_party_effect))

[<img src="{{ site.baseurl }}/images/InstroductionML.png" alt="Constructocat by https://github.com/jasoncostello" style="width: 800px;"/>]({{ site.baseurl }}/)