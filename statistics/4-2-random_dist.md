[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

```python

import numpy as np
import thinkstats2
import thinkplot


rand = np.random.random_sample((1000,))

#PMF
rand_pmf = thinkstats2.pmf(rand)
thinkplot.Hist(rand_pmf,width=0.01)

#CDF
rand_cdf = thinkstats2.cdf(rand)
thinkplot.Cdf(rand_cdf)

```


The distributions suggest that the numpy random.random function does generate a uniform distribution.

In the PMF, each value is equally likely to appear, giving a "square distribution", while in the CDF, we see a linear distribution, increasing in probability as the value increases.
