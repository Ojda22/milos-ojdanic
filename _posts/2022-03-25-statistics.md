---
layout: post
title: Let's hypothesise
subtitle: Around something significant?
thumbnail-img: /assets/posts/science_icon.png
tags: [statictics, introduction]
---

You may often hear about statistical hypothesis tests. 
More than in other places, they are encountered in science. 
There, serving as a scientific instrument to express the confidence of a scientific statement. 
So what is it about, and how do we do it?

A _**statistical hypothesis test**_ regards the outcome of the observations. 
Precisely, it regards whether there is no difference between specific characteristics of a population. 
Or, if there is a slight difference, we hypothesise it must be a due chance alone. Sounds familiar? 
This kind of hypothesis is called the **_null hypothesis_** (H<sub>0</sub>). 
While alternative (everything against null hypothesis), well, it is called **_alternative hypothesis_** H<sub>1</sub> or H<sub>a</sub>.

The test is often analysed by employing a _**p-value**_.
The value is the probability of obtaining test results at least as extreme as the results observed, under the assumption that the null hypothesis is correct. 
For example: Are boys taller than girls at age eight? The null hypothesis is that "they are the same average height."

When analysing the p-value of a significance test, we must establish a _**significance level**_, usually referred to as the Greek lower case letter alpha (a). 
A standard value for the significance level is 5%, reported as 0.05, and formally represents the frontier for specifying a statistically significant finding.

A significance test is "_**statistically significant**_" if the p-value is less than the significance level. 
In this case, the null hypothesis is rejected. Thus:

_**p <= alpha**_: reject H<sub>0</sub>, different distribution.

_**p > alpha**_: fail to reject H<sub>0</sub>, same distribution.

Be aware that the p-value is just a probability. 
And when dealing with probabilities, the event can go both directions, correct and not correct. 
In our context, the test could be wrong, and with it, our interpretation of the results.

There are two types of errors; they are:

_**Type I Error:**_ Reject the null hypothesis when there is no significant effect (false positive). The p-value is optimistically small.
<br>
**_Type II Error:_** Not reject the null hypothesis when there is a significant effect (false negative). The p-value is pessimistically large.

So it must be something that helps us gain confidence whether we correctly reject the null hypothesis, right?. 
Yes, a probability (not expecting it right) measures this confidence, formally called _**statistical power**_.

Statistical power has relevance only when the null is false, as it is the probability that a test will correctly reject a false null hypothesis.

The higher the statistical power for a given experiment, the lower the probability of making a Type II (false negative) error. 
The higher the probability of detecting an effect when there is an effect. 
The power is precisely the inverse of a Type II error probability.

Power = 1 - Type II Error
<br>
Prob.(True Positive) = 1 - Prob.(False Negative)

When interpreting statistical power, we seek experiential setups with high statistical power.

_**Low Statistical Power**_: Large risk of committing Type II errors, e.g. a false negative.<br>
_**High Statistical Power**_: Small risk of committing Type II errors.

Experimental results with too low statistical power will lead to invalid conclusions about the meaning of the results. 
Therefore a minimum level of statistical power must be reached.

As a good start, it is good practice to use reasonable defaults for some parameters, such as a significance level of 0.05 and a power level of 0.80. 
A power analysis can then estimate the minimum sample size required for the particular experiment. For more information, here come the references:

### References

[Wikipedia](https://en.wikipedia.org/wiki/Null_hypothesis) <br>
[Article: A Gentle Introduction to Statistical Power and Power Analysis in Python](https://machinelearningmastery.com/statistical-power-and-power-analysis-in-python/) <br>
[Book: Practical Statistics for Data Scientists](https://www.researchgate.net/profile/Janine-Zitianellis/post/Can_anyone_please_suggest_a_books_on_machine_learning_using_R_Programming/attachment/613a5b83647f3906fc975a71/AS%3A1066204907204608%401631214467436/download/Practical+Statistics+for+Data+Scientists+50%2B+Essential+Concepts+Using+R+and+Python+by+Peter+Bruce%2C+Andrew+Bruce%2C+Peter+Gedeck.pdf)
