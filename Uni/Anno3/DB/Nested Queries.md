Compare attributes with results from sub-queries, also using [[Exists]]. Only usable for WHERE queries.

Less declarative but sometimes more readable. Can be combined with non-nested queries.

Sub-queries cannot express set operations, although this limitation is not significative. We need a different way to compare

To solve the homogeneity problem, one can formulate nested queries using ANY, ALL or IN with a comparison operator. These operators can be negated with NOT before. 
There are come intesting equivalences between operators

The inner query is performed for every tuple in the outer query, this can be avoided only by using views.

## Visibility
We can't see outer nested values. It's only possible to view the result of the nearest nested query. Keep this in mind to decide if nesting is useful or not.

