# What result did the Author try to reach?
In this paper, the authors proved that the 1-NN decision rule is mathematically admissible, meaning there are certain scenarios where it will outperform a $k$-NN ($k>1$) rule. The Author concluded that: The nearest point include a half of available information of the unclassified point. This means when you have an **infinite amount of data**, you have a very powerful prediction with the absolute lowest possibility of error R* by analyze all of them perfectly, but if you don't want to analyze all of them, you can only incur maximum 2R* possibility of error by just pick the closest point and copy its classification. 

# What were the key elements of the approach?
Using standard probability theory, they set up an equation comparing the 1-NN error against the perfect Bayes error. They proved algebraically that the probability of the 1-NN rule making a mistake can never mathematically stretch beyond twice the baseline perfect error rate ($2R^*$).

# What can you use yourself?
However, in real case, it's really hard to have an infinite amount of data. Therefore, we often use k-NN approach and find the optimal k by Cross-Validation
