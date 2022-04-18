# MechaCar_Statistical_Analysis
Statisitical analysis of automobile performance with R
## Overview
AutosRUs' new MechaCar is "suffering from production troubles" and the company is hoping that an analytical review may help provide some insight. The goal of this project is to:
- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a study to compare the MechaCar performance against vehicles from other manufacturers.
## Results
### Linear Regrssion to Predict MPG

![Screen Shot 2022-04-17 at 6 26 09 PM](https://user-images.githubusercontent.com/95242493/163738433-04555830-d08e-40d8-ba42-71de6549ed43.png)
- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

  The most significant variables in our dataset which show a non-random effect on the MPG of the MechaCar are the Vehicle Length and the Ground Clearance.   As indicated by the yellow arrows in the image above, a linear regression model run on these variables against figures for MPG, resulted in p-values of     2.6x10-12 and 5.21x10-8, respectively. The intercept was also statistically significant, indicating that there are likely other factors, not included in   our dataset, that have a strong impact on the MPG.
- Is the slope of the linear model considered to be zero? Why or why not? 

  The slope of the linear model can not be considered to be zero, as the p-value of 5.35x10-11, indicated by the orange arrow above, is lower than even an   extreme level of significance, and thus the null hypothesis must be rejected. This means that the relationship between our variables and the miles per     gallon is subject to more than random chance.
- Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

  There are still unconsidered factors, this model does predict the mpg of the MechaCar prototype with some relative effectiveness. The r-squared value of   0.7149, highlighted in the purple box, indicates that the model is 71% accurate... though it could probably do better.

### Summary Statistics on Suspension Coils
**total_summary dataframe:**

![Screen Shot 2022-04-17 at 7 34 22 PM](https://user-images.githubusercontent.com/95242493/163740979-2ffa7c3f-619d-4f1d-bc59-02ccaaaa9ef1.png)

**lot_summary dataframe:**

![Screen Shot 2022-04-17 at 7 37 17 PM](https://user-images.githubusercontent.com/95242493/163741162-1abcbf5f-c6a3-41ec-a463-39ff7199fc04.png)

While the overall variance, as shown in the Total Summary data above, is under 100 psi and meets specifications, there is a problem with one of the individual lots. As shown in the Lot Summary stats, the variance for Lot 3 is well over the acceptable threshold, at 170.28.
