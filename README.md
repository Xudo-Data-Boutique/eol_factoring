# Use MS Azure Data Factory to speed up your cash conversion cycle

Cashflow can be a challenge. You have to pay your suppliers in 30 days, but your clients only pay in 60 to 90 days. You can use factoring to bridge this divide. Talk to your bank to see if your business is eligible for this kind of pre-financing.

# Factoring
Factoring is an option a CFO has to get cash from the bank as soon as a sales invoice is booked, long before the clients pay their invoices. This lowers the liquidity measure Days Sales Outstanding (DSO) and speeds up the cash conversion cycle (CCC) to avoid cashflow problems in businesses with longer payment terms, or with clients that tend to pay their invoices too late. The bank provides the cash, and in return takes a commission on the factored amounts.

# Data pipelines
In this series of blogposts I will describe how to use Postman, Azure Data Factory, Azure SQL Database and Azure Blob Storage to connect to the Exact Online API to collect outstanding sales invoices and debtors to send to the bank for factoring.

1. Using Postman to connect to an API that has OAuth2 authorization 
  - https://medium.com/plumbersofdatascience/connect-to-the-exact-online-api-with-postman-3eb63959f63e
  - Find the Postman collection in the repository
  
How to do OAUTH2 authentication and authorization for the Exact Online Cloud Accounting API using Postman? We need this step to get our first Access and Refresh tokens to get the process in Azure Data Factory running.

2. Setting up Oauth2 for EOL in Azure Data Factory
  - https://medium.com/@xudo_data_boutique/setting-up-oauth2-for-eol-in-azure-data-factory-c01198b0bfb6
  - Find the T-SQL to set up the database in the repository

As soon as we have retrieved our first Access and Refresh token from the API using Postman, we can set up an automated process to make sure we have access to the data at the time we need it.

3. 

Once we have the authorization in place and have access to the data, we will use Azure Data Factory Pipelines, an Azure SQL Database and Azure Blog Storage to get, process and store the data to send to the bank for factoring.
