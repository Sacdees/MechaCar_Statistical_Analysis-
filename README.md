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
## :

![mecha_mpg](https://github.com/Sacdees/MechaCar_Statistical_Analysis-/blob/main/Resources/mecha_coil.png)

![mecha_mpg](https://github.com/Sacdees/MechaCar_Statistical_Analysis-/blob/main/Resources/lot_summary.png)

![mecha_mpg](https://github.com/Sacdees/MechaCar_Statistical_Analysis-/blob/main/Resources/total_summary.png)
- ## LINEAR MODEL