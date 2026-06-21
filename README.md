# Onboarding and Activation Campaign

## Business Problem Summary

The company launched a new onboarding and activation campaign to improve user conversion and early engagement. Users were randomly assigned to either a Control group (existing onboarding experience) or a Treatment group (new onboarding experience).

The key business decision is whether the Treatment experience should be rolled out to all users.

This decision impacts -  
1. Product  
2. Growth
3. Marketing
4. Customer Success teams
5. Future users of the platform.

The primary metric that should improve is the Paid Conversion Rate, measured using the `converted_to_paid` field.

Potential risks include increased support burden and customer dissatisfaction. These risks will be monitored using guardrail metrics such as `support_tickets_30d` and `refund_requested`.

Before recommending rollout, evidence must show that the Treatment group improves conversion while maintaining acceptable performance on guardrail metrics.

## Dataset Used

File: `campaign_experiment_data.xlsx`

Key fields:

* experiment_group
* started_trial
* completed_onboarding
* converted_to_paid
* revenue_30d
* support_tickets_30d
* refund_requested
* engagement_score

## Tools Used

* Microsoft Excel
* Pivot Tables
* Statistical Analysis
* Data Validation

## Success Metrics

### Primary Metric

* Paid Conversion Rate (`converted_to_paid`)

### Secondary Metrics

* Trial Start Rate (`started_trial`)
* Onboarding Completion Rate (`completed_onboarding`)
* Engagement Score (`engagement_score`)
* Revenue per User (`revenue_30d`)

### Guardrail Metrics

* Refund Request Rate (`refund_requested`)
* Average Support Tickets (`support_tickets_30d`)

## Evidence Required

The Treatment should be recommended only if:

1. Conversion rate improves meaningfully.
2. Results are statistically significant.
3. Refund rates do not increase materially.
4. Support ticket volume remains acceptable.
5. Revenue and engagement improve or remain stable.

# North Star Metric

## Selected North Star Metric

Paid Conversion Rate (`converted_to_paid`)

## Why This Is the Main Success Metric

The primary objective of the onboarding and activation campaign is to increase the number of users who become paying subscribers. The `converted_to_paid` metric directly measures whether users successfully move from onboarding to becoming paying customers.

Because the company operates a subscription-based business model, paid conversion is the strongest indicator of campaign success and long-term revenue growth.

## Why Other Metrics Are Supporting Metrics

The following metrics are important but serve as supporting indicators:

* `started_trial` measures initial interest but does not guarantee revenue.
* `completed_onboarding` measures onboarding success but not customer conversion.
* `engagement_score` measures user activity but does not directly generate revenue.
* `revenue_30d` is valuable but occurs after conversion and can be influenced by other factors.

These metrics help explain user behavior but do not directly represent the primary business objective.

## Connection to Business Growth

An increase in paid conversion rate directly contributes to:

* Higher subscription revenue
* Increased customer acquisition efficiency
* Better return on marketing investment
* Sustainable business growth

If more users convert to paid subscriptions, the company generates greater recurring revenue and improves overall business performance.

## Risks of Optimizing This Metric Blindly

Focusing only on paid conversion rate may create unintended consequences.

Potential risks include:

* Increased refund requests from users who were pressured into converting.
* Higher support ticket volume due to confusion during onboarding.
* Lower customer satisfaction.
* Reduced long-term retention despite short-term conversion gains.

Therefore, paid conversion rate should be evaluated alongside guardrail metrics such as refund rate and support tickets before making a rollout decision.

## Data Quality Checks

### Missing Values

The dataset was reviewed for missing values before conducting the experiment analysis.

| Column Name      | Missing Values |
| ---------------- | -------------: |
| device_type      |             18 |
| traffic_source   |             24 |
| engagement_score |             14 |
| days_to_convert  |           1336 |

All other columns contained no missing values.

**Note:** The large number of missing values in `days_to_convert` is expected because users who did not convert to a paid subscription do not have a conversion date.

---

### Group Count Validation

| Experiment Group | User Count |
| ---------------- | ---------: |
| Control          |        693 |
| Treatment        |        715 |
| Total            |       1408 |

The Control and Treatment groups were reviewed and found to be reasonably balanced for comparison.

---

### Duplicate User ID Check

| Check                          | Count |
| ------------------------------ | ----: |
| Duplicate User IDs (Count > 1) |    16 |

Duplicate user IDs were identified using COUNTIF() and flagged for review before analysis.

---

### Invalid Binary Value Check

The following binary fields were reviewed:

* visited_landing_page
* started_trial
* completed_onboarding
* converted_to_paid
* refund_requested

Expected values: **0 or 1**

No invalid binary values were identified.

---

### Revenue Outlier Check

Revenue values were reviewed for potential outliers.

| Metric          | Value   |
| --------------- | ------- |
| Q1 Revenue      | 0       |
| Q3 Revenue      | 0       |
| Maximum Revenue | 8610.72 |

Because the majority of users generated zero revenue, the standard IQR outlier detection method was not appropriate. Revenue values were manually reviewed and retained as valid observations.

---

### Segment Distribution Check

Segment distributions were reviewed across:

* Region
* Device Type
* Traffic Source
* Plan Type

The distributions were examined to ensure that the Control and Treatment groups were reasonably balanced before performing the A/B test analysis.



