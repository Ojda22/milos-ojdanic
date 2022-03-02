---
layout: post
title: First post
subtitle: First post subtitle
tags: [test]
---    

Statistical significance is the least interesting thing about the results. You should describe the results in terms of measures of magnitude –not just, does a treatment affect people, but how much does it affect them.

    -Gene V. Glass

    The primary product of a research inquiry is one or more measures of effect size, not P values.

    -Jacob Cohen


We heard many times about that results are statistically significant. Okay, this is a claim with substatntially strong terminology for someone to confront it. But what does it mean or better claims. It claims nothing else but that results emerging from some data points are not due to chance, but due to existing variability in results.

Even though that sometimes it is enought to know that the difference is significant it is not complete. The reason lies that as we increasing the number of data points observed, the difference will converge towards significance (unless there is no effect whatsoever, effect size exactly zero). Thus, to better understand reported results, experimental design, analysis, we need to comprehend the magnitude of the difference between observed data points. And now we are taling about effects size of results. 

Note, while the P value (probability of significance) inform whether the effect exists (P value larger than alpha level chosen 0.01, 99% confidence), it does not tell us about the size of the effect. So, to not be misguided when reading the paper, look both for substantive significance (effect size) that statistical significance (P value) refers to.

In fact, an estimate of the effect size is often needed before starting the research endeavor, in order to calculate the number of subjects likely to be required to avoid a Type II, or β, error, which is the probability of concluding there is no effect when one actually exists. In other words, you must determine what number of subjects in the study will be sufficient to ensure (to a particular degree of certainty) that the study has acceptable power to support the null hypothesis. That is, if no difference is found between the groups, then this is a true finding.

In fact, even significant differences, if very very small (measure by effect size don't forget), are often meaningless.

Here it is an implementation on the effect size from github:

Statistical significance tests dependent on sample size, unlike effect size which is not. For this reason, P value is considered to be confounded with many misuses.

How to calculate effect size:

Effect size is calcualte based on the purpose of the study, with different indices. There are two main categories, looking for effect size between the groups and the size between variables.

For two independent groups, effect size can be measured by the standardized difference between two means. (ex. mean(group1) - mean(group2) / standard_deviation of either group)

Cohens term d is an example of effect size index. He classied it as small (d=0.2), mediaum(d=0.5), and large (d>=0.8). This values can also be used at planning stage to fund the sample size required for sufficient powerfor your study.

Between groups means, the effects size can also be understood as the average percentile distribution ofr group 1 vs group 2, or the amound of overlap when comparing their distributions. Thus, For an effect size of 0, the mean value of one group will be at the 50th percentile of another group, with distributions completely overlapping, that is, no difference. For an effect size of 0.8, the mean of a group 2 is at 79th percentile of group 1, meaning that a mean data point from group 2, will be higher than 79% of value from group 1. And their distribution overlap only at 53% of cases, which means non overlap at 47%. 




What Is Statistical Power and Why Do I Need It?

Statistical power is the probability that your study will find a statistically significant difference between interventions when an actual difference does exist. If statistical power is high, the likelihood of deciding there is an effect, when one does exist, is high. Power is 1-β, where β is the probability of wrongly concluding there is no effect when one actually exists. This type of error is termed Type II error. Like statistical significance, statistical power depends upon effect size and sample size. If the effect size of the intervention is large, it is possible to detect such an effect in smaller sample numbers, whereas a smaller effect size would require larger sample sizes. Huge sample sizes may detect differences that are quite small and possibly trivial.

Methods to increase the power of your study include using more potent interventions that have bigger effects, increasing the size of the sample/subjects, reducing measurement error (use highly valid outcome measures), and raising the α level but only if making a Type I error is highly unlikely.

How To Calculate Sample Size?

Before starting your study, calculate the power of your study with an estimated effect size; if power is too low, you may need more subjects in the study. How can you estimate an effect size before carrying out the study and finding the differences in outcomes? For the purpose of calculating a reasonable sample size, effect size can be estimated by pilot study results, similar work published by others, or the minimum difference that would be considered important by educators/experts. There are many online sample size/power calculators available, with explanations of their use

Box.  Calculation of Sample Size Example

Your pilot study analyzed with a Student t-test reveals that group 1 (N  =  29) has a mean score of 30.1 (SD, 2.8) and that group 2 (N  =  30) has a mean score of 28.5 (SD, 3.5). The calculated P value  =  .06, and on the surface, the difference appears not significantly different. However, the calculated effect size is 0.5, which is considered “medium” according to Cohen. In order to test your hypothesis and determine if this finding is real or due to chance (ie, to find a significant difference), with an effect size of 0.5 and P of <.05, the power will be too low unless you expand the sample size to approximately N  =  60 in each group, in which case, power will reach .80. For smaller effect sizes, to avoid a Type II error, you would need to further increase the sample size. Online resources are available to help with these calculations.

Power must be calculated prior to starting the study; post-hoc calculations, sometimes reported when prior calculations are omitted, have limited value due to the incorrect assumption that the sample effect size represents the population effect size.

Of interest, a β error of 0.2 was chosen by Cohen, who postulated that an α error was more serious than a β error. Therefore, he estimated the β error at 4 times the α: 4 × 0.05  =  0.20. Although arbitrary, as this has been copied by researchers for decades, use of other levels will need to be explained.

Reference:

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3444174/

http://www.eirene.de/Devroye.pdf
1986, Lux Devroye, Springer-Verlag, School of Computer Science, McGill University, Montreal Canada, Non-Uniform Random Variate Generation
