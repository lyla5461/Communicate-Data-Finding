# Prosper Loan Data Exploration

## by Yao Liu


## Dataset

This dataset contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others. 

Since there are too many variables in the csv file, I only select relevant columns like Credit Rating, Term, Borrower Rate, Emplotment Status, Credit Score Range, Income Range, and Loan Original Amount. 

By looking at the dataframe's first few rows and its statistics, I found that credit ratings are stored in two columns. So I combine them into one column as Rating and dropped the initial two columns. In addition, the credit score has lower and upper range stored in two columns, I decided to take the mean of the lower and upper range as the new Credit Score variable, which is easier for later analysis. Furthermore, the income range column contains categories should be part of $0 category, so I changed the Not Displayed and Not Employed as $0. I also dropped rows with missing values to make the dataframe clean. Lastly, I convert IncomeRange and Rating into ordered categorical type, this will make visualiztions clearer and easier to follow.


## Summary of Findings

In the exploration, I found that there was a negative relationship between the borrower rate of a loan and borrower credit score. Although the correlation between these two variables is not very high, after I plot the average borrower rate across all credit scores, I saw a downward sloped line. 

Besides the main variables of interest, borrower rate also has some relationships with other three loan's features like term, rating, and income range. Rating has the most obvious negative relationship with borrower rate, that is, the higher the rating, the lower the borrower rate. The other two variables' relationships with borrower rate is less obvious, but I can still see that longer term loans or lower income borrower tend to get higher borrower rate. 


## Key Insights for Presentation

In the presentation, I only show the main four features of loans that have impact on borrower rates. I start by showing the distribution of variable under study - borrower rate.

Secondly, I display the relationship between borrower rate and each of the categorical variables individually. I use the violin plots to better show the distribution of the categorical variable and trend agaist borrower rate. 

Lastly, to make the effect clearer, I controll for the credit score variable, and show the impact of different loan's rating and term on the borrower rate.