<img alt="Data4Deals logo" src="dark.svg" width="250" align="right" />

# Data4Deals Coding challenge

## Intro

If you’ve seen our website or had an intro interview, you see that transactional data sits on the center of your core system, and that marketing campaigns are what drive our product. 

For this challenge, we want you to focus on the merchants/campaigns side, and build a web server that consumes a database where merchants and campagins are configured.

For this full-stack/backend development position, we want you to build a webserver, that reads the data from the database.

For sake of simplicity, assume that there's a portal (like a Google Ad manager or Facebook equivalent), in which they are configured - this is out of the scope of this project.

If you feel like there are improvements that you can do but had no time, just create some TODO comments that we will use to discuss with you later. 

## Programming requirements

In this case, we want you to use Java 8.
Regarding the database, we would recommend MongoDB, but feel free to use other if you're more used to. 

#### Bonus points
If you are familiar with Sprint Data, consider using it.


## Problem statement: 

## PART 1: Create a dummy DB

Create a DB with a collection for merchants and another for campaigns.
A merchant can have 0, 1 or more campaigns.

Assume the following minimum document fields:
* A Merchant has a name a url.
* A Campaign refers to a certain merchant, and has initial budget (e.g., 1000€), a cashback percentage (e.g. 10% cashback) and can have a purchase amount threshold (e.g., cashback only valid on purchases above 30€).

You can populate the database in any way you like it.

Present us with the database schema and the decisions you took.


## PART 2: REST API

Create an api with the following routes:

* GET getMerchants() : returns a list with all merchants.
* GET getMerchant(int id) : returns the specified merchant.


- GET getCampaigns() : returns a list with all campaigns, that still have budget.
- GET getCampaigns(int limit) : returns a list with all campaigns, that still have budget, up to a maximum of _limit_ campaigns.
- GET getCampaigns(int limit, int offset) : returns a list with all campaigns, that still have budget, up to a maximum of _limit_ campaigns, and starting at _offset_ -> useful for creating infinite scroll feature in a frontend display.
- GET getCampaign(int id) : returns the specified campaign.


* POST consumeBudget(int id, double amount) : it subtracts _amount_ to the remaining budget of the campaign in the database. Assume this route will be called when cashbacks are issued.



## Key Points:
- Code structure
- Graceful error handling
- Good composition
- Separation of concepts
- Design patterns
- Language efficacy

## Bonus points
- Tests

## PART 3: README

Please provide us with any information you find relevant and instructions (for dummies) on how to build the environment and run your code. 