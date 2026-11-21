# Recommendation Memo — Customer Segmentation and Churn-Risk Prioritisation

**To:** Customer Retention Team  
**Subject:** Prioritising customer outreach using an explainable rule-based score  
**Dataset:** 15 synthetic customer records

## Decision
Prioritise proactive review of customers on Month-to-Month contracts, especially those with early tenure and higher support-ticket counts. Resolve service friction first; discuss longer-term plans or tailored retention options only after understanding the customer's concern.

## Method
A transparent 0–8 point score:
- Month-to-Month contract: +3
- Tenure of 12 months or less: +2
- At least 4 support tickets: +2
- Monthly charges of INR 80 or more: +1

Risk tiers: Low 0–2; Medium 3–4; High 5–8. Observed `Churn` was not used to calculate scores.

## Observed results
- High-priority customers: 6 customers; 6 labelled churned.
- Contract watchlist: 1 customer; 1 labelled churned.
- Stable contracted customers: 8 customers; 8 labelled retained.

These are descriptive in-sample observations from 15 synthetic records, not proof of future predictive accuracy.

## Recommended actions
1. **High-priority:** review support history, resolve open issues and offer a relevant retention conversation. Measure contact rate, issue resolution and subsequent retention.
2. **Contract watchlist:** conduct a short service check-in and explain longer-contract benefits without pressure. Measure response and renewal conversion.
3. **Stable contracted:** maintain service quality, send renewal reminders and monitor new support-ticket spikes. Measure renewal and complaint rates.

## Limitations and next measurement
The sample is very small and synthetic. Weights and thresholds are heuristic, not learned probabilities. Product usage, payment failures, satisfaction and time-based engagement trends are unavailable. Test the rules on a larger later-period dataset and compare contacted customers with a comparable holdout group.
