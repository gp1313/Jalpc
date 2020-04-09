# Key Ideas in Statistics used in Retail Ecosystem

In this blog we will discuss key ideas in field of statistics with context of retail ecosystem.

Iets start by assuming a hypothetical retail store named "Bizom Store". As a brand we are interested in understanding two questions one, what are the attributes of this store and second what kind of business should brand expect from this store. Scope of this article is limited to the second question.

Let start discussing key ideas from statistics by applying them on the transaction data of this outlets    which brand already have with them.

# Mean, Median, Mode, Quantiles, IQR and Simpson's Paradox

### Mean, Median and Mode : What do they mean?

Mean - x1

Median - x2

Mode - x3

- x1 is the expected order quantity from this outlet. here the assumption is that all the orders in past were taken in very similar setting, i.e there was no external factors such as festive / holiday season or discount
- x2 is a quantity threshold such that 50% of orders are less than or equal to x2.
- x3 is the quantity ordered highest number of times

### Simpson's paradox : There is a tremendous amount of information / insights in your data but a lot can go wrong

- Lets look at two SKUs A and B transaction data for Bizom stores
- If we just look at mean order quantity value of both SKUs they both look to have similar importance, but if we dig in more we understand that's not true
- 

### Quantiles and IQR : The world of insights starts were the game of averages ends

- In order to get true picture of what kind of distribution the order quantity numbers follow, just the mean or the median are almost never enough.
- Quantile is one step ahead of median, in simple words quantile breaks down the data into two half using median and calculates median of two parts separately
- The idea seems simple but is very powerful (this is true for almost all concepts in statistics)
- 

# Cumulative Plots, Variance and Normal Curves

- First step of all the great expedition in data science : Have a first hand look of the data
    - Bar histogram of data
    - Spot the missing data
    - Visual changes after data clean up as sanity check
- Cumulative effect
    - Spot trends in order numbers
    - Bring in more relevance
    - If you remove primary, the best performing secondary is your potential primary
- Variance and standard deviation
    - Variation in your data
    - How much variation is explainable
    - How to reduce it?
- Data distribution and data sampling
    - In ideal world
    - In retail world
    - Randomness is your friend

# Hypothesis Testing Framework

- When to believe in numbers?
    - Null hypothesis
- Bayesian way of thinking
    - Make best guess possible using available information
    - Don't ignore the new data and update the best guess accordingly
- Experiment design
- How to best sample the data?
- Confidence intervals
- Hypothesis testing
- Type 1 and type 2 Errors
