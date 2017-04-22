DATA606 Linear Regression Presentation
========================================================
author: Kyle Gilde
date: 4/20/2017
width: 1500
height: 1080

Linear Regression & Murder!
========================================================

![](http://img13.deviantart.net/43b8/i/2006/291/6/b/464_by_blood__stock.jpg)


7.29 Murders and Poverty, Part I.
========================================================
 
The following regression output is for predicting annual murders per million from the percentage living in poverty in a random sample of 20 metropolitan areas.

![](https://raw.githubusercontent.com/kylegilde/D606-Stats/master/lmoutput.PNG)

5-Part Question
========================================================
a) Write out the linear model.

b) Interpret the intercept.

c) Interpret the slope.

d) Interpret $R^2$.

e) Calculate the correlation coecient.


(a) Write out the linear model.
========================================================

A linear model is expressed as 
$y = {\beta}_{1}x + {\beta}_{0}$
where ${\beta}_{1}$ is the slope of the line
and ${\beta}_{0}$ is the line's y-intercept.

![](https://raw.githubusercontent.com/kylegilde/D606-Stats/master/lmoutput.PNG)

From the Estimate column of the regression output, we know that
${\beta}_{0} = -29.901$ and is the line's y-intercept.
${\beta}_{1} = 2.559$ and is the slope of the line. 

Consequently, the linear model for the murder rate as a function of the poverty rate is expressed as
$\widehat{murder} = -29.901 + 2.559*{poverty\%}$

Conditions for Least Squares Line
========================================================
Before continuing, let's stop & check to the best of our ability given that we only have the scatter plot and not the raw data that the conditions for least-squares regression have been met.


![](https://raw.githubusercontent.com/kylegilde/D606-Stats/master/lmplot.PNG)

Check of Conditions
========================================================

1. Linearity: The points in the plot do show a linear trend. 
2. Nearly normal residuals: From the scatter plot, we don't see any outlying points. 
3. Homoscedasticity (aka constant variability): Having only the scatter plot, the points appear to have constant variability.
4. Independent observations: The data are from a random sample, and they are not from a time series.
![](https://raw.githubusercontent.com/kylegilde/D606-Stats/master/lmplot.PNG)
(b) Interpret the intercept.
========================================================

The expected annual murders per million in metropolitan areas with no poverty is $-29.901$.

However, since this is not a meaningful value, it merely serves to adjust the height of the regression line.


(c) Interpret the slope.
========================================================

Since ${b}_{1}$ is positive, we would expect a positive relationship between the variables.

For each additional $1\%$ increase in the poverty rate, we would expect the annual murders per million to increase on average by 2.6.

As always, we should remember that correlation is not causation.


(d) Interpret R-Squared.
========================================================

In our model, $R^2$ is $70.52\%$, which means that the model's least-squares line accounts for approximately $71\%$ of the variation in the annual murders per million. 


(e) Calculate the correlation coefficient.
========================================================

The correlation coefficient $R$ can be calculated by taking the square root of $R^2$:

```r
r2 <- .7052
paste("R is approximately", round(sqrt(r2), 2))
```

```
[1] "R is approximately 0.84"
```


THE END!
