# Attribution-What Do We Want and What Can Be Done? - Haensel
 
## Notes 
 
- Touch points in a customer journey are paid
    + what is the value for each session
    + what is the profitability of the paid engagement
- There are various static attribution models
    + Last-Click, Last Non-Direct, Last Cookie Wins
        * easy to track, easy to understand, instant results
        * ignores prior touchpoints, no competitive advantage
    + First click
        * initial demand creation, easy to understand
        * ignores later touch points
        * attribution is much later than the cick events
        * requires good tracking and user-matching
    + Linear (all touchpoints get same value for attribution)
        * esay to understand, not ignoring touch-points
        * extrema and simple
    + Position based (mixing of first-click, last, and linear)
    + Time decay (linear with higher weights on recent sessions)
    + Rule based (collection of beliefs)
- Shapley value
    + Cooperative game thory
    + Calculates influence of a touchpoint by comparing conversion probability between two similar sets of customer journeys or touchpoint sequences
        * How does probability change depending on inclusion/exclusion of a certain channel?
- Markov Chains 
- What do we want?
    + Interaction between sessions
    + Performance/engagement within a session
- Measuring one specific session
    + What happened in the session?
    + What happened in prior? When?
    + What happened in follow-up? When?
- Customer interaction phases (three phases)
    + Initializer, holder, closer
- Sessions are then categorized into the three phases, but assigned using fuzzy logic
    + Get scores based on the I,H,C scores and determine attribution impact
 
## Key Takeaways 
 
- Picking a good objective function, measure of success, and loss function is paramount in data science
- Extreme and simple solutions are often not best, but still get a lot of traction
- Adoption
    + Define targets on main KPIs
    + Connect insights with actions
    + Monitor actions and performance relative to the targets
- Very specific problem they're trying to solve, came up with a new approach

## Other Details / Follow Up 
 
 
