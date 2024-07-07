# Overview

This assignment was prepared as part of an interview process for an analyst role at a University IT Department. All of the numbers in the raw data source are fictional.  

## Assignment

File [IE_Raw_Data.xlsx](https://github.com/VikSil/PowerBI_Public/blob/trunk/University_Department_I%26E/IE_Raw_Data.xlsx) contains an example of I&E statement for a University IT Department. View the spreadsheet and via a short presentation address the following:

1. Identify the variances you believe should be investigated and provide some thoughts as to why you believe these may have presented themselves - considering recent economic activity and that we're in an IT context.
1. Suggest how you would take these forward into Q3 forecasting discussions with a Cost Centre Manager and any risks/opportunities you'd like to flag to the FP&A Manager.


## Solution 

File [IE_Analysis.pbix](https://github.com/VikSil/PowerBI_Public/blob/trunk/University_Department_I%26E/IE_Analysis.pbix) contains graphical analysis of the input data. The layout of the dashboard is as follows:
* __Top section__: A table of the raw input data as absolute numerical data of budget and actual income/expenses for each month, along with totals accross months and line items.
* __Center Left__: Bar charts of the budgeted and actual income totals per month as absolute numbers. 
* __Bottom Left__: Bar charts of the budgeted and actual expense totals per month as absolute numbers. 
* __Center__: Variance heatmap per line item and month as a percentage. Zero percent means actual income/expenditure being the same as budgeted. Positive percentage means a positive balance, i.e. higher than budgeted income or lower than budgeted expense. Negative percentage means a negative balance, i.e. lower than budgeted income or higher than budgeted expense. 100% either negative or positive means that there was no budget but actual income/expense occured.
* __Bottom Center__: Variance heatmap per line item and month in absolute numbers. Positive numbers mean positive balance, and negative numbers mean negative net balance.
* __Center Right__: Pie chart of all positive variances as percentage of total positive variance. Positive variance is higher than budgeted actual income or lower than budgeted actual expense.
* __Bottom Right__: Pie chart of all negative variances as percentage of total negative variance. Negative variance is lower than budgeted actual income or higher than budgeted actual expense.
* __Below Bottom Right__: Button to switch heatmaps and variance charts between income and expenditure. Button to remove all filters (Ctrl+click).

### Analysis

* On the income side the most notable positive variance comes from "Sales, Services & Trading" line item, with the highest surplus in January (1711%|158.10) and notable surplusses in October (552%|51.01) and March (608%|56.21). The highest shortfall of planned income comes from "Recharges" line item, with the largest shortfall in September (82%|-72.31).
<p align="center"><img src="https://github.com/VikSil/PowerBI_Public/blob/trunk/University_Department_I%26E/img/01_All_Income.png" title="Income Dashboard" alt="Income Dashboard" width="500"/></p>

