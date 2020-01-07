# Starbucks Capstone Project

## Motivation
The purpose of the project is to analyze Starbucks data that contains simulated data that mimics customer behavior on the Starbucks rewards mobile app and to address the following:
  1) Which offer has the highest gain? Which offer can be recommended in general?
  2) Which offer is more relevant for a particular customer thus encouraging him to buy more?Are there particular demographic groups that respond best to a particular offer type?

## Installations

1) NumPy
2) Pandas
3) Matplotlib
4) Json
5) Plotly
6) Math
7) Tqdm
8) Seaborn

This project requires Python 3.x and the above Python libraries installed. You will also need to have software installed to run and execute an iPython Notebook

## Dataset

The data is contained in three files:

portfolio.json
id (string) - offer id offer_type (string) - the type of offer ie BOGO, discount, informational difficulty (int) - the minimum required to spend to complete an offer reward (int) - the reward is given for completing an offer duration (int) - time for the offer to be open, in days channels (list of strings)

profile.json
age (int) - age of the customer became_member_on (int) - the date when customer created an app account gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F) id (str) - customer id income (float) - customer's income

transcript.json
event (str) - record description (ie transaction, offer received, offer viewed, etc.) person (str) - customer id time (int) - time in hours since the start of the test. The data begins at time t=0 value - (dict of strings) - either an offer id or transaction amount depending on the record

Approach: 

A four step approach was followed for the analysis:
  1) Data Cleaning & Processing: This step helps treat any missing values or outliers present in the data set. Also, processing will help us transform the data in such a way that can help understand the data better
  2) Data Understanding & Exploration- Understanding the distribution in the data and identify any biases. This would help develop hypothesis & deeper understanding of the data
  3) Modelling & Evaluation: For this analysis, I have used Funk SVD algorithm as it works well with Sparse matrices. Appropriate evaluation measures will be used to identify best set of latent variables. MSE is the metric of evaluation. Best parameters based on the train and test MSE will be selected for the analysis
  4) Insights and Recommendations: Identify any interesting trends or patterns from the analysis and give final recommendations

## Code
Code is provided in Starbucks_Capstone_notebook.ipynb notebook

## Insights / Conclusion
In the EDA sections we saw that:
  1) Older customers dominating the Starbucks market and income level below $80K have higher customer base
  2) Most of the app users come from lower-middle class although Starbucks items are not cheap
  3) Users who joined on earlier years might have discontinued their memberships, given that majority of the users have around 2 years of membership days
  4) In the beginning we used mean squared error as an evaluation metrics and found that for FunkSVD has the best performance with 5 features.
  4) We also did some exploratory analysis in the later sections of the blog, interesting things like Women respond better to BOGO offers and Men prefer to have offers that have accounting discounts in them.

## Enhancements
  1) Tune the parameters in a more efficient way rather than more of an hit and trial approach. GridSerachCV or RandomizedSearchCV can be used to get the optimum number of latest variables
  2) Performance can be compared with supervised learning algorithms that will receive as input customer data and will predict whether consumer positively responds to an offer or not.
  3) In the current model we are not able to predict best offers for a new user given there is no historic data for the ID. In such situations we are showing best offer strategies using the entire data.
  4) Given the response from each of the different type of offers, we could create an offer level models and resume the responses and recommendation could be the one with most ROI.



## Blog post:
Here is the link to the blog post: https://medium.com/@lihkin26/recommending-customer-offers-for-starbucks-42d4980d0009?sk=1c0ebb1850823ff0f1fed178eb9c6fcc 
