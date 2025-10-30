# Type I error control

We set the rate of Type 1 errors through the significance level. A standard significance level of $\alpha=0.05$ gives a 5% false positive rate if the null hypothesis is true.

There are many recent arguments that $\alpha$ should be smaller than 0.05, such as Benjamin et al's [-@benjamin2018] argument that $\alpha$ should be set at 0.005. Many of these relate to the replication crisis that we will cover this later in this course. We simply want to generate less false positives.

## Multiple comparisons

One scenario where there is a longer history of using a smaller alpha is where you are testing multiple hypotheses. This could arise because you have multiple treatment groups or because you are measuring many potential outcomes.

If you are testing many hypotheses, it becomes increasingly likely that at least one of them will meet the statistical threshold merely by chance. If you conduct 20 tests and all of null hypothesis for each test is true, you expect one false positive.

![](https://imgs.xkcd.com/comics/significant.png)

A common correction applied to $\alpha$ in instances of multiple comparisons is the Bonferroni correction. If you are testing *m* hypotheses, set the significance level for each hypothesis at $\frac{\alpha}{m}$. The Bonferroni correction is conservative in that it decreases the family-wise error rate - which is the probability of making one or more false discoveries - to below 0.05.

A Bonferroni type correction is typically applied where there is large-scale multiple testing. In genomic association studies, where they are testing of the order of a million genetic variants, they will normally set the significance level at 5x10$^{-8}$

A smaller significance level and associated higher critical value means, however, that we will get a higher rate of Type II errors. We will discuss this in the following pages.

## Replication data sets

An alternative method of Type I error control is use of a replication sample, which is a subset of the data that is excluded from the initial analysis. If there are any significant results in the first analysis, testing for those hypotheses that were significant in the first is conducted on the replication sample.

This approach is common in machine learning applications, but is starting to become more common in statistical analysis. However, it is rarely used in experimental analysis.

We will cover the concept of replication more broadly in week 6.
