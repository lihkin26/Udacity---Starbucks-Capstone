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

## Code
Code is provided in 

## Further Improvements
Performance can be compared with supervised learning algorithms that will receive as input customer data and will predict whether consumer positively responds to an offer or not.
In the current model we are not able to predict best offers for a new user given there is no historic data for the ID. In such situations we are showing best offer strategies using the entire data.
Given the response from each of the different type of offers, we could create an offer level models and resume the responses and recommendation could be the one with most ROI.
Tune the parameters in a more efficient way rather than more of an hit and trial approach.

## Conclusion
In the EDA sections we saw that:
Older customers dominating the Starbucks market and income level below $80K have higher customer base
Most of the app users come from lower-middle class although Starbucks items are not cheap
Users who joined on earlier years might have discontinued their memberships, given that majority of the users have around 2 years of membership days
In the beginning we used mean squared error as an evaluation metrics and found that for FunkSVD has the best performance with 5 features.
We also did some exploratory analysis in the later sections of the blog, interesting things like Women respond better to BOGO offers and Man prefer to have offers that have accounting discounts in them.

## Blog post:
Here is the link to the blog post: https://medium.com/@lihkin26/recommending-customer-offers-for-starbucks-42d4980d0009?sk=1c0ebb1850823ff0f1fed178eb9c6fcc 
