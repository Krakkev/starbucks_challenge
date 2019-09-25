# Starbucks Capstone Challenge

### Introduction

This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks. 

Not all users receive the same offer, and that is the challenge to solve with this data set.

Your task is to combine transaction, demographic and offer data to determine which demographic groups respond best to which offer type. This data set is a simplified version of the real Starbucks app because the underlying simulator only has one product whereas Starbucks actually sells dozens of products.

Every offer has a validity period before the offer expires. As an example, a BOGO offer might be valid for only 5 days. You'll see in the data set that informational offers have a validity period even though these ads are merely providing information about a product; for example, if an informational offer has 7 days of validity, you can assume the customer is feeling the influence of the offer for 7 days after receiving the advertisement.

You'll be given transactional data showing user purchases made on the app including the timestamp of purchase and the amount of money spent on a purchase. This transactional data also has a record for each offer that a user receives as well as a record for when a user actually views the offer. There are also records for when a user completes an offer. 

Keep in mind as well that someone using the app might make a purchase through the app without having received an offer or seen an offer.

### How should I run this project?

First of all you need to install a virtual environment, activate it and then install the requirements.txt file 
``` 
virtualenv env -p python3
source env/bin/activate
pip install -r requirements.txt
```

Once that you have installed the whole dependences you can just run jupyter notebook
``` 
jupyter notebook
```
and you are going to find 3 different notebooks:
    
     1. understanding_and_cleaning_data.ipynb
     2. merging_data.ipynb
     3. Analysis.ipynb
     
 
*understanding_and_cleaning_data.ipynb*

Here you will find the process to clean the datasets and the creation of features that were needed in the next notebooks.

*merging_data.ipynb* 
In this file the data obtained before and the events of the offers and transactions are mixed up to make possible the analysis.

*Analysis.ipynb* 
In this notebook you will some different clusters made using K-means to know the clients and their relation with the use of the offers.

    
## CONCLUSIONS (Also located in Analysis.ipynb file)

Less than 10% of the clients spent more than 200 dollars without the motivation of offers. Those probably don't need offers to keep buying. But the rest of the clients could need a little push.

That is the reason why this analysis is so important. Just to give you an idea, more than 30% of the total transactions are influenced by offers!

There are 3 types of offers:
- Informational
- Discount
- BOGO (Buy One Get One)
Informational
The informational offer is the one with less impact in the users. Sadly, 89% of the users offered with this didn't buy anything.

BOGO
The BOGO offer has much more impact than Informational, more than 50% of the offers are completed.But seems to be prefered by women rather than men.

Discount
The Discount offers are the ones that has more impact! 70% of the offers seen were completed. This is a pretty good number, and seems to be accepted by almost for any type of user. (Also this offer has a better acceptance by women)

If the objective of the offers is to increase the increase the transactions made by the users Discount is the one to go with, followed by BOGO. Obviously the informational ones did not represents any money for the company, but also the impact is very very low. Probably another good think to analyze in the future could be which is the best way to comunicate the offers. Because this step is the reason for many incompleted offers.