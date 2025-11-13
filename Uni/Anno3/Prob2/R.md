Suite of pre-implemented functions, use them!

Gamma distribution is a continuous distribution of positive random variables. 

Use `rexp`, `rgamma`, ect. for preloaded distributions (you can search for the name in the help, selecting from a set of 4 different funcitons, d for density, p for probability, q to get value from probability, r for random selections).

How to sample from *any* distribution? For example, in Baeysian statistics we don't know the shape of the posterior. 

To view data, we can use the `hist` function for a histogram. If we want densities, we can use `freq = FALSE` (this is what we'll use). This is actually an estimator of the distribution of the random variable. We can also use `curve`, which is also an estimator, but a smooth one. 

Be careful about the size of the plots (don't be tricked). Height of the histogram estimates the density, but we can't tell if they're independent. The second plot is used for this case, plotting points in a 2d space with slightly shifted values. The acf (auto correlation funciton) plot measures correlation of a time series, by taking a sequence and shifting it many times, recording the correlation of a vector with itself. The x axis indicates the "lag", so at 0 it's 1 (correlation between two identical vectors). If our values are independent, we should see no correlation (close to 0).

By setting the seed, we can fix the pseudo-random sequence. 