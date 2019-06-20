# Q&A: Ask Dean and Karl Anything (about Best Practices) - Abbott and Rexer
 
## Notes 

- Worst practices: improper following through with the deployment of models
    + Mislabeled deciles (should have gone to deciles 9 and 10, but went to 1 and 2 instead) leading to a poorly performing campaign
    + Explaining the model in complex terms (need to communicate ideas in ways stakeholders can understand and explain to clients)
- Balancing accuracy, interpretability, and deploy-ability (and how will you explain it?)
    + Build decision trees to predict the neural network predictions. Shows how _some_ of what the NN is doing
    + Show business impact of simple model first, then show how more complicated models perform (and hopefully beat the simple model)
 
## Key Takeaways 

- Best practices are a good place to start, but not the right place to end
- Logit models, with solid data and good feature engineering can sometimes be the best performing model within some constraints
    + Even if the requirement is for a logistic regression, fit more complicated models and see what the "accuracy ceiling" is
    + What are key reasons scores are different between models?
        * Fit regression trying to predict score differences
 
## Other Details / Follow Up 
 
 
