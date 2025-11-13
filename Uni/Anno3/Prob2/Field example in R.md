Matrix with ones (lake) and zeros (field). We can plot this now. We then randomly select a matrix element and record if it's a 0 or 1. 

Note that we're using discrete values. We can sample using the `sample` function, with which we can define the set of tuples to sample from, the amount, with or without replacement (in our case the former with `replace=TRUE`).

The accuracy depends on the amount of random variables whose outcome we can observe, at a cost to computational time. 

To define a function, the correct syntax is:
Name <- function(parameters)