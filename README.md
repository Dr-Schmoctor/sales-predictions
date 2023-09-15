# Sales Predictions 2023
## by Jeffrey Prichard
 - Coding Dojo: Project 1

Analyzing data from sales can be a overwhelming when the data sets are large and dirty. However, this project takes a dataset from below to clean, analyze and present a conclusion from the data provided.

## Data Source
```
https://drive.google.com/file/d/1syH81TVrbBsdymLT_jl2JIf6IjPXtSQw/view
```
This dataset contains 8523 Rows, 12 Columns

## Data Dictionary
![readmedd](https://github.com/Dr-Schmoctor/sales-predictions/assets/124634764/9b8015ee-19d1-46dd-93a9-361d66f5701d)

**To prepare this project, the data was inspected and cleaned before analysis.**

## Methods
For projected analysis using Machine Learning Data was:
- Scaled for Machine Learning using skLearn
- OneHotEncoded for machine Learning using skLearn
- OrdinalEncoded for Machine Learning using skLearn

 The data was then modeled using:
 - Linear Regression
 - Random Forest

## Exploratory Analysis
For the exploratory analysis:
- a boxplot and histogram was visualized for each numeric datatype column
- a barplot was visualized for each categorical column. 
- Each visual was inspected and a description was added of the analysis.


![readme4](https://github.com/Dr-Schmoctor/sales-predictions/assets/124634764/6eaaedb9-2cdf-4324-8fdf-2f8776a29693)
* This histogram represents our total outlet sales per item. We can see that the majority of our sales are below the 4k line. However we did analyze this further by comparing the outlet sales per item.


![readme3](https://github.com/Dr-Schmoctor/sales-predictions/assets/124634764/afba62e1-6d6e-4c5a-bd9d-b1e1d28d8e47)
* This shows that the median outlet sale for all of our Item Types is similar. The data shows that several of the item-types have higher end outliers that are influencing the data.


![readme2](https://github.com/Dr-Schmoctor/sales-predictions/assets/124634764/4ea5a6e3-ffbb-4f84-8c86-e40128fe1b39)
* We also analyze the volume of each item_type in our data set. This shows a significant skew towards Fruits and Vegetables, Snack Foods and Household for Item_Types.


![top10features](https://github.com/Dr-Schmoctor/sales-predictions/assets/124634764/2c0c8e2b-fac3-4b86-b4ce-c13e2cb247ef)
* this visual shows our top 10 features by impact on our ML model. This shows us our most impactful was Item MRP followed by Outlet Type - Grocery Store, Item Visibility, Item Weight, and Outlet Type - Supermarket 3.


![top15largest](https://github.com/Dr-Schmoctor/sales-predictions/assets/124634764/b0c681a2-4926-49c1-b9cb-4c3c0b2091dd)
* this visual shows our top 3 coefficiencts are Outlet Location Type Tier 2 followed by OUtlet Identifier - OUT049 and Outlet Loation Typer - Tier 3.


 ## Model
 Baseline:
 - Training Data
    - MAE:  1360.218
    - MSE:  2959455.705
    - RMSE: 1720.307
    - R^2:  0.000
 - Test Data
    - MAE:  1326.121
    - MSE:  2772144.463
    - RMSE: 1664.976
    - R^2:  -0.005

 Linear Regression:
- Training Data
    - MAE:  848.194
    - MSE:  1298814.122	
    - RMSE: 1139.655
    - R^2:  0.561
 - Test Data
    - MAE:  807.189
    - MSE:  1199635.872
    - RMSE: 1095.279
    - R^2:  0.565
    - 
 Random Forest:
 - Training Data
    - MAE:  755.293
    - MSE:  1152694.395
    - RMSE: 1073.636
    - R^2:  0.611
 - Test Data
    - MAE:  728.033
    - MSE:  1093835.119
    - RMSE: 1045.866
    - R^2:  0.604
      
## Recomendations:
 It appears our Random Forest is a better model to utilize after the tuning.

1. The stakeholders can be confident in this analysis because our R2 value for the Training (.611) AND Test (.604) data are strong.
2. this model is also not underfit or overfit for our data. Compared to our first Random Forest model, which was overfit for our Training Data, this model shows a much closer R2 for both Training/Test and also has a similar RMSE on both.

The RMSE was also the best on our Tuned Random Forest model. It was a smaller error than our Linear or Baseline model on the Test data.

We recommend this model for use in the future.

However, we also can use our visualizations to offer deaper insight. For one, we should look into opening onlh supermarket Type 1 going forward as these have the highest outlet sales among the store types, we should also look into why the stores opened in 1998 perform so poorly. Possibly we could close these stores and open new Supermarket type 1 with the supplies.

## Limitations and Next Steps:
- It appears MRP is the most influential feature when impacting Projected Sales Price. It could be useful to expand our data and see if there are any other features that could impact this.

## For Further Information:
Please contact: 
- Jeffrey Prichard
- JeffWPrichard@gmail.com
