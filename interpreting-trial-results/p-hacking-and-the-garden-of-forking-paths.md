# P-hacking and the garden of forking paths

## P-hacking

In conducting their analysis, researchers have many decisions to make. Should they collect more data? How should they process the data? Should they transform it in any way? Should they exclude outliers? What statistical tests will they use? What outcomes will they test? And so on.

P-hacking occurs where researchers use this flexibility in their data collection, analysis and reporting to inflate their rate of significant findings. Result not significant yet? Collect some more data. Result not significant with that extreme data point? Exclude it. No significant change after 6 months? Try 12. No significant effect for people predicting what picture is behind the curtain? Let's restrict the analysis to the erotic ones.

A p-value of 0.05 sets an effective false positive rate of 0.05. You will only see data that extreme 5% of the time if the null hypothesis is true. But if you look at the data in many different ways and select only those arrangements that result in low p-values, the p-value ceases to be informative about the false positive rate. The false positive rate will be much higher [@simmons2011].

P-hacking is considered to be a major cause of the replication crisis. Even without publication bias, p-hacking can dramatically inflate the rate of false positives in the literature that will fail to replicate if tested.

### P-hacking without intent

P-hacking should not be taken to infer nefarious research practices (Brian Wansink and the Cornell Food Lab excepted [@lee2018]). Nor is p-hacking necessarily a case of the researcher making many comparisons and throwing out those results that don't meet their needs.

Rather, researchers might do a single analysis given their assumptions and the data. However, that single analysis is contingent on the data they see. If the data had been different they might have done a different analysis. There is effectively a large number of comparisons they could have done, and they pick the a more prospective approach. Andrew Gelman and Eric Loken [-@gelman2013] call this the garden of forking paths. Even though seemingly benign, the selection of the most prospective path effectively inflates the false positive rate.

### An example

Andrew Gelman Jennifer Hill and Aki Vehtari [-@gelman2020] write:

> We demonstrate the last two problems mentioned above --- multiple potential comparisons and the statistical significance filter --- using the example of a research article published in a leading journal of psychology. The article begins:
>
> > Each month many women experience an ovulatory cycle that regulates fertility. Whereas research finds that this cycle influences women's mating preferences, we propose that it might also change women's political and religious views. Building on theory suggesting that political and religious orientation are linked to reproductive goals, we tested how fertility influenced women's politics, religiosity, and voting in the 2012 U.S. presidential election. In two studies with large and diverse samples, ovulation had drastically different effects on single versus married women. Ovulation led single women to become more liberal, less religious, and more likely to vote for Barack Obama. In contrast, ovulation led married women to become more conservative, more religious, and more likely to vote for Mitt Romney. In addition, ovulatory-induced changes in political orientation mediated women's voting behavior. Overall, the ovulatory cycle not only influences women's politics, but appears to do so differently for single versus married women.
>
> One problem here is that there are so many different things that could be compared, but all we see is some subset of the comparisons. Some of the choices available in this analysis include the days of the month characterized as peak fertility, the dividing line between single and married (in this particular study, unmarried but partnered women were counted as married), data exclusion rules based on reports of menstrual cycle length and timing, and the decision of which interactions to study. Given all these possibilities, it is no surprise at all that statistically significant comparisons turned up; this would be expected even were the data generated purely by noise.

### Preventing p-hacking

There are many proposed solutions for p-hacking. The major solution is pre-registration of analysis plans. These transparently commit researchers to an approach, meaning that we can then take the p-value as a prima facie indication of seeing data that extreme under the assumption that the null hypothesis is true. These are discussed further on the next page.