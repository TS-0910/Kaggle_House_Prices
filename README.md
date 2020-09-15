# Kaggle - House Price
## Quick Intro
This is one of the most famous competition on Kaggle.<br/>
[Here](https://www.kaggle.com/c/house-prices-advanced-regression-techniques) is the detailed description, but in a nutshell, the gist of this competition is to **predict the house prices based on features such as the size of the garage, living room, overall quality etc**.<br/><br/>

Please see [here](https://github.com/TS-0910/Kaggle_Housing/blob/master/house-price-ts-0910.ipynb) to see my further analysis on Kaggle!

## Approach
I used the basic idea of [Pedro Marcelino's example solution](https://www.kaggle.com/pmarcelino/comprehensive-data-exploration-with-python) to approach the features, which is<br/>
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
I thought this score is not bad, but for getting a better score, I could potentially take log of 1stFlrSF and use it as well. (I basically treated TotalBsmtSF and 1stFlrSF the same, but TotalBsmtSF includes zero values) <br/>
Also, by using different machine learning methods and choosing the best result, and combining other contestants approaches and results, I could get a better score too. 
