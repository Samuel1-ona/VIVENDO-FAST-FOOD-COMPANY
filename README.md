# VIVENDO-FAST-FOOD-COMPANY

**Vivendo** fast food company in Brazil with over 200 outlet 
Customers often claim compensation from the company for food poisoning. The legal team processes these claims.The legal team maintains offices in RECIFE, SAO LUIS, FORTALEZA, and NATAL.The legal team wants to improve how long it takes to reply to customers and close claims.


![1000_F_351024684_qRJBZa0XlvKs5bKDHVqlcbVF2ux4tDga](https://user-images.githubusercontent.com/68438893/233087861-39c7b6b9-bf57-4e6d-aaf2-33b4a11c8d66.jpg)


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

#TOOLS USED FOR THE ANALYSIS 

1.EXCEL
2.POWER BI

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

#PROBLEM STATEMENTS

The head of the legal department wants a report on how each location differs in the time it
takes to close claims.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

#DATA

**The dataset contains one row for each claim**.



1.Claim_id column :   Nominal. The unique identifier of the claim. Missing values are not possible due to the database structure.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

2.Time_to_close column :  Discrete. The number of days to close the claim. Any positive value. Replace missing values with the overall median time to close.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

3.Claim_amount column :  Continuous. The initial claim requested in the currency of Brazil,rounded to 2 decimal places. Replace missing values with the overall median claim amount.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

4. Amount_paid column :  Continuous. Final amount paid. In the currency of Brazil. Rounded to 2 decimal places. Replace missing values with the overall median amount paid.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

5.Location column:  Nominal.  Location of the claim, one of “RECIFE”, “SAO LUIS”, “FORTALEZA”, or “NATAL”.  Remove missing values.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

6. Individuals_on_claim column :  Discrete. Number of individuals on this claim. Minimum 1 person. Replace missing value with 0.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

7. Linked_cases column : Nominal.  Whether this claim is linked to other cases. Either TRUE or FALSE. Replace missing values with FALSE. 

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

8. Cause column : Nominal. Cause of the food poisoning. One of “vegetable”, “meat” or “unknown”. Replace missing values with ‘unknown’.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------
                                                     
                                                     
                                                     
                                                     
                                                     
                                                     
                                                     
                                                     
                                                     
                                                     
                                                     
                                                     













                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                      
                                                        
                                                        











