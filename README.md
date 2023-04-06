[![author](https://img.shields.io/badge/author-rafaelnduarte-red.svg)](https://www.linkedin.com/in/rafael-n-duarte) [![](https://img.shields.io/badge/License-GPLv3-blue.svg)](http://perso.crans.org/besson/LICENSE.html) [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/rafaelnduarte/A-B_Testing-Experiment-Planning/issues)

# A/B Testing Experiment Planning
This is a structured plan, with direct instructions to help a marketing team perform an A/B test.

# Overview

This is the plan to execute an **A/B Test** on a website page to try to **improve conversion rates**. The hypothesis is that changing the **Call to Action (CTA) position** can **positively affect conversion numbers**, generating more submissions of the company's consulting services demo form.

In this experiment, the **null hypothesis** (current version, version A) assumes conversion rates are equal and if there is a difference this is only due to the **chance** factor. In contrast, the **alternative hypothesis** (version B) assumes there is a **statistically significant** difference between the conversion rates.

The versions should be as follows:

Version A 					Version B



For the experiment, we know that the website receives around 20.000 visitors per week, and the placement of the CTA will be the only change.
The Metrics
For this test, we will consider clicks on the CTA button as conversions. We can’t use submissions as a metric because we are assuming there are other steps that take place after the click, and the placement of the CTA might not change anything in that part of the process. For this reason, the metric we’ll analyze is conversion rate, considering a click on the button as a conversion.
Note: Since I wasn’t provided a current conversion rate, which would be our baseline, I’ll use the average landing page conversion rate provided by Wordstream as the baseline.

According to them:

	“Across industries, the average landing page conversion rate was 2.35%, yet the top 25% are converting at 5.31% or higher. Ideally, you want to break into the top 10% — these are the landing pages with conversion rates of 11.45% or higher.”

For this test, our baseline is a 2.35% conversion rate, and the goal of the test is to find out whether the placement of the CTA can improve this conversion rate.
Evaluating the Results

To validate our alternative hypothesis (the new CTA placement improves the conversion rate) we need to identify a difference in performance that can’t be the result of pure chance. For that, we need to show it to the right number of visitors so we can verify the statistical significance of the test.

These are the hypotheses of this test:


The Null Hypothesis is that the Conversion Rate of Versions A and B will be similar


The Alternative Hypothesis is that the Conversion Rate of Version B will be significantly higher than that of Version A.

Conversion Rates are calculated by dividing the number of conversions by the number of visitors on the website.

Conversions A / Visitors A
Conversions B / Visistos B

Once we have the data, we can perform a Chi-Squared test, to decide whether we should reject the Null Hypothesis or not. The Chi-Squared test assumes observed frequencies for a categorical variable (conversion, in our case) match with the expected frequencies. It calculates a test statistic (Chi) that has a chi-squared distribution and is interpreted to reject or fail to reject the null hypothesis if the expected and observed frequencies are the same. 

The probability density function of Chi-Squared distribution varies with the degrees of freedom (df) which depends on the size of the contingency table, which will be created once we have the results from the test. It should look something like this:





Outcome
Version A
Version B
Visitors
x
x
Conversions
y
z
No Conversions
x-y
x-z


To understand the statistical significance of the results, we need to understand what p-value and alpha are. 

P-value is the probability of obtaining test results at least as extreme as the results actually observed, under the assumption that the null hypothesis is correct. P-value is one of the outcomes of the test. 
Alpha, also known as the level of statistical significance, is the probability of making a type I error (rejecting the null hypothesis when it is actually true).

In general, alpha is taken as 0.05 indicating a 5% risk of concluding a difference exists between the groups when there is no actual difference.

Using p-value and alpha, we can evaluate the results as follows:

If p-value <= alpha: significant result, reject null hypothesis
If p-value > alpha: not significant result, do not reject null hypothesis

Let’s say we have a p-value of 0.25. Since it’s less than 0.5, which is the alpha, that means we have a significant result, and we should reject the null hypothesis.

In the case above, that would mean Version B is better than Version A. This is how the champion version will be elected by the end of the test.
The Data
The following data needs to be collected:
Page Views (Visitors)
Clicks on the button (Conversions)

With the number of visitors the page receives per week (20.000), we should have enough visitors to perform a valid test. The bigger the difference in performance we’re looking for, the smaller the sample size needs to be.

I suggest the test be run over the course of a week, sending 10.000 visitors to each variant.

Limitations
One of the limitations of the test is the number of visitors. As stated before, the bigger the difference in performance, the smaller the sample size needs to be. This means that we need fewer visitors and fewer conversions to choose the correct version if the difference in performance is big.

However, if the difference is too small, let’s say, 10%, we would need a lot more time, and a lot more visitors to be able to have a statistically significant test. That can become expensive and time-consuming, which is not ideal.

We also need to take external factors into consideration. Seasonality, and other external factors such as other marketing campaigns by the company or its competitors, changes in the law, and many other wild guesses on external situations, might change the number of visitors, their willingness to share their data, look for loans, etc.

Should you have any questions about any aspect of the project, I'd be happy to clarify.
