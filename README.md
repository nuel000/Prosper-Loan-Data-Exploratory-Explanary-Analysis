# Prosper Loan Data Exploration
## by Emmanuel Momoh


## Dataset

> The data set contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others.The dataset can be found [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv),with feature documentation available [here](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0).

## Summary of Findings

> At the begining of the investigation, I performed preliminary wrangling by converting Income Range and ProsperRating to categorical variable, this returns the income/Prosper rating classes with the categories and orderedness. I also seperated date loan Originated into day, month and year, so as to capture the year of the loan created. After plotting a bargraph of borrower rate by year, I discovered an interesting insight that borrower rate was highest at 2013 than other years.
During the exploration, I also discovered that the number of loans generated increased with time (years) and there seem to be more current loans than any of other loan statuses. The Days of delinquent has a negative relationship with prosperscore (though Prosper score is an ordinal variable).Finally, income range has a positive relationship with loan amount originated, this is expected because borrowers with higher monthly income will tend to receive higher loan amount.


## Key Insights for Presentation

> For the presentation, I focused majorly on the influence of ProsperScore and Prosper Rating on other variables
such as  Income Range, Employment Status, wether or not the Borrower has a home and Loan's current days of Delinquent.I start by looking at the relationship between Prosper Score and Income range, followed by the Loan's current days of Delinquent (under the bivariate plot), then plotted the variables using a boxplot and lineplot respectively.Afterwards, I looked at how most numeric variables faired with each other. To start,
I use the heatmap to crossplot variables like 'LoanOriginalAmount', 'BorrowerAPR', 'StatedMonthlyIncome','LoanMonthsSinceOrigination', and 'LoanCurrentDaysDelinquent'. From the visualizations I noticed the following

* ProsperScore tends to increase as Income Range Increases, which means both variables are positively correlated (borrowers earning $100,000+ tend to have highest prosper scores than the rest)

* High number of days delinquent, the lower Prosper and vice-versa. Therefore, its safe to say borrowers with high prosper score hardly default in loan repayment

* Employement seems to be a significant factor that affects the prosper Rating, in that those who are employed seemed to have higher prosper ratings in that group.

*The loan original amount is positively correlated with the stated monthly income, it makes sense since borrowers with more monthly income could loan more money. 

For the multivariate plots, we can see from the plot, ProsperScore and Home owner's Status is almost evenly distributed between all categories of income range except for those that are not employed, those with no imcome and income range from $1-24,999. These set of borrowers tend to have non-home owners popuplar amongst them