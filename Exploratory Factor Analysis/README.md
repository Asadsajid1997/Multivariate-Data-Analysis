
# Introduction:

HATCO (Hair, Anderson, and Tatham company) a large (though nonexistent company) industrial supplier conducted survey of its customer through an established marketing firm and gathered a dataset. The survey
was focused on attributes identified by HATCO in past which is perceived to be the most influential in
the choice of suppliers.

# Problem Statement:

1. Understand whether these perceptions can be grouped. By grouping the perceptions, HATCO will
be able to see the big picture in terms of understanding its customers and what the customers think
about HATCO.
2. Reduce the 7 variables to smaller size so that other multivariate technique can be more
parsimonious.

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
## X5 – Service‐‐‐overall level of service necessary for maintaining a satisfactory relationship between supplier and purchaser
## X6 - Salesforce's image‐‐‐overall image of the manufacturer's sales force
## X7 - Product quality‐‐‐perceived level of quality of a particular product (e.g., performance or yield)

* (It is to be noted that at the start of the analysis, we have total of 7 variables which were giving an overall
MSA of less than 0.5 which prompted us to delete the variable V5 from the dataset and then we achieved
satisfactory overall MSA to run factor analysis.)


# Analysis Required:
• Principal Component Analysis
• Exploratory Factor Analysis seeking the best parsimonious set of variables and factors, based on
deleting variables per their MSA score and cross-dual loadings, and factors based on contribution
to variance contribution and explanation
• Identify the core set of variables and factors with rationale
• Create surrogate variate factor scores using both factor scoring and summated scoring methods,
analyze descriptive statistics and correlations


# Result:
Based on our analysis we have categorized these 6 variables in 3 factors and found their summated scale
which further can be used in different multivariate techniques.

![image](https://github.com/Asadsajid1997/Multivariate-Data-Analysis/assets/126636246/4b182d2f-b25d-4697-99df-3a785ae68ad5)


## Stage 1: 
We are doing an exploratory analysis where data reduction is the primary goal. The unit of
analysis for factor analysis is variables for this study.


## Stage 2: 
This study is based on metric variables where the sample size consists of 100 observations of 6
variables.


## Stage 3:
The overall value of MSA for this analysis in the first iteration is 0.664 which is greater than 0.5
hence we can proceed further with the factor analysis, and all the individual variables had MSA greater
than 0.5. It is to be noted that at the start of the analysis, we have total of 7 variables which were giving
an overall MSA of less than 0.5 which prompted us to delete the variable V5 from the dataset and then we
achieved satisfactory overall MSA to run factor analysis.


## Stage 4: 
We have decided to perform Principal component analysis for this study because here data
reduction is a primary concern, focusing on the minimum number of factors needed to account for the
maximum portion of the total variance represented in the original set of variables. Next, we must decide
on the number of factors to extract. If we use the scree test criterion, we see then the point at which the
curve first begins to straighten out is 3, which is considered the maximum number of factors to extract.
Hence, we will be extracting 3 factors. It is to note that although latent root criterion asks us to retain only
two factors, it is suitable for an analysis where 20 to 50 variables are involved whereas we only have 6.
Therefore, we would go ahead with scree plot. The three factors retained represent 80.8 percent of the
variance of the 6 variables.

![image](https://github.com/Asadsajid1997/Multivariate-Data-Analysis/assets/126636246/35eed441-299d-40d8-9516-1f1ab49be5e2)

## Stage 5: 
The unrotated factor matrix is not conclusive as we can see that every variable is loading on
Factor 1 with residual variances loading on the remaining factors. We rotated this matrix orthogonally by
Varimax method and obtained the rotated factor matrix. As we can see, this gives much clearer
interpretation of the variable loading on the factors. These also satisfy the statistical guidelines because in
the sample of one hundred observations, the factor loadings of 0.55 and above are considered significant
based on sample size. All the individual communalities are also greater than 0.5. We conclude that there
is no cross-loading of one variable onto more than one factors. Although it is observed that variable X3
loads -0.66 on Factor 3 and 0.49 on factor 2, we conclude that the loading of 0.49 is not significant because
it is the less than the threshold of 0.55, hence we can ignore it.

![image](https://github.com/Asadsajid1997/Multivariate-Data-Analysis/assets/126636246/281f7beb-46ff-4a81-a597-922825ae8ee4)


Here is the variance explained by each factor. The size of the communality is a useful index for assessing
how much variance in a particular variable is accounted for by the factor solution. Higher communality
values indicate that a large amount of the variance in a variable has been extracted by the factor solution.
All of the variables here have high communality.

![image](https://github.com/Asadsajid1997/Multivariate-Data-Analysis/assets/126636246/03b00808-1555-4bf0-b6d2-f0ae696634c5)


Rotated Factor tables helps us understand the labels associated with the factors:
Factor 1 Marketing: X6, salesforce image; X4, Manufacturer’s image.
Factor 2 Product value: X1, Delivery speed; X7, Product quality.
Factor 3 Price value: X2, Price level; X3, Price flexibility.

![image](https://github.com/Asadsajid1997/Multivariate-Data-Analysis/assets/126636246/a0a0b282-0b59-45f8-b181-2452ae99fca5)

As we can see, there is no correlations between the scales.

![image](https://github.com/Asadsajid1997/Multivariate-Data-Analysis/assets/126636246/cbb29cc9-1a7c-4820-8003-d26eb75b033d)

High correlations between factor scores and summated scales imply that these summated scales can be
used in the place of these 3 factors for any analysis that needs to be done on these 6 variables.

# SUMMARY
To minimize the number of variables for study we have used exploratory factor analysis. The sample size
is 100 observations of 6 variables and as variable analysis is required; we have used R-type factor analysis.
In the beginning we were failed to achieve required MSA of more than 0.5 hence we have removed
attribute X5 and conducted analysis on remaining 6 variables. In second iteration we have achieved desired
result of MSA more than 0.5 and proceed further with factor analysis.
As the data reduction was primary concern of the study, we have used principal component analysis and
with the use of scree test criteria we have finalized that 3 factors should be extracted. These 3 factors
represent more than 80% of variability.
In the next step we used rotated factor matrix and got the clearer interpretation of variable loading on
factor. The factor loadings of 0.55 and above are considered significant based on sample. Based on result
we concluded that there is no cross-loading of one variable onto more than one factor. Also we have
identified variables associated with factors.


![image](https://github.com/Asadsajid1997/Multivariate-Data-Analysis/assets/126636246/4b182d2f-b25d-4697-99df-3a785ae68ad5)

In the last step we have checked the correlations between factor scores and summated scales which was
high so, based on our analysis we can use the summated scales in place of these 3 factors for any analysis
that needs to be done on these 6 variables.

