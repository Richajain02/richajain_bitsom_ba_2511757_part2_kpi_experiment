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

