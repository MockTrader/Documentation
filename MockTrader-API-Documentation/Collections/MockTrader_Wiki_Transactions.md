# Transactions

## Available endpoints for this collection
- [`GET` /users/:userId/transactions](#Get-all-transactions-for-user) : Get full transaction history for user
- [`GET` /users/:userId/portfolios/:portfolioId/transactions](#Get-transactions-in-portfolio) : Get transaction history for portfolio
- [`POST` /users/:userId/portfolios/:portfolioId/transactions](#Create-new-transaction) : Create new transaction in portfolio



## Get all transactions for user
[`GET` /users/:userId/transactions](#Get-all-transactions-for-user) : Get full transaction history for user

**Response** : 200 OK

**Response body** : 

```json
{
    "total": 6,
    "transactions": [
        {
            "bank_account": 640011867593573,
            "creation_time": "Tue, 09 Feb 2021 22:18:18 GMT",
            "description": "Funds transferred into Social media (TFSA)",
            "id": 2,
            "portfolio_uuid": "b453a274-bc01-4110-ae6a-8a39bb7fbdae",
            "type": "deposit",
            "value": 5000.0
        },
        
        ...
    ]
}
```



## Get transactions in portfolio

[`GET` /users/:userId/portfolios/:portfolioId/transactions](#Get-transactions-in-portfolio) : Get transaction history for portfolio

**Response** : 200 OK

**Response body** : 

```json
{
    "total": 2,
    "transactions": [
        {
            "bank_account": 640011867593573,
            "creation_time": "Tue, 09 Feb 2021 22:18:18 GMT",
            "description": "Funds transferred into Social media (TFSA)",
            "id": 2,
            "portfolio_uuid": "b453a274-bc01-4110-ae6a-8a39bb7fbdae",
            "type": "deposit",
            "value": 5000.0
        },
        
        ...
    ]
}
```



##  Create new transaction

[`POST` /users/:userId/portfolios/:portfolioId/transactions](#Create-new-transaction) : Create new transaction in portfolio

**Request body** : 

```json
{
    "bank_account": "1105374",
    "description": "Funds sent to savings portfolio",
    "value": 2500,
    "type": "deposit"
}
```

**Response** : 201 CREATED