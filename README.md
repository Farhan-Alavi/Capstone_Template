# Sprint 0 - Project Overview and Area of Interest
- My area of interest is medicine. There are many opportunities that arise when working with medical data as it is continuously updated and ever evolving. Predictions can be made to try and forecast specific things such as the number of diseases that may be reported in a certain area or how well a certain medication will sell in another area based on historical trends. 

- For my capstone project, the main idea is to train a **Predictive Machine Learning Model** to assess the number of **Infectious Diseases by Disease, County, Year, and Sex in California** from 2001 to 2022 and predict future cases based on historical data and demographics of the infected counties. 

## The Impact: 

- The MLM will help Infectious Disease Specialists, Doctors, and other medical professionals to visualize the historical cases over a date range and try to predict if the same factors will influence future cases. 
- I believe the visuals will also serve as a learning aid. 

## The Data:
The disease data is from the California Department of Public Health, a division of the US Government. 
The census data was found from https://www.census.gov/ 
Below you'll find more detailed information regarding the datasets and a progress update from inception to now. 

#Sprint 1: EDA and Getting Familiar with the Dataset
- Performed the first round of EDA. Optimized both the Infectious and Demographics CSV files on Excel before importing into Python for exploration and preprocessing. 
- Merged both CSVs in Excel and then checked the shape in Python. Final merged shape was (62234, 78)
- Checked for null and duplicated values. 
- Checked .info() to understand what kinf of datatypes we were dealing with. 
- Ran sanity checks after every major step to ensure everything worked as expected. 
### Infectious Disease table
| Column Name | Datatype |   |
|-------------|----------|---|
| Disease     | Object   |   |
| County      | Object   |   |
| Year        | int64    |   |
| Sex         | Object   |   |
| Male Cases  | int64    |   |
| Female Cases| int64    |   |
| Total Cases | int64    |   |
| Population  | int64    |   |


### Demographics table

| Column Name                       | Data type |
|-----------------------------------|-----------|
| County                            | Object    |
| Year                              | int       |
| Population                        | int       |
| Males                             | int       |
| Females                           | int       |
| White Males                       | int       |
| White Females                     | int       |
| Black Males                       | int       |
| Black Females                     | int       |
| Native Males                      | int       |
| Native Females                    | int       |
| Asian Males                       | int       |
| Asian Females                     | int       |
| Hawaiian Male                     | int       |
| Hawaiian Females                  | int       |
| Multi-Race Males                  | int       |
| Multi-Race Females                | int       |
| White-Mixed Males                 | int       |
| White-Mixed Females               | int       |
| Black-Mixed Males                 | int       |
| Black-Mixed Females               | int       |
| Native-Mixed Males                | int       |
| Native-Mixed Females              | int       |
| Asian-Mixed Males                 | int       |
| Asian-Mixed Females               | int       |
| Hawaiian-Mixed Males              | int       |
| Hawaiian-Mixed Females            | int       |
| Not-Hispanic Males                | int       |
| Not-Hispanic Females              | int       |
| Not-Hispanic White Males          | int       |
| Not-Hispanic White Females        | int       |
| Not-Hispanic Black Males          | int       |
| Not-Hispanic Black Males.1        | int       |
| Not-Hispanic Native Male          | int       |
| Not-Hispanic Native Female        | int       |
| Not-Hispanic Asian Male           | int       |
| Not-Hispanic Asian Female         | int       |
| Not-Hispanic Hawaiian Male        | int       |
| Not-Hispanic Hawaiian Female      | int       |
| Not_Hispanic Mixed Males          | int       |
| Not_Hispanic Mixed Females        | int       |
| Not_Hispanic White-Mixed Males    | int       |
| Not_Hispanic White-Mixed Females  | int       |
| Not_Hispanic Black-Mixed Males    | int       |
| Not_Hispanic Black-Mixed Males.1  | int       |
| Not_Hispanic Native-Mixed Males   | int       |
| Not_Hispanic Native-Mixed Females | int       |
| Not_Hispanic Asian-Mixed Males    | int       |
| Not_Hispanic Asian-               | int       |


### Merged table
| Column Name                         | Data Type |
|-------------------------------------|-----------|
| Disease                             | Object    |
| County                              | Object    |
| Year                                | Int64     |
| Male Cases                          | Int64     |
| Female Cases                        | int64     |
| Total Cases                         | int64     |
| Population                          | Int64     |
| Males                               | Int64     |
| Females                             | Int64     |
| White Males                         | Int64     |
| White Females                       | Int64     |
| Black Males                         | Int64     |
| Black Females                       | Int64     |
| Native Males                        | Int64     |
| Native Females                      | Int64     |
| Asian Males                         | Int64     |
| Asian Females                       | Int64     |
| Hawaiian Male                       | Int64     |
| Hawaiian Females                    | Int64     |
| Multi-Race Males                    | Int64     |
| Multi-Race Females                  | Int64     |
| White-Mixed Males                   | Int64     |
| White-Mixed Females                 | Int64     |
| Black-Mixed Males                   | Int64     |
| Black-Mixed Females                 | Int64     |
| Native-Mixed Males                  | Int64     |
| Native-Mixed Females                | Int64     |
| Asian-Mixed Males                   | Int64     |
| Asian-Mixed Females                 | Int64     |
| Hawaiian-Mixed Males                | Int64     |
| Hawaiian-Mixed Females              | Int64     |
| Not-Hispanic Males                  | Int64     |
| Not-Hispanic Females                | Int64     |
| Not-Hispanic White Males            | Int64     |
| Not-Hispanic White Females          | Int64     |
| Not-Hispanic Black Males            | Int64     |
| Not-Hispanic Black Males.1          | Int64     |
| Not-Hispanic Native Male            | Int64     |
| Not-Hispanic Native Female          | Int64     |
| Not-Hispanic Asian Male             | Int64     |
| Not-Hispanic Asian Female           | Int64     |
| Not-Hispanic Hawaiian Male          | Int64     |
| Not-Hispanic Hawaiian Female        | Int64     |
| Not_Hispanic Mixed Males            | Int64     |
| Not_Hispanic Mixed Females          | Int64     |
| Not_Hispanic White-Mixed Males      | Int64     |
| Not_Hispanic White-Mixed Females    | Int64     |
| Not_Hispanic Black-Mixed Males      | Int64     |
| Not_Hispanic Black-Mixed Males.1    | Int64     |
| Not_Hispanic Native-Mixed Males     | Int64     |
| Not_Hispanic Native-Mixed Females   | Int64     |
| Not_Hispanic Asian-Mixed Males      | Int64     |
| Not_Hispanic Asian-Mixed Females    | Int64     |
| Not_Hispanic Hawaiian-Mixed Males   | Int64     |
| Not_Hispanic Hawaiian-Mixed Females | Int64     |
| Hispanic Males                      | Int64     |
| Hispanic Females                    | Int64     |
| Hispanic-White Males                | Int64     |
| Hispanic-White Females              | Int64     |
| Hispanic-Black Males                | Int64     |
| Hispanic-Black Females              | Int64     |
| Hispanic-Native Males               | Int64     |
| Hispanic-Native Females             | Int64     |
| Hispanic-Asian Males                | Int64     |
| Hispanic-Asian Females              | Int64     |
| Hispanic-Hawaiian Males             | Int64     |
| Hispanic-Hawaiian Females           | Int64     |
| Hispanic-Mixed Males                | Int64     |
| Hispanic-Mixed Females              | Int64     |
| Hispanic-White Mixed Males          | Int64     |
| Hispanic-White Mixed Females        | Int64     |
| Hispanic-Black Mixed Males          | Int64     |
| Hispanic-Black Mixed Females        | Int64     |
| Hispanic-Native Mixed Males         | Int64     |
| Hispanic-Native Mixed Females       | Int64     |
| Hispanic-Asian Mixed Males          | Int64     |
| Hispanic-Asian Mixed Females        | Int64     |
| Hispanic-Hawaiian Mixed Males       | Int64     |
| Hispanic-Hawaiian Mixed Females     | Int64     |

# Sprint 2: Data Processing and Baseline Modelling
- Added the Male Cases and Female Cases fields back into the data set. 
- Split the Disease and County fields into dummy variables.
- Made a Linear Regression Model 
- Found the correlations between all the variables.
- Prepped a baseline model for Sprint 3 
- Final shape including dummy variables is (62234, 189)
- The baseline model I chose was a Linear Regression Model. Initiallty the R2 value was very low with a 

Training MAE: 14.9479045945444
Training MSE: 3879.5459280936643
Training R-squared: 0.17164770929598816
Training MAPE: 2.4551071836409132e+16

Test MAE: 13.907340401555361
Test MSE: 2130.3833886111574
Test R-squared: 0.16084145966786323
Test MAPE: 2.5130936857551144e+16

#### Correlation with Total Cases:

Female Cases and Male Cases have very high positive correlations with Total Cases (0.9869 and 0.9915 respectively), suggesting a strong positive linear relationship. Population, Males, Females, and other demographic groups also show moderate positive correlations with Total Cases.

However, many diseases and counties have negligible correlations with Total Cases, as indicated by correlation values close to zero.

P-values:

All the p-values are extremely small (0.000), indicating that the correlations are statistically significant. Overall, the results suggest that there is a strong positive linear relationship between Female and Male Cases and Total Cases. Additionally, moderate positive relationships exist between Total Cases and various demographic indicators like Population, Males, Females, etc. However, the correlations between diseases and Total Cases are generally low or negligible.

# Sprint 3: Advanced Modelling and Refining the Data
- Using the Train/Test split from the Linear Regression Model in Sprint 2, I built upon that foundation by using various other models such as KNN-regressor, Decision Tree-regressor, Random Forest-regressor, Pipeline, Gradient Boost, and GridSearch 

### Comparing the models
**KNN:**
Nearest Neighbor = 2700
Training MAE: 13.498010701950157
Training MSE: 5170.465471838032
Training R-squared: 0.040140512846411625

Test MAE: 11.840710270807483
Test MSE: 2437.960452981889
Test R-squared: 0.03968677842278867

**Linear Regression:**
Training MAE: 13.498010701950157
Training MSE: 5170.465471838032
Training R-squared: 0.040140512846411625

Test MAE: 11.840710270807483
Test MSE: 2437.960452981889
Test R-squared: 0.03968677842278867
Test MAPE: 1.943195516731936e+16

**Decision Tree:**
Max Depth = 12
Training MAE: 4.204467845858909
Training MSE: 423.273495187978
Training R-squared: 0.9096235549644484

Test MAE: 4.6579702368670155
Test MSE: 471.5742464023075
Test R-squared: 0.8142467884491111

### Building on the Decision Tree

**Random Forest:**
After iterating through 50 DTs, the average score was:

Performance on fitted data:
Average Decision Tree: 0.8877864821836363
Random Forest: 0.9205973386420051
----------------
Performance on test data:
Average Decision Tree: 0.7789187924161982
Random Forest: 0.8336376284299822

**Gradient Boosting:**
Mean Squared Error: 540.3983390520027
Mean Absolute Error: 5.630862947857966
R Squared: 0.787136961440343

**Comparing GB, AdaBoost, and RF**
Train Set Scores:
AdaBoost score: 0.2546471104144652
Random Forest score: 0.9227039110879212
G boost score: 0.8691151246222372
Test Set Scores:
AdaBoost score: -0.5473196086694583
Random Forest score: 0.8313412634240243
G boost score: 0.787136961440343

**Stacked Model:**
Mean Squared Error of Stacked Model: 444.1404303760023
R2 of Stacked Model: 0.8250529753239453
Mean Absolute Error of Stacked Model: 4.649376735200258

**Pipeline**
Train Score = 0.9217244739474117, Test Score 0.8294790101543619

**Grid Search:**
Best Hyperparameters: {'random_forest__max_depth': 10, 'random_forest__min_samples_split': 2, 'random_forest__n_estimators': 50}
Best Root Mean Squared Error (RMSE): 20.848093031488872
Best R2: 0.8287940221598805
Best Mean Absolute Error: 4.542704640287811

### Comparison of all our models:

Mean Absolute Error:
Decision Tree: 4.706424841252354
Gradient Boosting: 5.630862947857967
Random Forest: 72.60937230839234
Pipeline: 4.5702430278879325
Grid Search: 4.542704640287811

R2:
Decision Tree: 0.80719753444914
Gradient Boosting: 0.7871369614403428
Random Forest: -1.6851946900954924
Pipeline: 0.8294790101543619
Grid Search: 0.8287940221598805
Of all the models above, it comes down to either a Grid Search or Pipeline.

MAE: Pipeline = 4.5702430278879325 Grid Search = 4.542704640287811

R2 Pipeline = 0.8294790101543619 Grid Search = 0.8287940221598805

# Summary of project
I have come a long way since the very beginning of this project. From finding the dataset, to doing the initial EDA, to processing and building a baseline model, to optimizing that model by supplementing it with others, I feel I have accomplished so much. 

There is still a lot more work to be done but as of now, I'm feeling good about it. 
I believe I answered the questions I set out to solve. 

1. What was the data science approach?
Assessing historical data of Infectious Disease cases and trying to predict future cases. 
My highest R2 value was 0.83 and that proved that many of the variables from the dataframe did indeed have some sort of positive correlation with each other. 

2. Next steps?
Some next steps would be to add supplementary data such as more specific information regarding the ethnic breakdown of disease cases. Are certain ethnicities more susceptible to a disease? 
