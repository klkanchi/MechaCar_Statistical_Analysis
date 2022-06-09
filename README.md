# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG

The MechaCar_mpg.csv dataset contains mpg test results for 50 prototype MechaCars. The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. Using your knowledge of R, you’ll design a linear model that predicts the mpg of MechaCar prototypes using several variables from the MechaCar_mpg.csv file.

### To Deliver.

1. The MechaCar_mpg.csv file is imported and read into a dataframe
2. An RScript is written for a linear regression model to be performed on all six variables
3. An RScript is written to create the statistical summary of the linear regression model with the intended p-values
4. There is a summary that addresses all three questions

Resulting lm Model:

**mpg = (6.267)vehicle_length + (0.0012)vehicle_weight + (0.0688)spoiler_angle + (3.546)ground_clearance + (-3.411)AWD + (-104.0)**

![lm_model.png](https://github.com/klkanchi/MechaCar_Statistical_Analysis/tree/main/Resources/images/lm_model.png)

![linear_regression_all.png](https://github.com/klkanchi/MechaCar_Statistical_Analysis/tree/main/Resources/images/linear_regression_all.png)

![linear_regression_filtered.png](https://github.com/klkanchi/MechaCar_Statistical_Analysis/tree/main/Resources/images/linear_regression_filtered.png)

From the above output we can see that:

The vehicle length, and vehicle ground clearance are statistically likely to provide non-random amounts of variance to the model. That is to say, the vehicle length and vehicle ground clearance have a significant impact on miles per gallon on the MechaCar prototype. Conversely, the vehicle weight, spoiler angle, and All Wheel Drive (AWD) have p-Values that indicate a random amount of variance with the dataset.

The p-Value for this model, p-Value: 5.35e-11, is much smaller than the assumed significance level of 0.05%. This indicates there is sufficient evidence to reject our null hypothesis, which further indcates that the slope of this linear model is not zero.

This linear model has an r-squared value of 0.7149, which means that approximately 71% of all mpg predictions will be determined by this model. Relatively speaking, his multiple regression model does predict mpg of MechaCar prototypes effectively.

If we remove the less impactful independent variables (vehicle weight, spoiler angle, and All Wheel Drive), the predictability does decrease, but not drastically: the r-squared value falls from 0.7149 to 0.674.
