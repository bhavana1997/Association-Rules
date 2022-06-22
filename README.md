# Association-Rules

Association rule learning is a rule-based machine learning method for discovering interesting relations between variables in large databases. ... In contrast with sequence mining, association rule learning typically does not consider the order of items either within a transaction or across transactions.

Apriori is part of the association rule learning algorithms, which sit under the unsupervised branch of Machine Learning.Apriori does not require us to provide a target variable for the model. Instead, the algorithm identifies relationships between data points subject to our specified constraints.

Support
The first step for us and the algorithm is to find frequently bought items. It is a straightforward calculation that is based on frequency.
Support(A) = Transactions(A) / Total Transactions

Confidence
Now that we have identified frequently bought items let’s calculate confidence. This will tell us how confident (based on our data) we can be that an item will be purchased, given that another item has been purchased.
Confidence(A→B) = Probability(A & B) / Support(A)

Lift
Given that different items are bought at different frequencies, how do we know that eggs and bacon really do have a strong association, and how do we measure it? You will be glad to hear that we have a way to evaluate this objectively using lift.
There are multiple ways to express the formula to calculate lift.
1) Lift(A→B) = Probability(A & B) / (Support(A) * Support(B))
2) Lift(A→B) = Confidence(A & B) / Support(B)



# Steps Involved in Apriori Algorithm
1. Set a minimum value for support and confidence. This means that we are only interested in finding rules for the items that have certain default existence (e.g. support) and have a minimum value for co-occurrence with other items (e.g. confidence).
2. Extract all the subsets having higher value of support than minimum threshold.
3. Select all the rules from the subsets with confidence value higher than minimum threshold.
4. Order the rules by descending order of Lift.
