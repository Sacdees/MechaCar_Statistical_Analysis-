# MechaCar_Statistical_Analysis-
## Study Design: MechaCar vs Competition

The MechaCar prototypes were designed and produced using multiple design specifications to identify ideal performance of the vehicles.  Metrics include vehicle length, wieght, spoiler construction, drivetrain and amount of clearance from the ground.  Based on these factors MechaCar wanted a prediction model to help determine the average mpg based on those factors 

# DELIVERABLE 1:
## Linear Regression to Predict MPG:

![mecha_mpg](https://github.com/Sacdees/MechaCar_Statistical_Analysis-/blob/main/Resources/mecha_mpg.png)

- ## LINEAR MODEL

lm(mpg ~ vehicle_length + vehicle_weight + spoiler_angle + ground_clearance + AWD, data=mecha_mpg)

Call:
lm(formula = mpg ~ vehicle_length + vehicle_weight + spoiler_angle + 
    ground_clearance + AWD, data = mecha_mpg)

Coefficients:
     (Intercept)    vehicle_length    vehicle_weight     spoiler_angle  
      -1.040e+02         6.267e+00         1.245e-03         6.877e-02  
ground_clearance               AWD  
       3.546e+00        -3.411e+00 

- ## STATISTICS
summary(lm(mpg ~ vehicle_length + vehicle_weight + spoiler_angle + ground_clearance + AWD, data=mecha_mpg)) 

Call:
lm(formula = mpg ~ vehicle_length + vehicle_weight + spoiler_angle + 
    ground_clearance + AWD, data = mecha_mpg)

Residuals:
     Min       1Q   Median       3Q      Max 
-19.4701  -4.4994  -0.0692   5.4433  18.5849 

Coefficients:
                   Estimate Std. Error t value Pr(>|t|)    
(Intercept)      -1.040e+02  1.585e+01  -6.559 5.08e-08 ***
vehicle_length    6.267e+00  6.553e-01   9.563 2.60e-12 ***
vehicle_weight    1.245e-03  6.890e-04   1.807   0.0776 .  
spoiler_angle     6.877e-02  6.653e-02   1.034   0.3069    
ground_clearance  3.546e+00  5.412e-01   6.551 5.21e-08 ***
AWD              -3.411e+00  2.535e+00  -1.346   0.1852    
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 8.774 on 44 degrees of freedom
Multiple R-squared:  0.7149,	Adjusted R-squared:  0.6825 
F-statistic: 22.07 on 5 and 44 DF,  p-value: 5.35e-11

- ## SUMMARY
Many of the factor of the car build should change the value of how much MPG the MechaCar produces.  It would appear that vehicle weight and ground clearance seem to have the least affect on MPG, which would be a suprising result.  The regression would not be zero because of a postitive correlation between the different factors and the results produced ; as you change the variables the data changes as well.  The accuracy of this model falls around 71-72% and would recommend further testing before looking in on this data analysis for MPG determination.  

# DELIVERABLE 2 
## Summary Statistic on Suspension Coils:

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils should not exceed 100 pounds per square inch.

![mecha_mpg](https://github.com/Sacdees/MechaCar_Statistical_Analysis-/blob/main/Resources/mecha_coil.png)

- ## Total Summary

![mecha_mpg](https://github.com/Sacdees/MechaCar_Statistical_Analysis-/blob/main/Resources/total_summary.png)

- ## Lot Summary

![mecha_mpg](https://github.com/Sacdees/MechaCar_Statistical_Analysis-/blob/main/Resources/lot_summary.png)

- ## Summary
It would appear from the data given from this model that the test has fallen within the 100 pounds per square inch metric.  The PSI variance in the model was 62.29 well within the 100 PSI requirement.

# DELIVERABE 3
## T-Tests on Suspension Coils

t.test(lot1$PSI,mu=1500)

	One Sample t-test

data:  lot1$PSI
t = 0, df = 49, p-value = 1
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1499.719 1500.281
sample estimates:
mean of x 
     1500 

t.test(lot2$PSI,mu=1500)

	One Sample t-test

data:  lot2$PSI
t = 0.51745, df = 49, p-value = 0.6072
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1499.423 1500.977
sample estimates:
mean of x 
   1500.2 

t.test(lot3$PSI,mu=1500)

	One Sample t-test

data:  lot3$PSI
t = -2.0916, df = 49, p-value = 0.04168
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1492.431 1499.849
sample estimates:
mean of x 
  1496.14 

  ## Summary

  The following tests appear to hit and come close to the desired metrics as inticipated for the suspension tests.  These are just examples and the tests should be done extensively in comparison to other models of similar class to make sure they get the desired performance compared to other competitor products for ride quality.  



# DELIVERABLE 4
## Study Design: MechaCar vs Competition:

MechaCar at this time and point is ready to start apploy concepts to the data from his data team.  Researh is not wanted in comparison to other well-established products in the space with large consumber base and reliable sales and usage metrics.  Using the A/B testings will randomize the controlled experiement and help prevent bias on the results.  

MechaCar should perform statistical analysis and A/B blind comparison on several metrics if they wish to become competitive in the market, but as a start they should test: Miles Per Gallons (mpg) - monetary benefit ; Pound per square inch (psi) - ride quality ; 0 to 60 seconds test - performance ; Brake Testing on a specific distance - 200-1000 feet or safety standard for testing ; and ineterior decibel levels (dbs) - comfort quality.  These are all comparable metrics that can provide MechaCar on a great starting position.

If any of these metrics are less than the competitor than they must decice what is the target price point, audience and many other factors of company postioning using null or altertative anaylsis of the data ; yes or no ; tweak and test again.

