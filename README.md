# VIVENDO-FAST-FOOD-COMPANY

# INTRODUCTION

**Vivendo** fast food company in Brazil with over 200 outlet 
Customers often claim compensation from the company for food poisoning. The legal team processes these claims.The legal team maintains offices in RECIFE, SAO LUIS, FORTALEZA, and NATAL.The legal team wants to improve how long it takes to reply to customers and close claims.


![1000_F_351024684_qRJBZa0XlvKs5bKDHVqlcbVF2ux4tDga](https://user-images.githubusercontent.com/68438893/233087861-39c7b6b9-bf57-4e6d-aaf2-33b4a11c8d66.jpg)


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# TOOLS USED FOR THE ANALYSIS 

1.EXCEL
2.POWER BI

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# PROBLEM STATEMENTS

The head of the legal department wants a report on how each location differs in the time it
takes to close claims.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# DATA

**The dataset contains one row for each claim**.



1.Claim_id column :   Nominal. The unique identifier of the claim. Missing values are not possible due to the database structure.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

2.Time_to_close column :  Discrete. The number of days to close the claim. Any positive value. Replace missing values with the overall median time to close.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

3.Claim_amount column :  Continuous. The initial claim requested in the currency of Brazil,rounded to 2 decimal places. Replace missing values with the overall median claim amount.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

4.Amount_paid column :  Continuous. Final amount paid. In the currency of Brazil. Rounded to 2 decimal places. Replace missing values with the overall median amount paid.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

5.Location column:  Nominal.  Location of the claim, one of “RECIFE”, “SAO LUIS”, “FORTALEZA”, or “NATAL”.  Remove missing values.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

6.Individuals_on_claim column :  Discrete. Number of individuals on this claim. Minimum 1 person. Replace missing value with 0.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

7.Linked_cases column : Nominal.  Whether this claim is linked to other cases. Either TRUE or FALSE. Replace missing values with FALSE. 

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

8.Cause column : Nominal. Cause of the food poisoning. One of “vegetable”, “meat” or “unknown”. Replace missing values with ‘unknown’.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------
                                                     
 # DATA VALIDATION 
 --------------------------------------------------------------------------------------------------------------------------------------------------------------------
 
The original data is 2000 rows and 8 columns 14 rows was removed due to duplicate . I started by looking for missing values and spelling mistakes in each column. Because of a data type error, I also changed the format of claim_amount by eliminating the currency signs from each and every value in the column, and I changed the column name to claim_amount(R$). The new column name, Amount_paid(R$), was created by appending (R$) to the end of the original Amount_paid column.

 The cause column contains a data entry spelling error, as I noticed that most instances of "vegetable" are written in lower case, while others use upper case "VEGETABLES." Because the majority of instances are written in lower case, I changed all 16 rows in which every upper case character was present to lower case, making the cause column distinct.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# STATING THE NUMBER OF MISSING VALUES

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
1.40 values in amount_paid are missing, and the overall median of amount_paid, 20105.7, was used to fill up the gaps.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

2.The Linked_case column has 26 missing values, all of which were changed to FALSE.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# DESCRIPTIONS
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

1.The Claim_id has 1000 distinct and 1000 unique values.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

2.The days in the Time_to_close column range from 76 to 518 days and all of their values are positive ( 222 distinct values, 62 unique) .

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

3.All initial claims are listed in the Claim_amount(R$) column and are made in Brazilian equivalent (R$) (1000 distinct values , 1000 unique).

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

4.The Amount_paid(R$) column contains a list of all final claims that have been made in Brazilian reals (R$) (982 distinct values , 981 unique).

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

5.As expected, the location column has 4 distinct locations.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

6.The number of individual claims is listed in the individual_on_claim column, with a range of 1 to 15 individuals per claim ( 15 distinct).

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

7.Linked_cases column lists all the connected claims, categorized as TRUE or FALSE.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

8.Cause column has three distinct causes.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

# DATA VISUALIZATION AND INSIGHTS

## What is the number of claims in each location?


In the data, there are four distinct sites, with RECIFE having the highest number of individual claims (7000) and NATAL having the lowest number of individual claims (2300).

![sum of individuals on claims by location](https://user-images.githubusercontent.com/68438893/233124771-ca2d716f-b2a3-473c-9a97-c727c7c523e3.png)


----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Explain whether the observations are balanced across categories of the variable location.

The observations are not balanced across categories of the variable location when considering the sum of claims in each location. The sum of claims for each location indicates the total amount of claims made in each location and allows us to compare the magnitude of claims between the locations.


In this case, RACIFE has the highest sum of claims with 7000, followed by SAO LUIS with 4100, FORTALEZA with 2500, and NATAL with 2300. The large differences in the sum of claims between RACIFE and the other locations suggest that the observations are not balanced.


To further confirm the extent of the imbalance, we can calculate the relative frequencies of claims in each location by dividing the sum of claims in each location by the total sum of claims and then multiplying by 100. This will give us the percentage of claims in each location.

For example, the relative frequency of claims in RACIFE is (7000/15900)*100 = 44.03%.
Similarly, the relative frequency of claims in SAO LUIS is (4100/15900)*100 = 25.79%,
in FORTALEZA is (2500/15900)*100 = 15.72%,
and in NATAL is (2300/15900)*100 = 14.49%.

From these calculations, we can see that the observations are not balanced across categories of the variable location when considering the sum of claims. The large differences in the sum of claims between RACIFE and the other locations suggest that RACIFE has a significantly higher number of claims compared to the other locations. Therefore, we should be cautious in drawing conclusions or making generalizations about the claims distribution based solely on these four locations.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Describe the distribution of time to close for all claims. Your answer must include a visualization that shows the distribution

The distribution of time to close for all claims can be described based on the number of claims made within each time range.


To further understand the distribution of time to close for all claims, we can calculate the relative frequencies of claims in each time range. We do this by dividing the count of claims in each time range by the total count of claims and multiplying by 100.

Relative frequency of claims for 100-199 days: (1419 / 1986) * 100 = 71.46%
Relative frequency of claims for 200-299 days: (484 / 1986) * 100 = 24.37%
Relative frequency of claims for 300-399 days: (53 / 1986) * 100 = 2.67%
Relative frequency of claims for 70-99 days: (24 / 1986) * 100 = 1.21%
Relative frequency of claims for 400 days and above: (6 / 1986) * 100 = 0.30%


From these calculations, we can see that the majority of claims (about 71%) were closed within the time range of 100-199 days. The number of claims decreases as the time range increases, with only 0.3% of claims taking 400 days or more to close. This suggests that the distribution of time to close for all claims is heavily skewed to the left, with the majority of claims closing within the first 200 days.

The legal team has more claims between 100 and 199 days compared to all other days distributions, making this period of time the time period with the highest number of individual food poisoning claims.

![count of individuals on claims by count of days](https://user-images.githubusercontent.com/68438893/233126373-7eedff49-49d6-489d-bd73-2ce73b2d7be5.png)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Describe the relationship between time to close and location. Your answer must include a visualization to demonstrate the relationship. 

RACIFE has the highest sum of claims with 7000, and also the highest time to close claims with 877. This suggests that the location with the highest sum of claims also had the longest time to close claims on average.

SAO LUIS has the second-highest sum of claims with 4100, and also the second-highest time to close claims with 513. This suggests that the location with the second-highest sum of claims also had the second-longest time to close claims on average.

FORTALEZA has the third-highest sum of claims with 2400, and also the third-highest time to close claims with 309. This suggests that the location with the third-highest sum of claims also had the third-longest time to close claims on average.

NATAL has the lowest sum of claims with 2300, and also the shortest time to close claims with 287. This suggests that the location with the lowest sum of claims also had the shortest time to close claims on average.

Therefore, we can observe a negative relationship between time to close and location, where locations with a higher sum of claims tended to have a higher average time to close the claims. This could indicate that there are differences in the efficiency of claims processing across locations, and that locations with a higher workload may have a longer processing time. 

![count of days to close by location and claims](https://user-images.githubusercontent.com/68438893/233126686-b8250487-5f77-4fe9-bcc6-e36a02700043.png)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

# RECOMMENDATION

To ensure that all claims are timely resolved in the area, more legal staff must be given to RACIFE. Additionally, a proportionate legal team that can make a difference in each area will be assigned to the place with the fewest claims.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

# CONCLUSION

We can see that most claims (approximately 71%) were resolved within the 100–199 day window. Only 0.3% of claims require 400 days or more to be resolved, and the number of claims declines as the time span widens.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
















                                                     
                                                     
                                                     
                                                     
                                                     
                                                     
                                                     
                                                     
                                                     
                                                     













                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                        
                                                        











