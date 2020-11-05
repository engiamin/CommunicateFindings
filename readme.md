# Prosper Loan Data: Exploratory Analysis
## by Engi Amin


## Dataset

The prosper loan dataset is financial dataset that shows the current status of loans by Prosper Marketplace, Inc. Prosper is a San Francisco, California-based company specialized in peer-to-peer lending industry (https://www.prosper.com/). The dataset consists of 113937 data entries for 81 variables including characteristics of the borrower, loan and investors.

The goal of this analysis is to explore the factors that affect a loan’s outcome status.


The main feature of interest (response variable) is `LoanStatus` which defines the current status of the loan: Cancelled,  Chargedoff, Completed, Current, Defaulted, FinalPaymentInProgress, or PastDue.

The features that would support the investigation (independent variables) are: 
- `Term`: the length of the loan expressed in months.
- `ProsperRating (numeric)`: The  Prosper Rating assigned at the time the listing was created.
- `ProsperScore`: A custom risk score built using historical Prosper data. The score ranges from 1-10, with 10 being the best, or lowest risk score.
- `ListingCategory`: The category of the listing that the borrower selected when posting their listing
- `EmploymentStatus`: The employment status of the borrower at the time they posted the listing.
- `EmploymentStatusDuration`: The length in months of the employment status at the time the listing was created.
- `IsBorrowerHomeowner`: A Borrower will be classified as a homowner if they have a mortgage on their credit profile or provide documentation confirming they are a homeowner.
- `DebtToIncomeRatio`: The debt to income ratio of the borrower at the time the credit profile was pulled.
- `IncomeRange`: The income range of the borrower at the time the listing was created.
- `LoanOriginalAmount`: The origination amount of the loan.
- `CurrentCreditLines`: Number of current credit lines at the time the credit profile was pulled.

The original dataset was composed of 113,937 loan records with 81 features. After the cleaning process, the dataset was composed of 77,524 loan records with 12 features.

## Summary of Findings

The univariate exploratory analysis showed that 6.8% of its borrowers have been charged off or defaulted which will be interesting to focus on in the following analysis. Also, most of the borrowers have debt consolidation loans with loan amounts varying largely. Most of the borrowers are employed homeowners with a medium income asking for a 3-year term loan. Prosper gave a medium rating a score to most of its borrowers.

The bivariate exploratory analysis showed that borrowers who have defaulted have a higher median of debt-to-income ratio than all others. Most of those who defaulted reported 'other' in their listing. This requires Prosper to look into more detail into the listings of their borrowers. In addition, most of those who default have high or medium income rating not low. There is, also, a positive linear relation between the current number of credit lines and debt-to-income ratio. A borrower with a higher debt-to-income ratio is likely to have many credit lines.

The multivariate exploratory analysis showed that current borrowers who have highest debt-to-income ratio are not home owners and those who ask for higher orginal loan amount are home owners. It also showed that defaulted and charged off borrowers are mostly home owners and have mostly asked for loans less than 20,000 dollars. Borrowers with complete or almost complete payments have mostly asked for loans less than 20,000 dollars and have low debt-to-income ratio.

The analysis shed light on the relation between the original loan amount and Prosper's score, which ensures that Prosper grants larger loans only to borrowers with the highest scores who are less likely to default. The relation between the number of credit lines and debt-to-income ratio which is a red flag for risk analysts to watch for. If a borrower has too many credit lines, then they are not doing a great job managing their debts.


## Key Insights for Presentation

The presentation focused on three main dimensions:

**(1) The distribution of loan statuses of Prosper**

The majority of loans in the dataset are still current (67.7%), 2.4% are past due and 6.8% have either been charged-off or defaulted. This puts a responsibily on risk-analysts at Prosper to keep good track of their current borrowers.

**(2) How debt-to-income ratio affects loan status**
Borrowers who have defaulted have a higher median of debt-to-income ratio than all others. This is a very important red flag for risk analysts. 

**(3) The Interplay of Loan Original Amount, Debt to Income Ratio and Home Ownership**

**Current Borrowers**
- Those who have highest debt-to-income ratio are not home owners.
- Most of current borrowers who ask for higher orginal loan amount are home owners.

**Default and Charged off Borrowers**
- Are mostly home owners.
- Have mostly asked for loans less than 20,000 dollars.

**Borrowers with Complete or almost Complete Payments**
- Have mostly asked for loans less than 20,000 dollars.
- Have low debt-to-income ratio.

## Final Conclusion
It looks like Prosper is keeping very good track of the loan statues and their borrowers' characteristics making sure that most of the borrowers are employed, have medium to high income and that loans that default are kept at minimum.