# Two Sample Hypothesis Testing for Conversions

## Summary

Walkthrough of the analysis process to determine if a new landing page resulted in increased conversions. 

This includes examination of the data, cleaning, visualization of distribution to determine the appropriate statistical test to be used culminating with the decision for recommended course of action.

The results show that there was no increase in converisons due to the new landing page.

## Data Source

Data sourced from the kaggle synthetic dataset [putdejudomthai][data_set].

## Analysis 

Detailed steps are outlined in the [jupyter notebook](./ecom_ab_hyptest.ipynb). 

>The notebook can be run locally or on kaggle. If run locally, the data files need to be manually downloaded to a data folder.

In the data cleaning step, we identified and removed errors where control and treatment groups were mislabeled and then removed duplicated records for some users. 
We did not lose a significant amount of data due to errors and duplication. The data type for the 'conversions' column was changed to a boolean for categorical analysis.

A bar plot visual was built to show the percentage of conversions within each group.

For categorical variables, we could use either the Z-test for proportions or the chi-squared test. We used the Z-test and based on the p value we saw that there was no statistical evidence to conclude that the treatment outperformed the control group for conversions.

[data_set]: https://www.kaggle.com/datasets/putdejudomthai/ecommerce-ab-testing-2022-dataset1/data