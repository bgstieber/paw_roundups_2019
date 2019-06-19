# Challenges in Recommender Systems at Twitter Scale - Bansal (@ash_bans or @ngiezhou)

## Notes

- Twitter is basically a large recommendation system
- Type of engine
    + Collaborative: unique advantage due to user behavior, easy to detect user similarity because users follow others
    + Content based: harder due to heterogeneity of tweets (document length, language and culture, multiple languages in tweets)
- What type of recommendations? user-user (people like you follow this person), user-item (people like you liked this tweet), item-item (people liking this tweet also liked this tweet)
- Twitter problem: short shelf life of products, so need to have the ability to refresh full recommendation engine every few days
    + How can you make this effieicnt?
- Analysis of problem
    + 2X2 matrix: number of items on rows, shelf life/churn on columns
- Techniques
    + Text tokenization, semantic graph, named entity recognition, wikid (wikification), embeddings
- Challenges: coverage (can't really look at all tweets, need to select subset with high relevance but low latency), diversity (varying recommendations across topic distributions), utility (how to measure engagement without an explicit "click"? user might just need to skim items without clicking on it), adaptability (how fast can system adapt, how can it adapt for users with low engagement), scalability (literally billions of users and hundreds of millions of tweets), user preference (explicit vs learned interests)

## Key Takeaways

- A lot of time spent formulating and defining the problem. Much consideration about specifics of the Twitter business model and its users.
- Timing considerations for tweets/user behavior
- Wasn't sure how applicable this was to many other business, but demonstrated the importance of fully examining the business problem and context
    + Twitter is surely rather unique in its challenges for building and scaling recommendation engines
- Working on shifting from following users to following topics or interests

## Other Details / Follow Up

Form factor?