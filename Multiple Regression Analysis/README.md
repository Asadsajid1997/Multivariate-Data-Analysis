# Introduction:
HATCO (Hair, Anderson, and Tatham company) a large (though nonexistent company) industrial supplier
conducted survey of its customer through an established marketing firm and gathered a dataset. The survey
was focused on attributes identified by HATCO in past which is perceived to be the most influential in
the choice of suppliers.

# Objective:
The main question for this study is what influences the product usage? and to find that we have used
multiple regression analysis to forecast client product consumption based on their opinions of HATCO’s
performance. Also, this model will help HATCO to accurately predict usage level and identifying the most
influential factor in product consumption.

To achieve this objective, we have addressed following problem statements:
1. Consider the overall general Model X9 = X1 X2 X3 X4 X5 X6 X7
2. Perform correlation analysis
3. Fit and analyze the best single independent (simple) regression analysis
4. Fit and analyze stepwise regression analysis to select the best subset model using alpha = 0.05
5. Fit and analyze full model (confirmatory) regression analysis using alpha = 0.05
6. Using the best subset from the stepwise regression analysis now include variable X8 (Firm Size)
and analyze its effect and the new resultant model
7. Analyze and discuss the multiple regression analysis assumptions, e.g., Linearity, Normality,
Homoscedasticity, and Independence using residual and other graphical/statistical measures and
tests for all models
8. Analyze and discuss any influential observations with recommendations, as well as the model’s
multicollinearity.

# Dataset:
The collected data consist of 100 observations on 7 different variables and is an example of segmentation
study for a business-to-business situation.
Each of these variables was measured on a graphic rating scale, where a ten‐centimeter line was drawn
between the endpoints, labeled "Poor" and "Excellent". Respondents indicated their perceptions by
making a mark anywhere on the line. The mark was then measured and the distance from zero (in
centimeters) was recorded. The result was a scale ranging from zero to ten, rounded to a single decimal
place. The seven HATCO attributes rated by each respondent are as follows:

## X1 -Delivery speed‐‐‐amount of time it takes to deliver the product once an order has been confirmed
## X2 - Price level‐‐‐perceived level of price charged by product suppliers
## X3 - Price flexibility‐‐‐perceived willingness of HATCO representatives to negotiate price on all types of purchases
## X4 - Manufacturer's image‐‐‐overall image of the manufacturer/supplier
## X5 – Service*‐‐‐overall level of service necessary for maintaining a satisfactory relationship between supplier and purchaser
## X6 - Salesforce's image‐‐‐overall image of the manufacturer's sales force
## X7 - Product quality‐‐‐perceived level of quality of a particular product (e.g., performance or yield)
## X8 - Size of firm‐‐‐size of the firm relative to others in this market. This variable has two categories: 1=large, and 0=small
## X9 - Usage level‐‐‐how much of the firm's total product is purchased from HATCO, measured on a 100‐point percentage scale, ranging from 0 to 100 percent

# Analysis Required:
• Simple regression analysis with a single best variable
• Stepwise regression analysis at alpha = 0.05
• Full model multiple regression analysis at alpha = 0.05
• Introduction of variable Firm size (X8) to the model created from stepwise regression

# Result:

## Stage 1: 
We are doing multiple regression analysis with the objective of accurately predicting total
product purchase of HATCO. We are also interested in identifying the variables that lead help in predicting
total product purchase.

## Stage 2: 
This study is based on metric variables where the sample size consists of 100 observations of 8
variables. One of them, total product purchase which is called Usage level (X9) as per documentation, is
independent variable. Whereas X1 to X7 are potential independent variables. For the sample of 100
observations, with 7 potential independent variables, we are able to detect relationships with R2 values of
approximately 18% at a power of .80 with the significance level set at .05. The sample also meets the
guideline for the minimum ratio of observations to independent variables (5:1) with an actual ratio of 14:1

## Stage 3: 
The three assumptions to be addressed for the individual variables are linearity, constant variance
(homoscedasticity), and normality. Please refer to the attached excel sheet and SAS program output for
the scatter plots and residual plots between dependent variable, independent variables, and residuals.

## Stage 4: 
In this stage, we will take 4 approaches towards model building starting from simple regression
analysis with a single best variable, stepwise regression analysis at alpha = 0.05, a full model multiple
regression analysis at alpha = 0.05 and using the best subset from stepwise regression, we will introduce
variable Firm size (X8) to the model.


![image](https://github.com/Asadsajid1997/Multivariate-Data-Analysis/assets/126636246/3d34bba8-db96-49da-88ac-b92e7aec9e6b)


# 1st Approach: Simple regression analysis with a single best variable
As it is clear from the correlation matrix that the single best variable for the simple regression analysis is
Service (X5) with a correlation of 0.700 at the p-value of less than 0.001.

Fitting a simple linear regression model to predict X9 based on X5 gives us the below mentioned stats:

## Model Estimates:
R2: 0.49; Adj. R2: 0.48; Root MSE: 6.44; Coefficient of variation: 13.98; F value: 94.52; p-value
corresponding to this F value: <0.0001, Standard error: 0.86

![image](https://github.com/Asadsajid1997/Multivariate-Data-Analysis/assets/126636246/bd551336-ded6-4e33-88bc-e1660778fb88)

Based on above estimates, the regression variate will be Y = 21.65 + 8.38(X5). The coefficient of 8.38
implies that with 1 unit change in the value of X5, all else being equal, there will be 8.38 unit change in
the value of X9. P-value of the estimate and the model are both satisfactory. R2 of 0.49 indicates that 49%
of the variance in the model is being explained by X5.

# 2nd Approach: Stepwise regression analysis at alpha = 0.05
Fitting a stepwise multiple regression model to predict X9 based on selected independent variables (except
X8) gives us the below mentioned stats:

![image](https://github.com/Asadsajid1997/Multivariate-Data-Analysis/assets/126636246/d23fd12b-019c-4eb0-b2b4-819c89a4a8cc)

The first variable to enter the model is X5, with R2 value of 0.49. X3 enters next with 0.26 increase in R2.
The last variable to enter the model is X6 with an increase of 0.01 taking the total R2 value at 0.76. No
other variable can enter the model at alpha = 0.05. Root MSE of this model is 4.39 with coefficient of
variance as 9.53.

![image](https://github.com/Asadsajid1997/Multivariate-Data-Analysis/assets/126636246/5d7cbc2a-092c-41db-b2a0-bfed03d12b95)

The regression variate will be Y = -6.52 + 3.37(X3) + 7.62(X5) +1.40(X6). The coefficients of 3.37, 7.62,
and 1.4 implies that with 1 unit change in the value of X3, X5, and X6, all else being equal, there will be
3.37, 7.62, and 1.4 unit change in the value of X9, respectively. P-value of the estimate and the model are
both satisfactory, while we acknowledge that the X6 is on the borderline. R2 of 0.76 indicates that 76%
of the variance in the model is being explained by X5, X3 and X6.


#  3rd Approach: Full model multiple regression analysis at alpha = 0.05
Fitting a full multiple regression model to predict X9 based on all the independent variables (except X8)
gives us the below mentioned stats:

## Model Estimates:
R2: 0.77; Adj. R2: 0.76; Root MSE: 4.42; Coefficient of variation: 9.59; F value: 45.25; p-value
corresponding to this F value: <0.0001.

![image](https://github.com/Asadsajid1997/Multivariate-Data-Analysis/assets/126636246/9b049a01-7e2f-4312-ae3a-0c73788098bd)

Regression variate: Y = -10.18 + -0.05(X1) – 0.069(X2) + 3.36(X3) - 0.04(X4) + 8.36(X5) + 1.2(X6) +
0.56(X7). The respective coefficients of the independent variables imply that with 1 unit change in the
values of independent variables, all else being equal, there will be unit change in the value of X9 equivalent
to the coefficients. P-value of the model is satisfactory however there are some estimates whose p-value
does not satisfy the criteria of 0.05, namely X1, X2, X4, X6, and X7. It is interesting that in stepwise
regression, X6 was found to be significant by a very low margin, but the inclusion of other variables has
rendered it unimportant. R2 of 0.77 indicates that 77% of the variance in the model is being explained by
all the variables in the model.


# 4th Approach: Introduction of variable Firm size (X8) to the model created from stepwise regression:
Introducing X8 to the stepwise multiple regression model to predict X9 gives us the below mentioned
stats:

## Model Estimates:
R2: 0.79; Adj. R2: 0.78; Root MSE: 4.17; Coefficient of variation: 9.05; F value: 90.89; p-value
corresponding to this F value: <0.0001.

![image](https://github.com/Asadsajid1997/Multivariate-Data-Analysis/assets/126636246/3cc8a273-8bbe-4aa1-b367-5984ad0914ca)


We have already interpreted the stepwise regression model hence the process is same for this one. One
thing that needs to be highlighted is that inclusion of Firm size (X8) in the model has increased the Adj.
R2 to 0.78 from 0.76. Root MSE and coefficient of variance have also improved from the best regression
we have earlier. It is safe to say that with the inclusion of firm size, this is the best model out of all 4 that
we tried. Its parsimonious and has the highest Adj. R2. The regression variate here is Y = -16.33 +
4.24(X3) + 8.05(X5) +1.46(X6) + 3.85(X8). Since X8 is a categorical variable, the interpretation of X8’s
coefficient will be that with a bigger firm size (X8 = 1), the increase in the X9 would be 3.85 units.


# Multiple Regression Assumptions:
## Linearity: 
We have checked the scatter plots of every independent variable with the dependent variables.
While we conclude the assumption of linearity holds for all the variables, we certainly can see that there
are some variables which are more linear than the others. Examples being X3 and X3, that is the reason
they have more impact on the model and are the important variables identified in stepwise model. Also,
the standardized residual plot shows no non-linearity. (Please refer to the attached SAS output)

## Homoscedasticity: 
The residual plots of all the independent variables does not seem to show any
homoscedasticity. (Please refer to the attached SAS output)

## Normality: 
It seems that the condition of Normality is satisfied in the sense that in both the models, full
and stepwise, residual normal plot is on the diagonal but there are ups and downs in between. So, it would
be fair to say that it barely satisfies normality. It will be also fair to say that the full model deviates from
normality standard the most and the stepwise regression model with addition of X8 obeys normality
standard the most.

## Independence: 
Since all the plots of the residuals against independent variables are either null plots or
random plots without any pattern, it is safe to say that this condition is satisfied in all the models.

## Multicollinearity:
In the step wise regression model, the independent variables chosen (X3, X5, and X6) don’t have this
effect, as evident by the correlation matrix. However, when we try to fit Firm size (X8) into this model,
there is some multicollinearity introduced because of a somewhat high correlation between X3 and X8 (-
0.64). But the model still doesn’t suffer too much because if we observe both the variates of Model 2 and
Model 4, we see very little difference in the coefficients of X3, X5 and X8. The third model, all variable
regression model, suffers greatly from multicollinearity because there are multiple variables that are
correlated to each other and all of them have been used in the model.


# SUMMARY:
The complimentary evaluation of the confirmatory model and the regression results both help answer the
central research question: What influences product usage? The regression models produce predictions
with excellent degrees of predictive accuracy. The variation explained is greater than 75%, and the
predicted error rate for every prediction is about +-5%. These levels, in addition to the results confirming
model validity, give the greatest degrees of confidence regarding the quality and accuracy of the regression
models used as the basis for developing business strategies.

All the estimated models yielded results which were substantially identical: there are 2 significant
variables on product usage - price flexibility(X3) and services (X5) and one considerably less significant
influence – salesforce image (X6). For instance, based on estimated model 1 point increase in consumer
perception of variable X5 (services) will produce an increase of at least 8% in using a product. Same goes
for other 2 variables 1 point improvement in price flexibility and salesforce image will lead to 3.3% and
1.4% increase in product usage respectively. Additionally variable X8 (Firm Size) has demonstrated
significant influence on product usage. Usage levels at larger organizations are almost 4% greater than at
smaller firms. These results provide management a foundation to formulate a plan to increase product
usage.

Based on the findings to stat that only 3 variables have influence on product usage is an understatement
rather it is more accurate to think of these variables as representative of the perceptual dimensions.
Although there is some variation in the normality condition for the full model, but still, all the models do
satisfy the assumptions of multiple regression. We recommend management to use the 4th approach,
results of the stepwise regression with variable X8 for the best predictive accuracy.





