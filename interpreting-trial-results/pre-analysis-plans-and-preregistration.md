# Pre-analysis plans and pre-registration

A pre-analysis plan is a step-by-step plan setting out how you will analyse the data from your experiment. It is written before data collection, or at least before seeing the data.

Components of a pre-analysis plan typically include:

-   A description of the sample that will be used, including proposed sample size and randomisation techniques
-   The hypotheses to be tested
-   How any variables will be constructed (i.e. you may be planning to manipulate data in the analysis, such as by excluding outlier values or transforming it to log levels)
-   What statistical tests will be used
-   How you will deal with multiple outcomes

Commitment to a pre-analysis plan is required to be able to take p-values at their face value.Why? A p-value is the probability of the data on the assumption that the null hypotheses is true. As we noted before, our measurement of the data is a test statistic such as a z-score.But your measurement of the data relies on the analysis you choose. If you change that analysis based on the data you see (e.g. by excluding outliers or measuring at a different point in time or using a different outcome measure) your p-value is no longer the probability of the data given the null hypothesis is true. The p-value is now the probability of the data given the null hypothesis is true and given you made a series of choices.

To put this into more practical terms, all of the choices that are specified in a pre-analysis plan affect the chance of "success" of a trial. The more degrees of freedom you allow yourself in your analysis, the more likely you are to stumble upon a p-value lower than 0.05 by chance. Don't find anything at 6 months, try 12. Maybe exclude the outlier. And so on.

These researcher degrees of freedom are one reason behind the "replication crisis" that we will explore in the third module.

### Preregistration

Preregistration is publication of the pre-analysis plan in a public archive. This acts as a form of commitment to the pre-analysis plan and enables others to verify that you have done the analysis as you stated.

As an example, BETA at PM&C pre-registers many of it studies. You can see some of the pre-registered studies [here](https://www.socialscienceregistry.org/trials/search?search%5Binvestigator_name%5D=BETA+Team+Registration).