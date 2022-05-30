---
layout: post
title: Machine Learning Dictionary
subtitle: Definitions, meanings, explanations...
thumbnail-img: /assets/posts/dictionary.png
tags: [machine learning, fundamentals]
category: blog
---    

[WIP](./202.html) - stay tuned... 

<!---
```Training``` - estimating parameters for machine learning methods using set of data D
```Testing``` - evaluating how well does a method works on new data D' after training

```N-Fold Cross-Validation``` - instead of using only one set D' for testing, lets divide D+D' in N blocks, and perform training N times, while each time using different block from N for testing, and N-1 for training.

```Confusion metrix``` - summary how does a machine learning method algorithm performs. Rows on the matrix corresponds what machine learning algorithm predicted. And columns corresponds to known truth.

```True Possitive``` - Model identifies as correct what is correct
```True Negative``` - Model identifies as negative what is negative
```False Negative``` - Model identifies as negative what is correct
```False Possitive``` - Model identifies as correct what is negative

```Sensitivity``` - Percentage of correct instances correctly identified as correct (TP / TP + FN)
```Specificity``` - Percentage of incorrect instances correctly classified as incorrect (TN / TN + FP)

```Bias``` - Inability for a machine learning method (like linear regression) to capture true relationship of data instances. High bias does not capture well, low bias captures well (maybe too well)
```Variance``` - Difference in fits between data sets

```Overfit``` - Method performs well on training data set and not well on testing data set. Ideally, model has low bias (accurately models true relationship of data), and low variability (producing consistent predictions across different datasets)

```Mean Squered Error``` - measures distance from the data to the fit line, square them and add them up (squared so that negative distances do not cancel out the positive distances)

```Probability``` - The chance of the occurrence of an event x: p(x)
```Surprise``` - How surprising is to observe an event: log2(1/p(x))
```Entropy``` - The expected value of a surprise: Sigma(sum) p(x) log2(1/p(x)) 

--->