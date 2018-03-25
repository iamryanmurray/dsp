[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

```python
import scipy

mu = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mu, scale=sigma)

#Change heights from inch to cm
h_min = 177.8
h_max = 185.42


#We want the CDF for the max - CDF for min:

range = dist.cdf(h_max) - dist.cdf(h_min)

print(range)

```


Approximately 34% of the US male population is between 5'10" and 6'1".
