# Improving CLV Predictions - Dean Abbott

## Notes

 - Clients not interested in lifetime value (although that's what they said), but more focused on "immediate" customer value. What will they be doing in the next 60-90 days?
 - Difference between propensity and lifetime value: __dollars__
     + this is what retailers think in: dollars not likelihood

__Statistical Perspective__

 - Framing the CLV question
     + when do purchases occur: continuous (occur at any time) vs. discrete (occur at fixed intervals)
     + what type of purchase: contractual (know when customer defects) vs non-contractual (don't know when customer defects)
 - once it's framed, you can assume a distribution of customer behavior on top of other distributions (I think this is what has been missing in our work thus far on Lively calculation)
     + purchases: poisson
     + time to next purchase: exponential
 - Big idea: assume a distribution on Recency (time to next purchase), Frequency (# of purchases in a time period), and Monetary ($ of purchases in a time period)
     + Target: number of expected purchases, value of expected purchases
 - CLV = number of expected purchases * value of expected purchase
 - Bayesian models
 - R package: __`BTYD`__

__Non-parametric/ML Perspective__

- ML: not constrained to assumed distributions or transactional inputs, and can customize predicted customer value to a time window of interest
    + how does accuracy depend on time window?
- Data: one row per customer per transaction date, look forward to see if they made another purchase
    + transaction history, visit history, engagement scores (probably proprietary thing, not like NP engagement score)
        * Lot of time-dependent feature engineering
    + trying to predict customer value in next 30 days
- Randomly assign __customer__ to train/test to avoid serial correlation
- Used random forest to do regression
- Don't explain in terms of R^2 or mean absolute error
- Made strong case that predicting value needs to incorporate visit/session data instead of just transactional data
    + This is an issue with the statistical/parametric approach which heavily relies on transactional data
- How to use:
    + high near-term CLV shoppers should be omitted from promotions to maintain margin
    + if shoppers have higher near-term CLV, but do not make purchase, re-engage
- Don't be afraid to go under-the-hood for RF model
    + Build a decision tree to predict the random forest predictions (predictions on declie bin)
    + Building a model in this way gives evidence on how top or bottom deciles separate themselves


## Key Takeaways

- Statistical approach requires assuming distribution for variables of interest. Also need some good data, might not have enough to do decent likelihood maximization, Bayesian optimization approach
- Communicate in terms of business value
    + Showed confusion matrix (frequency, column percentage, and row percentage) with Binned Predicted Values on rows and Binned Actual Values on columns (binning schemes differed)
- ML approach might make more sense for this context, especially if the data isn't too big, or if not a lot of repeats
- Investigate RF model using decision tree
- Statistical vs ML
    + Normal assumptions hold for statistics
    + ML flexible and can incorporate features not directly related to transactional data
- Look-ahead models need as much data as you're trying to analyze, need to be concerned about model drift

## Other Details / Follow Up

Might try and reach out to Dean Abbott about model drift/longer lookahead

Use similar framework for upgrade/downgrade model