# IDENTIFICATION OF TRAVEL SHARING PATTERNS OF THE ZUBER COMPANY

## PROJECT OVERVIEW

The mining company `OilyGiant` is looking to build `200 new oil wells`. Our task is to find the region with the highest profit margin for the company. We have information about oil reserves in three specific regions. We will train and test the model for each region in `geo_data_0.csv`.

`Conditions:`
- Only `linear regression` should be used for model training.
- When exploring the region, a `500-point study` is carried out with the `best 200 points` being selected for profit calculation.
- `The budget` for the development of `200 oil wells` is `100 million dollars`.
- `A barrel of raw materials` generates `4.5 USD of revenue`. The revenue from a `product unit is 4500 USD` (the volume of reserves is expressed in thousands of barrels).
- After risk assessment, keep only the `regions with loss risk less than 2.5%`. Of those that fit the criteria, the region with the highest average profit should be selected.
- The data is synthetic: contract details and well characteristics are not published.

Three models will be trained, one for each region (dataset). Once trained, the model will be applied to a validation dataset to forecast oil reserve levels. Based on the 200 largest oil reserves, the potential profit will be determined using the validation dataset. After the initial data has been processed and examined, an average profit distribution will be compiled for each location. For each region, the average profit, 95% confidence interval, and risk of loss will be calculated and displayed. We will choose the largest and most advantageous area for OilyGiant to build its new well based on those calculated figures.


## STEPS:

### STEP 1: IMPORTING LIBRARIES

### STEP 2: IMPORTING DATABASES

### STEP 3: DATA EXPLORATION

### STEP 4: MODELING

### STEP 5: CALCULATION OF BENEFITS

### STEP 6: APPLICATION OF BOOTSTRAPPING METHOD TO DETERMINATE THE MOST PROFITABLE REGION


## CONCLUSION

We start by training the linear regression model with the datasets of each region to `predict the average reservation volumes` and the RMSE of each validation set of each dataset.` Obtaining that region 1 geo_data_1` has a `more accurate model but a lower average volume than region 0 and 2`.

We then `calculated the profits associated with the 200 wells` with the highest predicted values ​​and `found that region 0 (geo_data_0)` earned a `Profit` of $36 million, `Volume` of approx. 30 million barrels, with region 0`s profit being greater than regions 1 and 2, and exceeding the projected reserve volumes of 22 million barrels. While this was a good starting point for the analysis, `more samples were needed to achieve greater accuracy`.

To improve the accuracy of our models, we used the bootstrap method to obtain 1000 samples and determine the distribution of profits for each region. Using the resulting average profit, the 95% confidence interval, and the risk of loss values, we concluded that Region 1 is the most suitable location, because Region 0 and 2 exceed the risk of loss threshold of 2.5%, and the lower and upper profit confidence intervals are positive unlike the other regions.

Therefore we conclude that `region 1` is the best region for OilyGiant Mining Company to build its new oil well. This decision is made despite the fact that initially it was thought that `region 0` was the most profitable, but its model had a high RMSE, so `after applying the bootstrap method, region 1` which improves the precision of the model obtained a higher average profit and a lower risk of loss than requested.

PROJECT BY: GIORGIO RAMIREZ QUIROZ
