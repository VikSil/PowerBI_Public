# Overview

This assignment was prepared as part of an interview process for an analyst role at a University IT Department. All of the numbers in the raw data source are fictional.  

## Assignment

File [IE_Raw_Data.xlsx](https://github.com/VikSil/PowerBI_Public/blob/trunk/University_Department_I%26E/IE_Raw_Data.xlsx) contains an example of I&E statement for a University IT Department. View the spreadsheet and via a short presentation address the following:

1. Identify the variances you believe should be investigated and provide some thoughts as to why you believe these may have presented themselves - considering recent economic activity and that we're in an IT context.
1. Suggest how you would take these forward into Q3 forecasting discussions with a Cost Centre Manager and any risks/opportunities you'd like to flag to the FP&A Manager.


## Solution 

File [IE_Analysis.pbix](https://github.com/VikSil/PowerBI_Public/blob/trunk/University_Department_I%26E/IE_Analysis.pbix) contains graphical analysis of the input data. The layout of the dashboard is as follows:
* __Top section__: A table of the raw input as absolute numerical data of budget and actual income/expense for each month, along with totals accross months and line items.
* __Center Left__: Bar charts of the budgeted and actual income totals per month as absolute numbers. 
* __Bottom Left__: Bar charts of the budgeted and actual expense totals per month as absolute numbers. 
* __Center__: Variance heatmap per line item and month as a percentage. Zero percent means actual income/expense being the same as budgeted. Positive percentage means a positive balance, i.e. higher than budgeted income or lower than budgeted expense. Negative percentage means a negative balance, i.e. lower than budgeted income or higher than budgeted expense. 100% either negative or positive means that there was no budget but actual income/expense occured, or none of the budgeted resouce was tapped.
* __Bottom Center__: Variance heatmap per line item and month as absolute numbers. Positive numbers mean positive net balance, and negative numbers mean negative net balance.
* __Center Right__: Pie chart of all positive variances as percentage of total positive variance. Positive variance is higher than budgeted income or lower than budgeted expense.
* __Bottom Right__: Pie chart of all negative variances as percentage of total negative variance. Negative variance is lower than budgeted income or higher than budgeted expense.
* __Below Bottom Right__: Button to switch heatmaps and variance charts between income and expense. Button to remove all filters (Ctrl+click).

### Analysis

* On the income side, the most notable positive variance comes from "Sales, Services & Trading" line item, with the highest surplus in January (1711% | 158.10) and notable surpluses in October (552% | 51.01) and March (608% | 56.21). Most notable negative variance of income comes from "Recharges" line item, with the largest shortfall in September (-82% | -72.31).
<p align="center"><img src="https://github.com/VikSil/PowerBI_Public/blob/trunk/University_Department_I%26E/img/01_All_Income.png" title="Income Dashboard" alt="Income Dashboard" width="1000"/></p>

* On the expenses side, the most notable positive variance comes from "Equipment Purchases" and "Support Staff" line items. The highest savings in the former occured in November (38% | 93.41) and March (39% | 86.59). On the latter savings occured throughout October to March, with an exception of December, when there was a overexpenditure. Most notable negative variance of expenses comes from "Equipment Repairs and Maintenance" with significant overexpenditure in April (-882% | -127.37). Overexpenditures also occured on "Casual and Agency Staff", "Telecomms" and "Utilities" line items.
<p align="center"><img src="https://github.com/VikSil/PowerBI_Public/blob/trunk/University_Department_I%26E/img/02_All_Expenses.png" title="Expenses Dashboard" alt="Expenses Dashboard" width="1000"/></p>

* The above surplus in "Sales, Services & Trading" at the start fo calendar year may be related to settlement of accruals from December when increased overall economic activity is normally observed. Shortfall in "Recharges" may be related to the start of academic year, but would have to be further investigated.

* The above savings on "Equipment Purchases" and "Support Staff" are likely a result of simply failing to make planned equipment replacements and hirings. However, these savings are offset and surpassed by expenses on "[Equipment Repairs and Maintenance](https://github.com/VikSil/PowerBI_Public/blob/trunk/University_Department_I%26E/img/03_Expenses_Equipment.png)", when old equipment breaks, and "[Casual and Agency Staff](https://github.com/VikSil/PowerBI_Public/blob/trunk/University_Department_I%26E/img/04_Expenses_Agency_Staff.png)" that has likely been hired as a short-term solution to lack of staff when it is critically needed.

* The overexpenditures on ["Telecomms" and "Utilities"](https://github.com/VikSil/PowerBI_Public/blob/trunk/University_Department_I%26E/img/05_Expenses_Utilities.png) are explained by increasing cost of living and providers increasing prices on their services (this presentation was prepared in Q2 2024 in the UK that was recovering from a 30 year inflation peak).

* The expense line item "[Staff Training and CPD](https://github.com/VikSil/PowerBI_Public/blob/trunk/University_Department_I%26E/img/06_Expenses_Training.png)" has a significant overexpense in the month of April (-731% | -17.46), while in almost all other months none of the budget has been tapped. This is likely due to staff paying little attention to training until the fiscal year end (in the UK fiscal year ends on 5th of April), when 'use it or loose it' policy is applied.

* When planning for Q3 the following adjustments could be considered:
    * Allowing for a greater buffer for utilities payments, in case of further price increases.
    * Making sure that old equipment is replaced in a timely fashion, in order to avoid extra expenses on emergency repairs.
    * Increasing headcount of permanent staff (this could include hiring someone to take care of equipment) instead of relying of short-term staffing that costs more over time.
    * Distributing budgeted resources on "Staff Training and CPD" more evenly throughout the year, as it facilitates better knowledge and skill retention and more sustainable development of the staff.