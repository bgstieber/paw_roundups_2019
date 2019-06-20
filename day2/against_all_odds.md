# Against All Odds: The Slow, Startling Triumph of Reverend Bayes - Elder
 
## Notes 

- Bayesian approach: factoring in data outside of your system
    + example with early batting averages
    + James-Stein estimator
- Regression issues with multicollinearity
    + Pick variables using VIF
- Ridge regression to shrink coefficients _toward_ zero
    + See also LASSO and elastic net
- Borrowing strength
    + Get data from elsewhere, and hope that it helps you more than it hurts you
    + Expand where you're getting data from, which is especially helpful when dealing with small segments of data
- Case Study: SSA Disability Approval
    + Interesting what you can find in the data (fraud, human decision making, bribery)
    + Where do the models and label disagree?
    + Goal was to fast-track "easy" cases
        * How to handle free-text?
    + Non-zero initialization
        * Calculate predicted probability for each word, use Bayesian methods to shrink the estimate closer to the empirical mean (prior)
        * Not a lot of data -> close to prior, lots of data -> close to empirical
        * Used these predicted probabilities as features instead of the output from bag-of-words (one hot encoding)

 
## Key Takeaways 
 
- Further investigation in Bayesian methods is warranted
- Don't start from scratch, use information from outside your sample
    + Regression regularization
    + James-Stein
    + Borrowing Strength
    + Non-Zero Initialization (see Laplacian smoothing)
 
## Other Details / Follow Up 
 
 
