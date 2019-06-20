# What are Analytic Operations and What are Some Frameworks to Improve Them - Grossman
 
## Notes 
 
Frameworks

- Develop, Deploy, and Extract (DDE)
    + Develop: build the model
    + Deploying: how is the model integrated? existing system or stood up as a separate system? what does the model do?
        * How do you deploy?
        * How do you detect drift and update?
    + Extract: does it replace something? double-check/QC on existing system? handle difficult cases?
        * What actions are associated with a model and what value do they provide?
- Analytic Diamond
- SAM (Score - Action - Measures)
    + Full picture of model infrastructure
        * Models produce scores
        * Scores have actions (or should)
        * Actions have measures
- Segment by Score, Action by Cell (SSAC)

Case Studies

- IBM Oncology
    + Watson won Jeopardy
    + Tried to beat cancer, but didn't add much value 
    + Got audited
    + A major failure on many accounts (cost tens of billions of dollars with little value returned)
- Obama for America
    + Three models: support (do you support O?), persuasion (can you be persuaded to vote for O?), turnout (will you vote?)
    + Actions were tricky
    + Utilized the segment by score, action by cell approach

- Understand the differences between
    + model builders, model deployers, product team responsible for creating actions
 
## Key Takeaways 

- Four frameworks are worth paying attention to
- SAM framework is also important
- Lot of detail in this quick talk about analytics/data science model management
- Models should be packaged in a way that's consistent with IT expectations
 
## Other Details / Follow Up 
 
Competitive Strategy - Michael E. Porter