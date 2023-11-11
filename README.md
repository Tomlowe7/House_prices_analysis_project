# House_prices_analysis_project

![image](https://github.com/Tomlowe7/House_prices_analysis_project/assets/126796950/2dd69110-243d-4e1c-8f49-bfb70e8bfa8f)


## Abstract
The Database of House Prices contains a lot of features of homes that have been put up for sale in Ames City, Iowa (USA) from 2006 until 2010. From this Database files we can learn about the judgment of people when they want to buy or sell a house. We will draw conclusions according to the ratio between the prices of different houses (with different features) that were put up for sale. 

As part of the project objective, I will seek to answer what are the features that affect the most on house prices (for better or for worse), are there any factors that don't affect house prices at all? Which are the more popular neighborhoods where more sales of buildings have been made there over the years? Which neighborhoods are considered to be more upscale? and what is the importance of home remodeling to achieve a successful sale, at an above-average price? 

Moreover, I will examine the impact of the global financial crisis of 2007–2008 (GFC), which was a severe worldwide economic crisis and the most serious financial crisis since the Great Depression. This project will obviously concentrate on the bursting of the United States housing bubble, and it's destructive effect on the American Hosue Market prices. 

## Data Description 

#### The Raw data that i used has 81 columns, aka, 81 features of houses that went up for sale in Ames City, Iowa (USA). Are they all important to my objective? I can't determine this yet. I will begin by reviewing the factors that I hypothesize to might be significant in their impact on house prices:

<b> LotArea: </b> Lot size in square feet (continues value of size). 

<b> Neighborhood: </b> 25 Neighborhood locations within Ames city limits (Categorial values: textuall names).

<b> BldgType: </b> Type of dwelling (Categorial values: 1Fam=Single-family Detached, 2FmCon=Two-family Conversion, Duplx=Duplex, TwnhsE=Townhouse End Unit, TwnhsI=Townhouse Inside Unit).

<b> HouseStyle: </b> Style of dwelling (Categorial values: 1Story=One Story, 1.5Fin=One and one-half story: 2nd level finished, 1.5Unf=One and one-half story: 2nd level unfinished, 2Story=Two story and so on...).

<b> OverallQual: </b> Rates the overall material and finish of the house (Discrete Ordinal values: from 1=very poor to 10=very excellent).

<b> OverallCond: </b> Rates the overall condition of the house (Discrete Ordinal values: from 1=very poor to 10=very excellent).

<b> YearBuilt: </b> Original construction date (Discrete Datetime values that determine the age of the house).

<b> YearRemodAdd: </b> Remodel date (Discrete Datetime values; Will be the same value as construction date if no remodeling or additions has been made).

<b> ExterQual: </b> Evaluates the quality of the material on the exterior. (Categorial values: Ex=Excellent, Gd=Good, TA=Average, Fa=Fair, Po=Poor). There is another feature called <b> ExterCond </b> which evaluates the present condition of the material on the exterior and gets the same categorial values. 

<b> BsmtCond: </b> Evaluates the general condition of the basement. (Categorial vaules are the same as ExterQual and ExterCond, but with an extra value of NA=No Basement).

<b> HeatingQC: </b> Heating quality and condition. (Categorial values: Ex=Excellent, Gd=Good, TA=Average, Fa=Fair, Po=Poor)

<b> CentralAir: </b> Central air conditioning (Binary values: N=No, Y=Yes).

<b> FullBath: </b> Number of Full bathrooms above grade (Discrete values that indicates the number of full bathroom in the house). There is another feature called <b> HalfBath </b> who do the same for halfbaths. 

<b> KitchenQual: </b> Kitchen quality. (Categorial values: Ex=Excellent, Gd=Good, TA=Average, Fa=Fair, Po=Poor)

<b> TotRmsAbvGrd: </b> Total rooms above grade (Discrete values that indicates the total number of bedrooms in the house (does not include bathrooms, but does include basement bedrooms). 

<b> GarageCars: </b> Size of garage in car capacity (Discrete values that indicates the number of cars that can fit the garage of the house).
 
<b> YrSold: </b> Year Sold YYYY. (Discrete Datetime values).

<b> SaleCondition: </b> Condition of sale. (Categorial values: Normal=Normal Sale; Abnorml=Abnormal Sale -  trade, foreclosure, short sale; AdjLand=Adjoining Land Purchase; Alloca=Allocation - two linked properties with separate deeds, typically condo with a garage unit; Family=Sale between family members; Partial=Home was not completed when last assessed, its associated with New Homes). 

The Database file has <b> 81 Columns </b> that can get a varity of value types (=81 House Features, before any concessions).
<b> 1460 Rows </b> = 1460  Observations of houses for sale in Ames City, Iowa between the years 2006-2010 (n=1460).

####  In this project, I will use EDA and Feature Engineering to analyze the Iowa Housing Market and to identify features that influence the prices of house sales, hence my objective variable is 'SalePrice'.


## Exploratory Data Analysis (EDA)


The objective variable, SalePrice has Mean value of 180,921usd, with Standard deviation of 79,443usd, and a Median of 163,000usd.

The cheapest house in this database was sold at Minimum price of 34,900usd, and the most expensive house in this database was sold at Maximum price of 755,000usd.

The LotArea feature, regrading the size of the houses has Mean value of 10,517 square feet, and Median value of 9,478.5, which means half of the houses for sale in Ames City are smaller than 9,478.5 square feet. 

Other interesting stats are the OverallQual and OverallCond, which indicates that the Average Quality of the houses for sale in Ames City is 6.01 (on a scale of 1-10), and the Average Condition of the houses for sale is 5.58, respectively. This indicates that the living standards in this city is relatively reasonable.

YearBuilt feature indicates the age of the houses. The oldest house was built in 1872, and the newest house was built in 2010. The Median points out that half of the houses that went up for sale were built before 1973, which is pretty old. This could be a hint of a shortage trend in new construction in Ames City. 


#  Main Takeaways:

- The house features: Pool quality, Miscellaneous feature, Type of alley access to property, Fence quality, Fireplace quality, are all not significant enough to influence the house prices.
- The Sale Condition of the house is not significant enough to have any impact on house sale prices, mainly because the vast majority of real estate transactions are made under Normal Sale Conditions. 
- I couldn't find anything that would suggest that there is a strong link between the Size of the house and it's Sale Price.
- The 3 most popular house styles in Ames City, Iowa for 2006-2010 are: One story houses, Two story houses, and 1.5 story (with 2nd level finished). One story and Two story houses have positive influence on house sale prices, but I can't determine the same on the 1.5 story house which had no strong connection with higher prices. 
- There is a clear linear relationship between the Quality of the House and it's Selling Price. The Overall Quality of the House is an important factor that influence positively on the Price. However, The Overall Condition of the House did not had such strong link with the House Sale Price. I could still identify a positive trend that can hint to a correlation, but it's not that unambiguous like the effect of the Overall Quality.
- The TOP3 Neighborhoods for the most house transactions that took place there are (Quantity wise) during 2006-2010 in Ames City are: North Ames (Names) with more than 250 houses sold, College Creek (CollgCr) with ~150 houses sold, and the Old Town with more than 100 houses sold.
- The TOP3 Luxury Neighborhoods where the most expensive houses were sold for over a mean price of 300,000usd during 2006-2010 in Ames City are: Northridge, Northridge Heights, Stone Brook. 
- The Overall Quality and Condition of the houses in the Ames City real estate market during 2006-2010 did not differ significantly over the period. And old houses doesn't necessarily mean cheap houses.

<b> Main Outcome: </b> My conclusion from this project is that the major factor that influence house sale prices in Ames City, Iowa, during the year 2006-2010 is the catastrophic effect of the bursting of the US housing market bubble which slashed house prices and had a negative impact all over the world.
