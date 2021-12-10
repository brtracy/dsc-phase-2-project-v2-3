# Real Estate Investing in King County, WA
***

## Project Overview

This project uses multiple linear regression modeling to analyze house sales to build a predictive model. 

### Business Problem

There is a new real estate investor in Seattle that has contracted us to build a predictive model that could be used to predict the price of any particular home in King County, Washington. The goal is to compare that prediction to the current sale price in order to allow the investor to decide if they should buy it given that the home may be under-valued.

### The Data

The home sale data is provided to us from another firm, and encompases 21,597 homes sold in King County between May of 2014 and May of 2015. It includes 21 features for each home that conern both the makeup of the home, the lot the home is on, quality/condition, and location data. Our target is the sold price of the homes.

### The process

After initial data exploration to familiarize ourselves with the contents, we went through each feature one by one to learn about what the feature explained, the values and ranges contained in them, and their relation to the sale price.

Some features were initially removed from modeling, like 'id' and 'date' because there was no relationship between them and price. Others had some null values that needed addressing. A handful of feature are categorical, and had to be converted for modeling as well. 

The modeling approach began with a baseline model with which we were able to further remove predictors from consideration. After baseline, we spent time going through the removed predictors and attempting to engineer new features to include in our model that would improve it as well as allow us to use all the data that was collected.

Each iterative model added one or several new features that were included in evaluation, with futher decisions about inclusion or exclusion of these new features. Once we were comfortable with the model based on encoded and engineered features, we performed our train/test split, log transformed the price data to be more normal, and built the final model.


### Conclusions

The final model can explain about 72% of the variation when scored against testing data, across 32 predictors. The final model is also the closest of any of the iterative models to meeting all assumptions for linear regression. The square footage of the home seems to be the primary driving predictor of price. Other predictors which have a positive effect on price include the status of the property as being waterfront, that it has a view, is renovated (recently), and is in excellent condition.


### Next Steps

Through the process, our modeling showed improvement, but it's still not great. It's our responsibility to the stakeholder to inform them that the model should not be the only decision maker for purchasing a home. There are likely additional features that affect home price we either don't have the data for or haven't engineered yet.

Some things that are important to home price could include relative location to amenities (like grocery stores, entertainment, restaurants, etc), schools, crime, relative location to public transportation, and others.