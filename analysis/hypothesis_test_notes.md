# Hypothesis Testing Notes

## Metric Tested

Paid Conversion Rate

## Null Hypothesis (H0)

The paid conversion rate of the Treatment group is equal to or lower than the paid conversion rate of the Control group.

## Alternative Hypothesis (H1)

The paid conversion rate of the Treatment group is higher than the paid conversion rate of the Control group.

## Test Method

A/B Test (Control vs Treatment)

## Test Type

One-tailed Two-Proportion Z-Test

## Significance Level

α = 0.05

## Reason for Choosing This Metric

Paid Conversion Rate is the North Star Metric because it directly measures business growth and subscription revenue.

## Decision Rule

If p-value < 0.05:
Reject the null hypothesis.

If p-value ≥ 0.05:
Fail to reject the null hypothesis.

## Business Interpretation

A statistically significant increase in paid conversion rate would support rolling out the new onboarding experience to all users.

# Hypothesis Test Results

## Test Inputs

Control Group:

* Users = 693
* Conversions = 22
* Conversion Rate = 3.17%

Treatment Group:

* Users = 715
* Conversions = 50
* Conversion Rate = 6.99%

## Test Method

A/B Test (Control vs Treatment)

## Statistical Test

Two-Sample T-Test Assuming Unequal Variances

## Results

* t-Statistic = -3.2801
* One-Tail P-Value = 0.000533

## Decision Rule

Significance Level (α) = 0.05

If p-value < 0.05:
Reject the Null Hypothesis.

If p-value ≥ 0.05:
Fail to Reject the Null Hypothesis.

## Decision

Since the p-value (0.000533) is less than 0.05, the Null Hypothesis is rejected.

## Business Interpretation

The Treatment onboarding experience produced a statistically significant increase in paid conversion rate compared with the Control experience.

Paid conversion increased from 3.17% in the Control group to 6.99% in the Treatment group.

## Recommendation

Roll out the Treatment onboarding experience to a broader user population while continuing to monitor refund rate, support ticket rate, and engagement metrics as guardrail measures.



