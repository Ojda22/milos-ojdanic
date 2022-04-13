---
layout: post
title: What is the effect size?
subtitle: We need to measure the magniture
thumbnail-img: /assets/img/thumb.png
tags: [statistics, introduction]
category: blog
---    

```
Statistical significance is the least interesting thing about the results. 
You should describe the results in terms of measures of magnitude. 
Not just, does a treatment affect people, but how much does it affect them.

    -Gene V. Glass
```
```
The primary product of a research inquiry is one or more measures of effect size, not P values.

    -Jacob Cohen
```

We heard many times that results are statistically significant. 
Okay, this is a claim with substantially strong terminology for someone to confront it. 
But what does it mean, or better, what this claim tries to tell me? 
It claims nothing else, but results emerging from some data points are not due to chance but due to existing variability in results.

Even though sometimes it is enough to know that the difference is significant, more ofter this information is not complete. 
The rationale lies behind a sneaky trick. 
As we increase the number of data points observed, the difference will converge towards significance (unless there is no effect whatsoever, effect size exactly zero). 
Thus, statistical significance tests depend on sample size, and for this reason, the p-value is deemed to be entangled with many misuses. 
Therefore, to better understand reported results, experimental design, analysis, we need to comprehend the magnitude of the difference between observed data points. 
And now, get ready; we are talking about the **_effects size_** of results.

Note, while the p-value (probability of significance) inform whether the effect exists (p-value larger than alpha level chosen 0.01, 99% confidence), it does not tell us about the size of the effect. 
So, to not be misguided when reading about reported study, look both for substantive significance (effect size) that statistical significance (p-value) refers to.

In fact, an estimate of the effect size is often needed before starting the research endeavour to calculate the number of subjects likely to be required to avoid a Type II, or β, error, which is the probability of concluding there is no effect when one actually exists. 
In other words, you must determine what number of subjects in the study will be sufficient to ensure (to a particular degree of certainty) that the study has adequate power to support the null hypothesis. 
Only then, if no difference is found between the groups, it is a factual finding.

Even significant differences, if very, very small, are often meaningless - thus, measure the effect size, don't forget!.

Here is an implementation of the effect size offered by Vargha and Delaney [1]: [https://gist.github.com/timm/5630491](https://gist.github.com/timm/5630491)

How to evaluate the effect size?

Effect size is calculated based on the purpose of the study, with different indices. 
There are two main categories: the effect size between the groups and the size between variables.

Effect size can be measured by the standardized difference between two means for two independent groups. ```(ex. mean(group1) - mean(group2) / standard_deviation of either group)```

Cohen's term d [2] is an example of an effect size index. 
He classified it as small (d=0.2), medium(d=0.5), and large (d>=0.8). 
These values can also be used at the planning stage to fund the sample size required for sufficient power for your study. (please refer to the previous post)

Between groups means, the effect size can also be understood as the average percentile distribution of group 1 vs group 2, or the amount of overlap when comparing their distributions. 
Thus, for an effect size of 0, the mean value of one group will be at the 50th percentile of another group, with distributions completely overlapping, that is, no difference. 
For an effect size of 0.8, the mean of group 2 is at the 79th percentile of group 1, meaning that a mean data point from group 2 will be higher than 79% of the value from group 1. 
And their distribution overlaps only at 53% of cases, which means non-overlap at 47%.

Reference:

[1] A. Vargha and H. D. Delaney, A critique and improvement of the CL common language effect size statistics of McGraw and Wong. Journal of Educational and Behavioral Statistics, 25(2):101-132, 2000)

[[2]  https://www.statisticshowto.com/cohens-d/](https://www.statisticshowto.com/cohens-d/)

[[3] https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3444174/](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3444174/)

[[4] Lux Devroye, Non-Uniform Random Variate Generation 1986, Springer-Verlag, School of Computer Science, McGill University, Montreal Canada](http://www.eirene.de/Devroye.pdf)

[[5] Sullivan GM, Feinn R. Using Effect Size-or Why the P Value Is Not Enough. J Grad Med Educ. 2012;4(3):279-282. doi:10.4300/JGME-D-12-00156.1](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3444174/)
