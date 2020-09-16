# Kaggle - House Prices
## Quick Intro (Here is [my detailed analysis on Kaggle](https://github.com/TS-0910/Kaggle_Housing/blob/master/house-price-ts-0910.ipynb))
This is one of the most famous competitions on Kaggle.<br/>
Here is [the overall description](https://www.kaggle.com/c/house-prices-advanced-regression-techniques), but in a nutshell, the gist of this competition is to **predict the house prices based on features such as the size of the garage, living room, overall quality etc**.<br/><br/>


## Approach
I used the basic idea of [Pedro Marcelino's example solution](https://www.kaggle.com/pmarcelino/comprehensive-data-exploration-with-python) to approach the features, which are<br/>
1.Basic idea of which features are important, and which can be eliminated<br/>
2.Transformation of important features using logs<br/>
<br/>
Then, I used machine leraning(light GBM) to predict the price.<br/>

## Result
RMSE = 0.1117 <br/>
R2 = 0.92638 <br/>
These are the scores based on the training data.<br/>
<br/>
When I used the actual test data and submitted it, RMSE was 0.13980.<br/> 
I thought this score was not bad, but to get a better score, I could potentially take log of 1stFlrSF and use it as well. (I basically treated TotalBsmtSF and 1stFlrSF the same, but TotalBsmtSF includes zero values) <br/>
Using different machine learning methods,choosing the best result, and combining other contestants approaches and results could improve the score too. 
