[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

```python

%matplotlib inline

import numpy as np

import nsfg
import first
import thinkstats2
import thinkplot
resp = nsfg.ReadFemResp()

dist = resp.numkdhh
pmf = thinkstats2.Pmf(dist, label='numkdhh')
thinkplot.Hist(pmf)
thinkplot.Config(xlabel='Number of Children', ylabel='Pmf')

bias_dist = dist[dist != 0]
pmf = thinkstats2.Pmf(bias_dist, label='numkdhh')
thinkplot.Hist(pmf)
thinkplot.Config(xlabel='Number of Children', ylabel='Pmf')


print(np.mean(dist))
print(np.mean(bias_dist))
```
