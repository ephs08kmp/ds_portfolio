# Frac Method Analysis

While hotly debated, hydraulic fracturing is used after the drilling of an oil or gas well is complete.  Hydraulic fracturing uses fluid and other materials to create small fractures in a rock formation in order to stimulate the production of further oil and gas from the well.  While water and sand are the major components of this fluid, each individual operator has say over what else is added to this fluid.  There are many different schools of thought behind the use of individual additional ingredients without much evidence to support the use of one method over another.  Fortunately well operators are required to keep detailed records of the ingredients used, including the amount of such ingredients.  Here I will explore three methods of fracing a well, adding slickwater friction reducers, using gelling agents, and also cross-linking the gel, along with the production from each type of well to help well operators make better decisions as to the chemicals they are adding to their frac fluids.

For this project, I used linear regression, random forest regression, random forest quantile regression, and gradient boosting regression.  Overall, the models that explained the most variance in the data was the random forest regression model, and the random forest quantile regression model.  These models had R-squared values of 0.5337 (+/- 0.13) and 0.5335 (+/- 0.13), respectfully.  The gradient boosting regression model was not far behind with an R-squared value of 0.5040 (+/- 0.10), however the linear regression model explained the least amount of variance in the model with an R-squared score of 0.3236 (+/- 0.08).  The Random forest models were both able to paint a picture of the importances of different well and frac features, notably that the slickwater method has the greatest odds of increasing production, followed by the cross-linked gel method.  The well features that had the greatest odds of increasing production were a vertical depth of around 6600 ft, a horizontal length of about 2 miles, and using over 600 pounds of sand per foot of well drilled.  Well operators can use this information to optimize the production of their wells and minimize the impact of ineffective methods.

The production data I used was extacted from the [Colorado Oil and Gas Comission Information System (COGIS)](https://cogcc.state.co.us/data.html#/cogis) through a proprietary service provided by [DrillingInfo.com](DrillingInfo.com).  The detailed ingredient lists for each well were pulled from the [FracFocus Chemical Registry](http://fracfocusdata.org/).

### Installation
Download the following from above:
__For Data Cleaning and Exploration__
All raw data sets were too large to upload to github.  They have been uploaded to [GoogleDrive](https://drive.google.com/drive/u/0/folders/1XvwIHSMJVQs7U-nzpQhcedv4LWQ8Ta7J) instead.
- __Raw Data Files:__
    - `2017_prod_reports.csv`, which includes Colorado well production by month since 1990.
    - `DHJZ6-17-18Wells.CSV`, which includes the information on all Colorado well production
    - `dj hz 6-17-18 Production Time Series.CSV`, which contains production for each month for each well in Colorado
    - `bakkenWells.CSV`, which contains the Montana raw data
    - `DI Engineering Explorer well roll up.xlsx`, which contains the Oklahoma and Texas well production 
    - `FracFocus` folder, which contains csv files from the FracFocus Registry
- __Clean Data Files:__
    - `fracwells_co.csv`, which contains cleaned and merged data on well production and fracing methods for Colorado.
    - `fracmethod_clean.csv`, which contains cleaned frac method data from across the United States, which was used for merging with individual state production data.
- __For Modeling:__
    - `cofeatures.csv`, which contains cleaned and merged data with engineered and non-engineered features for Colorado.
    - `mtfeatures.csv`, which contains cleaned and merged data with engineered features for Montana.
    - `okfeatures.csv`, which contains cleaned and merged data with engineered features for Oklahoma and Texas.

### Usage

__Data Cleaning:__ Run all cells in the `2_Frac_Production_Data_Cleaning.ipynb` file using a jupyter notebook.

__Exploratory Data Analysis:__ Run all cells in the `3_Frac_Production_Analysis.ipynb` file using a jupyter notebook.

__Modeling:__ Run all cells in the `4_Frac_Production_Modeling_CO.ipynb` file using a jupyter notebook.
 
 __Multi-States Modeling:__ Run all cells in the `5_Frac_Production_Multi_States.ipynb` file using a jupyter notebook


### Extending this
If you want to extend this work, here are a few places to start:
- Explore each state individually to determine if there are differences in the features that are important for predicting the production
- Gather more data on the perforation intervals to determine how the spacing of perforations impacts the production
- Complete this analysis on more of the high-oil and gas producing states to increase the number of wells and therefore reduce the variability in the data
- Streamline the data collection and reporting so that there is more consistency in the data to then get a more consistent result
