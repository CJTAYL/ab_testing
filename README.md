# A/B Testing for Advertising Campaign

<img src='https://github.com/CJTAYL/ab_testing/assets/64110892/a3d93c1e-d3a4-45d5-b4cb-13bbcc7c5538' width='400' height='400' />


## Executive Summary 

An A/B test was conducted to evaluate the effects of a new advertising campaign on total amount spent in dollars. A total of 60 consumers participated in the study. Thirty were assigned to the control group, which used the current advertising campaign, and 30 were assigned to the test group, which used the proposed advertising campaign. The results of an independent t-test indicated a statistically significant difference between the two groups. Specifically, consumers exposed to the proposed advertising campaign spent more in total dollars compared to consumers exposed to the current campaign. Based on the results of the analysis, the new advertising campaign should be implemented. 

## Methodology

The primary dependent variable was total amount spent in dollars. The variable was identified by the marketing team as a key metric for evaluating the new advertising campaign. 

Data were also collected on 9 other variables:
- Group assignment
- Date
- Impressions
- Reach (number of unique impressions received)
- Clicks (Number of website clicks received through the ads)
- Searches (Number of users who performed at least one search on the website)
- View (Number of users who viewed content on the website)
- Add to cart (Number of users who added products to their cart)
- Purchase (Number of purchases)

When conducting a A/B test, one should develop a null and alternative hypothesis and select a significance level prior to examining the data. A significance level of 0.05 was used and the null and alternative hypotheses for the current test are listed below:

$H_0$: The population means for the groups are equal.

$H_1$: The population mean for the test group is higher than the population mean for the control group.

Before conducting the analysis, the data were cleaned and missing values were replaced with the column median for the group assignment. For example, if a participant in the control group did not have data recorded for the Searches, the median number of clicks for all participants in the control group was used for the value. 

After cleaning the data, point plot, which is displayed below, was generated to determine if there was a difference in the mean total dollars spent between the groups. 

![image](https://github.com/CJTAYL/ab_testing/assets/64110892/d67a887a-d38d-4d86-8b3a-535200b55651)

The project aimed to compare the means of the control and test group, therefore an independent t-test was identified as the most appropriate hypothesis test. Before conducting a hypothesis test, one should ensure that the  assumptions for the test are met. Some assumptions are met through the appropriate experimental design choices (indicated with an asterisk) and others are determined after the data have been collected. 

The assumptions for an independent t-test are:
- independence of observations*
- no significant outliers 
- data for each group should be approximately normally distributed 
- the variance of the dependent variable should be approximately equal across groups
- samples are drawn from the population at random*
- the dependent variable must be measured on an interval or ratio scale*

To determine if a significant outliers were present in the data, a box plot of the dependent variable was generated. 

![image](https://github.com/CJTAYL/ab_testing/assets/64110892/ab816b44-dac1-45f5-bc76-3603d2b8f961)


The absence of data points beyond the whiskers indicates that there are no significant outliers in the dataset. Additionally, it provides evidence that the variance between the two groups is approximately equal. 

To determine if the data for each group was approximately normally distributed, a histogram of the dependent variable was generated. 

![image](https://github.com/CJTAYL/ab_testing/assets/64110892/4b13aa60-e08f-41af-a6bd-b2cbfad69883)

The histogram provides some evidence that the distributions are approximately normal. To gain a better understanding of the data and ensure that the assumption is met, the Wilks-Shapiro test was conducted. The hypothesis for the test are: 

$H_0$: The sample data are drawn from a normal distribution.

$H_1$: The sample data are not drawn from a normal distribution. 

When using a significance level of 0.05, the p-value did not indicate sufficient evidence to reject the null hypothesis. In other words, the results of the test indicate the sample is drawn from a normal distribution. 

Although the box plot provided some evidence that the variance across groups was equal, Bartlett’s test was conducted to ensure the assumption of equal variance was met. The hypotheses for the test are:

$H_0$: The variances are equal across groups.

$H_1$: The variances are not equal across groups.

When using a significance level of 0.05, the p-value did not indicate sufficient evidence to reject the null hypothesis. In other words, the results of the test indicate the variance is approximately equal across groups.

## Results of Independent T-Test 

After the assumptions of the hypothesis test were verified, an independent t-test was conducted. The results of the test are presented below:

Test Statistic: 2.97
P-Value: 0.0043
Interpretation: Reject the null hypothesis

A 95% confidence interval was calculated to provide additional information about the group means. The intervals were:

- Mean Difference: 274.63
- 95% Confidence Interval: (61.85.54, 487.41)

## Interpretation of Results 

The p-value is below the significance level of 0.05, indicating that there is evidence to reject the null hypothesis. In other words, there is a difference between the group means for total dollars spent. Additionally, the confidence interval does not include zero, which provides another piece of evidence that there is a difference between the two groups.

## Post-Hoc Power Analysis 

A post-hoc power analysis was conducted to determine the test’s ability to correctly reject a false null hypothesis. To determine the effect size, Cohen’s d was calculated and returned a value of 0.77. Cohen’s d, along with the significance level and number of observations, were used to calculate the power of the test, which returned a value of 0.83.
 
## Discussion 

Based on the p-value and confidence interval for the difference between group means, the null hypothesis (i.e., the group means were equal) was rejected in favor of the alternative hypothesis. Therefore, the available evidence suggests that consumers spend more money when they are exposed to the new advertising campaign. The power analysis returned a value of 0.83, which is above the commonly used value of 0.80, indicating that the test is capable of correctly rejecting a false null hypothesis and provides support for the test’s results. 
