# Recommendation Memo

## Objective

Determine whether the new onboarding and activation campaign should be launched to all users.

## Business Question

Does the Treatment onboarding experience generate higher paid-user conversion than the existing onboarding experience?

## Primary Success Metric

* Paid Conversion Rate (`converted_to_paid`)

## Supporting Metrics

* Trial Start Rate (`started_trial`)
* Onboarding Completion Rate (`completed_onboarding`)
* Engagement Score (`engagement_score`)
* Revenue per User (`revenue_30d`)

## Guardrail Metrics

* Refund Request Rate (`refund_requested`)
* Support Tickets within 30 Days (`support_tickets_30d`)

## Decision Criteria

Recommend rollout if:

* Treatment conversion rate exceeds Control conversion rate.
* Statistical testing confirms the difference is significant.
* No major increase occurs in refund requests.
* Support ticket volume remains within acceptable limits.
* Business impact is positive overall.

## Recommendation Approach

The final recommendation will be based on comparison of Control and Treatment groups, statistical significance testing, and review of all guardrail metrics before approving a full rollout.

## North Star Metrics

North Star Metric: Paid Conversion Rate (converted_to_paid).  

This metric was selected because it directly measures the campaign's impact on subscription growth and revenue generation. Supporting metrics and guardrail metrics were also evaluated to ensure that conversion improvements did not negatively affect user experience.


