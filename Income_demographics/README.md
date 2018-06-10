
# Gender Pay Gap: Predicting income based on demographic data

What are the biggest indicators of a person's income? Their education level? Race? Gender? Age? What are demographic indicators that improve a woman's pay to help close the gender gap?

For this project, I used logistic regression, K nearest neighbors classifer, random forests, and a gradient boosting classifier. Overall, the model that most accurately predicted if a person earned over \$50,000 was the gradient boosting classifer, followed by the logistic regression model. These models had ROC AUC scores of 0.9097, and 0.9054, respectfully. The random forest model followed closely behind, with a ROC AUC score of 0.9050, and the K nearest neighbors classifier was the least accurate in its predictions of income categories, with a ROC AUC score of 0.8453. Both the gradient boosting classifer and the logistic regression models were able to paint a picture of the importances of the different demographic features that impact whether or not a person earns over \$50,000, most notably age, being married, hours worked per week, and having an advanced degree.   

The data I will be using is extacted from the [1994 census bureau database](http://www.census.gov/ftp/pub/DES/www/welcome.html).  This dataset contains census data from approximately 32,000 working people over the age of 16, who made over 100 dollars that year, and who are representative of the larger population.  For each of these people, the dataset tracks a person's age, native country, marital status, education, employment, capital gains and losses as well as the target variable, whether or not the person's income was over 50,000 for that year.  

Note that according to the [Bureau of Labor and Statistics](https://www.bls.gov/data/inflation_calculator.htm), due to inflation and cost of living increases, \$50,000 in 1994 would be worth approximately $84,500 in 2018. 

### Installation
Download the `adult.data.csv` file, above, or through the [UCI Machine Learning Repository link](https://archive.ics.uci.edu/ml/datasets/adult):

### Usage
Run all cells in the `Gender_Pay_Gap_Modeling` file using a jupyter notebook.
Summary of the analysis and modeling can be found in the `Predicting Income Based on Demographic Data.pptx` file. 

### Extending this
If you want to extend this work, here are a few places to start:

- Explore how these factors have changed since 1994
- Compare these indicators of higher income to those in other developed countries
- Extend modeling to determine which indicators are most important for predicting if minority races earn higher incomes
