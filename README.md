# Decision-Tree-Algorithm

Although we hear a lot about deep learning these days, there is a wide variety of other machine learning techniques that can still be very useful. Decision tree learning is one of them. By recursively partitioning your feature space into segments that group common elements yielding a class outcome together, it becomes possible to build predictive models for both classification and regression.


* * *

## What are decision trees?

Suppose that you have a dataset that describes wines in many columns, and the wine variety in the last column.

These independent variables can be used to build a predictive model that, given some new inputs, tells us whether a specific measurement comes from a wine of variety one, two or three, ...

As you already know, there are many techniques for building predictive models. Deep neural networks are very popular these days, but there are also approaches that are a bit more _classic_ - but not necessarily wrong.

Decision trees are one such technique. They essentially work by breaking down the decision-making process into many smaller questions. In the wine scenario, as an example, you know that wines can be separated by color. This distinguishes between wine varieties that make _white wine_ and varieties that make _red wine_. There are more such questions that can be asked: what is the alcohol content? What is the magnesium content? And so forth.

![DecisionTree](https://user-images.githubusercontent.com/90423812/195668784-66d47078-08f8-4ecd-8f20-bfbbfd69d02c.png)
An example of a decision tree. Each variety (there are three) represents a different color - orange, green and purple. Both color and color intensity point towards an estimated class given a sub question stage. For example, the first question points towards class 2, the path of which gets stronger over time. Still, it is possible to end up with both class 1 and class 3 - by simply taking the other path or diverting down the road.

* * *

## How are decision tree classifiers learned in Scikit-learn?

When learning a decision tree, it follows the **Classification And Regression Trees** or **CART** algorithm - at least, an optimized version of it. Let's first take a look at how this algorithm works, before we build a classification decision tree.

### Learning a CART tree

At a high level, a CART tree is built in the following way, using some _split evaluation criterion_ (we will cover that in a few moments):

1. Compute all splits that can be made (often, this is a selection over the entire feature space). In other words, do this for each of the independent variables, and a target value. For example, in the tree above, "Proline <= 755.0" in the root node is one such split at the first level. It's the _proline_ variable, with _755.0_ as the target value.
2. For each split, compute the value of the _split evaluation criterion_.
3. Pick the one with the best value as the split.
4. Repeat this process for the next level, until split generation is exhausted (by either a lack of further independent variables or a user-constrained depth of the decision tree).

In other words, the decision tree learning process is a recursive process that picks the best split at each level for building the tree until the tree is exhausted or a user-defined criterion (such as maximum tree depth) is reached).

* * *

## Attribute Selection Measures

If the dataset consists of N attributes then deciding which attribute to place at the root or at different levels of the tree as internal nodes is a complicated step. By just randomly selecting any node to be the root can’t solve the issue. If we follow a random approach, it may give us bad results with low accuracy.

For solving this attribute selection problem, researchers worked and devised some solutions. They suggested using some criteria like :
- Information Gain
- Gini Index

You can learn more about them from [here](https://www.kdnuggets.com/2020/01/decision-tree-algorithm-explained.html).

* * *

## What needs to be done?

- Build a Decision Tree algorithm from scratch and using SKLearn and trained on the Titanic dataset.
- Compare the accuracy for both the methods.

### Dependencies

- NumPy
- Pandas
- Matplotlib

* * *


## *****How to contribute?*****

- Clone the Repository.
- Create an issue telling us about your idea or project.
- Wait for the maintainer to assign you the issue.
- You can start working as soon as the issue is assigned to you.
- Make sure you make your own folder named as your github username and upload your content there.
- Now if you have successfully completed your work, you are ready to make the pull request.
- Congrats, you have made your PR! Now wait for the Maintainer to check for the plagiarism and project working.

## Note

- Codes must have comments to explain them.
- All contributors must follow the contribution rules in order to get their PRs merged.
- Be respectful to people in the comment section.
- If you are following a Youtube video, make sure you do some changes and *****not submit the exact code*****.
