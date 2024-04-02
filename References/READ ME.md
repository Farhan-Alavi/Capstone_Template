## Project Overview and Area of Interest
- My area of interest is medicine. There are many opportunities that arise when working with medical data as it is continuously updated and ever evolving. Predictions can be made to try and forecast specific things such as the number of diseases that may be reported in a certain area or how well a certain medication will sell in another area based on historical trends. 

- For my capstone project, the main idea is to train a **Predictive Machine Learning Model** to assess the number of **Infectious Diseases by Disease, County, Year, and Sex in California** from 2001 to 2022 and predict future cases based on historical data and demographics of the infected counties. 

## The Impact: 

- The MLM will help Infectious Disease Specialists, Doctors, and other medical professionals to visualize the historical cases over a date range and try to predict if the same factors will influence future cases. 
- I believe the visuals will also serve as a learning aid. 

## The Data:
The disease data is from the California Department of Public Health, a division of the US Government. 
The census data was found from https://www.census.gov/ 
Below you'll find more detailed information regarding the datasets and a progress update from inception to now. 

## What changed between Sprint 1 and Sprint 2.
- Re-did the initial round of EDA
- Added the Male Cases and Female Cases fields back into the data set. 
- Split the Disease and County fields into dummy variables.
- Made a Linear Regression Model 
- Found the correlations between all the variables.
- Prepped a baseline model for Sprint 3 

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
|             |          |   |
|             |          |   |

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

Final shape including dummy variables is (62234, 189)
