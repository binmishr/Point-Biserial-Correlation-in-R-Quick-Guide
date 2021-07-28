# Point-Biserial-Correlation-in-R-Quick-Guide

Point Biserial correlation in R, What do you understand by biserial correlation?

In some situations in which one variable is dichotomous according to some qualitative factor and another variable is numeric according to some quantitative variate. In this kind of situation’s person correlation coefficient is not appropriate. Hence a measure of correlation is known as biserial correlation.

Significance of Spearman’s Rank Correlation »
Assumptions

The major assumptions made for biserial correlation are

    Y is almost normally distributed.
    The regression Y on X is linear
    The mean value of Y in the minor or smaller category as specified by X lies on the regression lines.

Basically, It is used to measure the relationship between a binary variable and a continuous variable.

As usual, the point-biserial correlation coefficient measures a value between -1 and 1.

    -1 indicates a perfectly negative correlation
    0 indicates no correlation
    1 indicates a perfectly positive correlation

This tutorial describes how to calculate the point-biserial correlation between two variables in R.

Correlation Analysis Different Types of Plots in R »
Example: Point-Biserial Correlation in R

Let’s create two vectors x and y. x as binary variable and y as continuous variable

x <- c(0, 0, 1, 1, 0, 1, 1, 0, 1, 1, 0)
y <- c(10, 18, 12, 14, 10, 22, 25, 15, 19, 18, 10)

cor.test() function is used for the point-biserial calculation.

cor.test( y,x)

Pearson’s product-moment correlation

data:  x and y
t = 2.1625, df = 9, p-value = 0.05883
alternative hypothesis: true correlation is not equal to 0
95 percent confidence interval:
 -0.02329718  0.87699529
sample estimates:
      cor
0.5847499

The correlation value is 0.58 and it is significant at 90%.

How to Calculate Partial Correlation coefficient in R-Quick Guide »
Inference

A significant positive correlation was observed between x and y (p<0.1).

In another case, you can try package ltm

library(ltm)
biserial.cor(y, x, use = c("all.obs"), level = 2)
0.5847499

Conclusion

From the output, we can observe that the point-biserial correlation coefficient is 0.58 and it is significant at 90% significance level.
