# Assignment 2

Complete the exercise described in the pdf above and enter your answers in 
the spaces below.

## Running the Script as Given

Run the entire script and compare 
the output from ```summary(lm_full_model)```, 
which includes all variables, 
with that from ```summary(lm_no_damage)```, 
which omits the damage indicator. 
If there are no cars with damage in your simulation, 
run the script again to take another draw.


a. Copy and paste the regression model estimates after the commands
```summary(lm_full_model)``` and ```summary(lm_no_damage)```. 

```
Call:
lm(formula = car_price ~ mileage + accident + damage, data = car_data)

Residuals:
   Min     1Q Median     3Q    Max 
-10329  -2933    181   2976  11304 

Coefficients:
              Estimate Std. Error t value Pr(>|t|)    
(Intercept)  5.024e+04  1.998e+03  25.147  < 2e-16 ***
mileage     -2.012e-01  3.885e-02  -5.179 1.23e-06 ***
accident    -4.812e+03  8.627e+02  -5.578 2.24e-07 ***
damage      -2.059e+04  2.168e+03  -9.496 1.80e-15 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 4073 on 96 degrees of freedom
Multiple R-squared:  0.6899,	Adjusted R-squared:  0.6802 
F-statistic: 71.21 on 3 and 96 DF,  p-value: < 2.2e-16


Call:
lm(formula = car_price ~ mileage + accident, data = car_data)

Residuals:
     Min       1Q   Median       3Q      Max 
-20324.3  -2143.7    653.5   3761.6  11291.0 

Coefficients:
              Estimate Std. Error t value Pr(>|t|)    
(Intercept) 52787.3683  2742.8820  19.245  < 2e-16 ***
mileage        -0.2525     0.0533  -4.737 7.41e-06 ***
accident    -6722.2839  1162.2419  -5.784 8.91e-08 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 5643 on 97 degrees of freedom
Multiple R-squared:  0.3987,	Adjusted R-squared:  0.3863 
F-statistic: 32.16 on 2 and 97 DF,  p-value: 1.932e-11


b. Compare the estimated coefficient for ```ACCIDENT``` 
with and without the damage variable. 
How does this relate to the coefficient for ```DAMAGE```?

```
accident    -4.812e+03  8.627e+02  -5.578 2.24e-07 ***
damage      -2.059e+04  2.168e+03  -9.496 1.80e-15 ***

accident    -6722.2839  1162.2419  -5.784 8.91e-08 ***

```


c. Compare the values of 
```Multiple R-squared``` and ```Adjusted R-squared``` for the two models. 
Which model do you recommend (pretending that you don't know the true model)? 

```
summary(lm_full_model)
Multiple R-squared:  0.6899
```




## Running the Script after Modification


d. Copy and paste the new regression model estimates after the commands
```summary(lm_full_model)``` and ```summary(lm_no_damage)```. 

```
Call:
lm(formula = car_price ~ mileage + accident + damage, data = car_data)

Residuals:
    Min      1Q  Median      3Q     Max 
-7897.5 -3346.9  -270.9  2812.5 11020.0 

Coefficients:
              Estimate Std. Error t value Pr(>|t|)    
(Intercept)  5.003e+04  2.144e+03  23.332  < 2e-16 ***
mileage     -2.074e-01  4.121e-02  -5.033 2.25e-06 ***
accident    -4.870e+03  9.178e+02  -5.306 7.20e-07 ***
damage       1.779e+03  1.662e+03   1.070    0.287    
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 4193 on 96 degrees of freedom
Multiple R-squared:  0.3642,	Adjusted R-squared:  0.3443 
F-statistic: 18.33 on 3 and 96 DF,  p-value: 1.76e-09```

Call:
lm(formula = car_price ~ mileage + accident, data = car_data)

Residuals:
    Min      1Q  Median      3Q     Max 
-7168.3 -3394.8  -466.7  3065.1 11009.7 

Coefficients:
              Estimate Std. Error t value Pr(>|t|)    
(Intercept)  4.987e+04  2.140e+03  23.298  < 2e-16 ***
mileage     -2.041e-01  4.112e-02  -4.963 2.96e-06 ***
accident    -4.516e+03  8.567e+02  -5.271 8.22e-07 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 4196 on 97 degrees of freedom
Multiple R-squared:  0.3566,	Adjusted R-squared:  0.3433 
F-statistic: 26.88 on 2 and 97 DF,  p-value: 5.156e-10

e. For this new set of regressions, compare the estimated coefficient 
for ```ACCIDENT``` with and without the damage variable. 
How does this relate to the new coefficient for ```DAMAGE```?

```
without damage
accident    -4.516e+03  8.567e+02  -5.271 8.22e-07 ***
with damage
accident    -4.870e+03  9.178e+02  -5.306 7.20e-07 ***
```


f. Compare the values of 
```Multiple R-squared``` and ```Adjusted R-squared``` for the two models. 
Now which model do you recommend (pretending that you don't know the true model)? 

```
Multiple R-squared:  0.3642
```

