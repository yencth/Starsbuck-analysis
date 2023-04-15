# Starsbuck capstrone project in Udacity

### Introduction
This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks.

Not all users receive the same offer, and that is the challenge to solve with this data set.

In this project, I will build a model that predicts whether or not someone will respond to an offer. 

### Datasets
The data is contained in three files:


Here is the schema and explanation of each variable in the files:

* portfolio.json

id (string) - offer id
offer_type (string) - type of offer ie BOGO, discount, informational
difficulty (int) - minimum required spend to complete an offer
reward (int) - reward given for completing an offer
duration (int) - time for offer to be open, in days
channels (list of strings)

* profile.json

age (int) - age of the customer
became_member_on (int) - date when customer created an app account
gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
id (str) - customer id
income (float) - customer's income

* transcript.json

event (str) - record description (ie transaction, offer received, offer viewed, etc.)
person (str) - customer id
time (int) - time in hours since start of test. The data begins at time t=0
value - (dict of strings) - either an offer id or transaction amount depending on the record

### Files description
#### data: folder contain input data:
* portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
* profile.json - demographic data for each customer
* transcript.json - records for transactions, offers received, offers viewed, and offers completed
#### Starbucks_Capstone_notebook.ipynb: 
note book of data analysis, data processing and modeling
#### requirements.txt: 
The libraries need to be installed

## Summary the results
We analysis the data and find the answer for question:  whether or not someone will respond to an offer?
The best model is XGboost, which return accuracy is 74% use demographics data.
This is not high accuracy. We could improve the performance by tunning model or get more features (in transcript data).

This is link of medium: