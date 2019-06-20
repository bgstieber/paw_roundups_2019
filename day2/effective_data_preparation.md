# Effective Data Preparation - Nisbet
 
## Notes 

- Businesses are just big human ecosystems
- Must approach predictive analysis as a _systems activity_
    + CRISP-DM
- Over 80% of time was consumed with data preparation, not modeling
    + Aggregation, data coding, missing data, data type, deriving new variables
- Training in data prep
    + Ad-hoc, under-appreciated, under-managed, misunderstood as being a sequence of tasks rather than being an interactive system of operations
- Data prep system: need to understand its context and that it is very interconnected (small changes in one part can greatly affect others)
- Data sets are complex systems
    + Some aspects of information are rooted in details, some aspects are greater than the sum of its parts
    + Need to blend top-down and bottum-up approaches to information discovery
- Three data preparation questions
    + How important is new variable derivation in this process?
    + How much of each data preparation activity can we automate safely?
        * Some can and some cannot
    + How can you build a data preparation training program?
- Data integration
    + Data can be: stored in different locations, formats, different coding systems, different levels of aggregation/granularity
    + Must be intregated consistently
- Data quality
    + Need to find errors (there will be errors) and fix them (renaming, data type, data coding)
    + Filling missing values
- Data conditioning
    + Operations performed on all variables
        * Standardization of real numbers
        * Balancing of data sets with rare targets
            - Over-sampling (SMOTE) or under-sampling (and others...RL?)
- Data enhancement
    + Many of the most predictive variables are those you derive yourself
 
## Key Takeaways 
 
- Spending 60-90% of time on data preparation seems like a problem we can't solve. Just can get better at doing it.
- Data prep is a system of operations, not a linear/sequential process
- A lot of the concepts presented were similar to the tidy data framework and the 12 rules of sharing data in spreadsheets
- While doing data prep, do some preliminary modeling along the way
    + Requires having the target variable defined, and helps with feature selection and engineering, as well as sampling techniques
- Feature engineering/creation is incredibly important
    + Best variables are often the ones you derive yourself
    + Ask stakeholders for their "shopping list" of variables
        * They don't have to give an explicit definition, and you'll probabaly have to create proxies
- How to reduce the % of time spent in data preparation? Automation
    + Where should the automation happen?
 
## Other Details / Follow Up 
 
Should we embrace the 60-90% or try to change it?

Bob Nisbet, he's written some books, might be worth checking out