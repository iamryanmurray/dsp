[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

```python

import numpy as np
import nsfg

preg = nsfg.ReadFemPreg()
live = preg[preg.outcome == 1]

firsts = live[live.birthord == 1]
others = live[live.birthord != 1]

def CohenEffectSize(group1, group2):
    #function from thinkstats ipynb
    diff = abs(group1.mean(),group2.mean())
    
    var1 = group1.var()
    var2 = group2.var()
    n1,n2 = len(group1),len(group2)
    
    pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
    d = diff / np.sqrt(pooled_var)
    return d



length_d = CohenEffectSize(firsts.prglngth,others.prglngth)

totalwgt_lb_d = CohenEffectSize(firsts.totalwgt_lb,others.totalwgt_lb)

print(length_d)
print(totalwgt_lb_d)

```


The Cohen effect size for the difference in weight (0.09) is approximately a factor of three larger than the difference in pregnancy length (0.03).  However both of these differences are smaller than 0.2, so these differences, while statistically significant, are trivial.  First pregnancies are longer by 0.08 weeks, and subsequent babies have higher birth weights by 0.1 lb.
