# lol_project_home_pricing
Predict future housing prices 
# About
  * I will be using the Ames Housing Data set from Kaggle to create a model that is capable of predicting housing prices in a given market. 
# Initial Write-Up
  1. What is the question you hope to answer?
    * I hope to be able to accuratley predict with a high degree of certainty what the price of a home will be. 
  2. What data are you planning to use to answer that question?
    * I am using the Ames Housing Data set from Kaggle.  
  3. What do you know about the data you're using so far?
   * I know that there are 79 explanatory variables in my data set. I also know that this data is populated from housing sales in Ames, Iowa. 
  4. Why did you choose this topic?
    * I chose this project because in a past life I worked in the resdidential housing industry and know a great deal about residential homes. I am also in the market to be a first time home buyer and it would be interesting to create a prediction model for home sale prices. 
  
  
# Project Check-In
  1. What data have you gathered, and how did you gather it?
   * I have gathered sales data for home sales in Ames, Illinois with a year sold range between 2006 and 2010. I gathered a test set and train set from Kaggle. I will be utilizing the "House Prices: Advanced Regression Techniques" compaetition for this project. 
  2. How have you explored the data and what insights have you gained as a result?
   * I started exploring this data by just getting a feel for what it looked like. In the training set there are 80 descripitive columns giving varying information about the home and 1 column that gives the sale price. In this data there are 1460 rows each row with a unique ID to identify the house that was sold. As a preliminary look into the data I created a correlation matrix to try and pick out the descriptive columns that would have the most correlation with sale price. This was some what difficult to picture with 80 inputs. I will likely try to reduce the descriptive columns down to those that are the most pertinent.
  3. Will you be able to answer your question with this data, or do you need to gather more data (or adjust your question)?
    * Yes I will be able to answer this question with the data that I have. I may consider making the question more challenging as I dive into this work. Being completely new to the world of data science I am hesitant in my skills, but also feel that I have a learned a great deal in a short period of time. 
  4. What modeling approach are you using to answer your question?
     * For now I am going to start with the supervised learning model. As I learn more and determine if it is feasible I may dive into some unserpervised learning to make the question alittle mo0re difficult. 

# Project Update 
After a somewhat great deal of pain turmoil I have managed to format the data in such a way that I could use some of the modeling techniques we have learned in class. This data contained many object classifiers that needed to some manipulation. First I replaced all the null values with the term "missing". For this data this seemed like the best approach to maintain the accuracy of the data. I then used get_dummies to convert these columns into a numerical data set that could be manipulated. Unfortunatly this jumped the number of features I was working with from 79 to 261. 

After Fixing the categorical features I filled all integer based null values with the mean of their column. I then concatenated everything together into a new data frame. 

For my modeling I started with a relatively simple Decision Tree regressor model to determine the sale price. This gave me a baseline RMSE to work off of for future models. I then decided to build a Random Forest Regressor model for my final project. With this model I was able to lower the RMSE by about 40%.

After building and training the model I then predicted the sale price of a data set that did not provided everything but the sale price. I will submit the predictions that I made from this data to the Kaggle competition to see how I compared against others. 


  
