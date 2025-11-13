1. Simulation  ([[Sampling]])
2. Integration ([[Expectations]])
3. Optimisation

Called "Montecarlo" (casino) because of its use of randomly generated numbers. These are used to solve something that isn't random.

### Example
Given a field with a fixed area (eg. 20km^2) and a lake inside of it with an irregular shape with its own area.

How do we estimate (compute/measure is impossible - Coastline Paradox) the area of the lake?
	Note: the area of the lake isn't random, but injecting randomness makes it much easier to solve.

We can shoot cannon balls into the field **at random**, recording if it hit water or not. By repeating this process, we get a long string of binary values which were **randomly generated** (in a weird way).

We can now define a random variable $X$  (in this case a Bernoulli) with $n$ recorded outcomes $X_1,...,X_n$ 

Seen as the area of the lake and field don't change, the probability of hitting water remains the same. So for each random variable $P(X_1=1) = ... = P(X_n=1)$, they are **identically distributed**. 

Even if we keep hitting grass in one direction, we can't decide to move the cannon based on this information, because this wouldn't be random and it would cause dependence between the n random variables, which need to be iid (independent identically distributed). 

Given $A=$"hit water", $P(A) \alpha \frac{\text{Area Lake}}{\text{Area Field}}$.
So if we want to estimate the area of the lake, we can multiply the field area by the probability of hitting water. The measurement has become probabilistic.

To find such probability, we can find the avg. value of $X$ (sample proportion/mean). The more samples we have, the more precise the measurement (thanks to CLT).