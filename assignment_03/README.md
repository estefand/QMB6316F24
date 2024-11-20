# Assignment 3

Following the instructions in the document ```QMB6316_assignment_03.pdf``` above, 
enter your responses in the code blocks shown below.


In this exercise, we will follow an approach different than that taken in class. 
We will first estimate a model with our choices of functional form, then consider exclusions of insignificant variables from the full model. 
Note that this approach allows for inclusion of possibly irrelevant variables and avoids excluding any relevant variables. 


At each stage, use the best model that you have found so far, 
incorporating the findings from the answer to the previous question.




a. Estimate a regression model that uses all available variables, 
except for the indicator for an enclosed cab.
	Make sure to choose a reasonable transformation of the dependent variable, 
	such as the logarithmic transformation, if necessary.
	
```
    saleID        saleprice           age           enghours      
 Min.   :101.0   Min.   :  1500   Min.   : 2.00   Min.   :    1.0  
 1st Qu.:169.8   1st Qu.:  7750   1st Qu.: 7.00   1st Qu.:  777.2  
 Median :238.5   Median : 12000   Median :15.00   Median : 2398.0  
 Mean   :238.5   Mean   : 20747   Mean   :15.91   Mean   : 3530.2  
 3rd Qu.:307.2   3rd Qu.: 20925   3rd Qu.:24.00   3rd Qu.: 5409.8  
 Max.   :376.0   Max.   :200000   Max.   :33.00   Max.   :18744.0  
   johndeere          spring           summer           winter      
 Min.   :0.0000   Min.   :0.0000   Min.   :0.0000   Min.   :0.0000  
 1st Qu.:0.0000   1st Qu.:0.0000   1st Qu.:0.0000   1st Qu.:0.0000  
 Median :0.0000   Median :0.0000   Median :0.0000   Median :0.0000  
 Mean   :0.1413   Mean   :0.2246   Mean   :0.2319   Mean   :0.1703  
 3rd Qu.:0.0000   3rd Qu.:0.0000   3rd Qu.:0.0000   3rd Qu.:0.0000  
 Max.   :1.0000   Max.   :1.0000   Max.   :1.0000   Max.   :1.0000  

```

Does this seem to be a reasonable model, as opposed to using average tractor prices? 
	That is, is the R-squared or the R-bar-squared reasonably high?

```
Call:
lm(formula = log(saleprice) ~ age + enghours + johndeere + spring + 
    summer + winter, data = tractor_sales)

Residuals:
     Min       1Q   Median       3Q      Max 
-2.19146 -0.54194 -0.02331  0.49336  2.15617 

Coefficients:
              Estimate Std. Error t value Pr(>|t|)    
(Intercept)  1.004e+01  1.105e-01  90.846  < 2e-16 ***
age         -5.491e-02  5.818e-03  -9.438  < 2e-16 ***
enghours     7.443e-05  1.652e-05   4.505  9.9e-06 ***
johndeere    5.445e-02  1.345e-01   0.405    0.686    
spring       1.938e-01  1.243e-01   1.559    0.120    
summer      -6.316e-02  1.228e-01  -0.514    0.607    
winter       1.088e-01  1.365e-01   0.797    0.426    
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 0.7705 on 269 degrees of freedom
Multiple R-squared:  0.2648,	Adjusted R-squared:  0.2484 
F-statistic: 16.15 on 6 and 269 DF,  p-value: 7.206e-16



```


b. Which variables seem to help explain used tractor prices? 
	Which have positive and negative relationships with tractor prices?
	Did you find any variables that do not have statistically significant coefficients under this specification?

```
Enter your response here.



```



c. Before making any reductions to your model, revise the model specification first
	by considering nonlinear specifications.
	A used tractor dealer tells you that overpowered used tractors are hard to sell, since they consume more fuel. 
      Tractor prices often increase with horsepower, up to a point, but beyond that they decrease. 
      To incorporate this advice, you create and include a variable for squared horsepower and include that in a new regression model. 
      

```
Enter your regression results here.



```


  c.i) Hypothesize the signs for the coefficients on horsepower 
	under this scenario. 
		What should be the sign of the coefficient for horsepower? 
		What sign do you expect for squared horsepower?
      
```
Enter your response here.


```

  c.ii) Perform 1-sided t-tests of the hypotheses for each of the horsepower coefficients. 
That is, are the t-statistics higher than 1.96, with the same sign as you hypothesized?

```

Enter your response here.
Use the coefficients from the regression output for this model to draw your conclusions.



```

  c.iii) Compare the model with or without the quadratic functional form for horsepower.
            Which model do you recommend? 
		Be sure to cite evidence to support your choice. 
		Specifically, check the four specification criteria: 
		statistical significant $t$-statistics, 
		an increase in R-squared, 
		a good theoretical justification, and 
		no large change in the other coefficients.

```
Enter your response here.



```


d. Again, use the best model that results from the answer to the previous question to address further questions.
	Use the model you have so far to test that the time of year has no effect on the sale of tractors.
	That is, test whether the t-statistics on the seasonal indicators are statistical significant. 
	Is there evidence that tractor prices follow a seasonal pattern? 

```
Enter your response here.
Use the coefficients from the regression output for this model to draw your conclusions.



```
	
	
e. Finally, consider another modification to your model. 
	Some say that John Deere tractors hold their value longer than other tractors. 
      This raises the question of whether an additional hour of use affects the value of a John Deere tractor 
	differently than for tractors of other brands. 
	You can test this by including an interaction with ```age:johndeere``` in the regression.
	
```
Enter your regression results here.



```

Test the hypothesis, at the 5 percent level of significance, that the slope for engine hours differs by brand. 

Does an additional hour of use affect the price of a John Deere tractor
differently than tractors of other brands?
	
```
Enter your response here.



```
	
	
	
