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
















                                                     
                                                     
                                                     
                                                     
                                                     
                                                     
                                                     
                                                     
                                                     
                                                     













                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                        
                                                        











