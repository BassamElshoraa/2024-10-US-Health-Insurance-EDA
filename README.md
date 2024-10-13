# **US Health Insurance EDA**

| Contents 											 	   	|
| -------- 											 	   	|
| [Project Description](#Project-Description)			   	|
| [Dataset Overview](#Dataset-Overview) 		   		|
| [Columns Description](#Columns-Description)							|
| [Data Wrangling](#Data-Wrangling)					   		|
| [Data Cleaning](#Data-Cleaning)						   	|
| [Data Visualization](#Data-Visualization)					|
| [Conclusion](#Conclusion)									|
| [Built with](#Built-with)							   		|

## Project Description: 
Medical Insurance is a contract that requires an insurer to pay some or all of a person's healthcare costs in exchange for a premium, with the insurance typicallly pays for medical expenses incured by the insured. Insurance cost differs from each individual, certain variable may affect a person insurance cost to be higher or lower.
This project will analyze medical insurance cost in a dataset and exploring variables that may affect it. Further, this project will showcase data analysis skills to provide meaningful insight.

## Dataset Overview 
The dataset used in this analysis contains information about health insurance policies, coverage, premiums, and demographic details such as age, income, and region.

## Columns Description:
1. `age`: age of primary beneficiary.
2. `sex`: insurance contractor gender, male or female.
3. `bmi`: body mass index, providing an understanding of body, weights that are relatively high or low relative to height, objective index of body weight (kg/m2) using the ratio of height to weight.
4. `children`: number of children covered by health insurance/number of dependents.
5. `smoker`: is the beneficiary smoking? yes or no.
6. `region`: the beneficiary's residential area in the US; northeast, southeast, southwest, northwest.
7. `charges`: individual medical costs billed by health insurance, in USD.

## Data Wrangling:
Our data can be found on `insurance.csv` file provided on this repository. 

## Data Cleaning:
### Exploration Summery
1. our dataset consists of 1338 rows with 7 columns, and has no NaNs values.
2. `sex`, `region`, `children`and `smoker` coulmns needs to be casted into a categoy type
3. We need to drop one duplicate row.

We endded up with a datafram of 1337 rows and 7 columns after completing the cleaning process. 

## Data Visualization
Using `Matplotlib` and `Seaborn`, we made several meaningful visuals and charts to help us gain informative insights regarding any correlation between attributes in our dataset.

## Conclusion
- our dataset consists of 1337 rows with 7 columns, and has no NaNs values.
- The age distribution ranges from a minimum of 18 to a maximum of 64 years.
- The median age is 39 and the Mean is 39.2 , indicating that half of the insured individuals are younger than this age.
- The first quartile (27 years) and the third quartile (51 years) suggest that the majority of insured individuals are between their late twenties and early fifties.
- Notably, there are 22 insured individuals who are exactly 64 years old, indicating a significant presence of this age group within the insured population.
- There are no outlier values in the Age distribution in the data.
- The BMI distribution of the Insured approximately follows a normal distribution with a Mean of 30.66 and Median of 30.4.
- There are a total of 9 outlier values in the BMI distribution, all in the higher side. The highest BMI observed is 53.13.
- The insured individual with the highest BMI (53.13) is 18 years old and doesn't have children, paying 1163.46 in charges. This reflects common underwriting practices where age and health metrics influence insurance premiums.
- The distribution of charges is heavily right-skewed (mean > median), with a mean of 13,279.12 and a median of 9,386.16, indicating a few individuals with very high charges significantly influence the average.
- The lowest charge recorded is 1,121.87, while the highest is a substantial 63,770.43, highlighting a significant range in premium payments.
- Out of 1,337 data points, there are 139 outlier values, all of which are in the higher end of the distribution, indicating a few individuals face exceptionally high charges.
- The insured individual with the highest charges (63,770.43) is a 54-year-old female No-smoker with a high BMI.
- The person with the highest BMI (obese, or least healthy, based on available data) is also one of the youngest (male, 18, non-smoker.) He is paying less premium charges than the mean(which, we note, is affected by extreme outlier values of charges like the person above), but significantly more than the median. This is in line with our basic understanding of underwriting rules.
- The dataset is almost evenly distributed among genders, with 675 Males (50.5%) and 662 Females (49.5%).
- Average premium charges for smokers are indeed significantly higher than non-smokers.
- Of the total 1337 insured, 274 (20.5%) are smokers and the rest are non-smokers.
- Among 274 smokers, proportion of males (159) are higher than females (115).
- The average insurance premium for smokers are significantly higher than non-smokers.
- All four regions are represented approximately evenly in the dataset.
- In the dataset, approximately 85% (1137/1337) of the insured have less than 3 children.
- We can conclude that the premium charges show a weak positive correlation with Age and BMI of the insured, and a strong positive correlation with smoking habit.

## Built with:		
- JupyterLab	
- Python3	   	
- Pandas		
- Numpy			
- Matplotlib	
- Seaborn		
