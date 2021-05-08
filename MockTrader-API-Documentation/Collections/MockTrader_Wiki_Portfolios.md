# Portfolios

## Available endpoints for this collection
- [`GET` /users/:userId/portfolios](#Get-all-portfolios-for-user) : Get all portfolios for user
- [`GET` /users/:userId/portfolios/:portfolioId](#Get-portfolio-by-Id) : Get one portfolio
- [`POST` /users/:userId/portfolios](#Create-new-portfolio) : Create new portfolio
- [`PATCH` /users/:userId/portfolios/:portfolioId](#Modify-portfolio) : Modify existing portfolio
- [`DELETE` /users/:userId/portfolios/:portfolioId](#Delete-portfolio) : Delete existing portfolio



## Get all portfolios for user
[`GET` /users/:userId/portfolios](#Get-all-portfolios-for-user) : Get all portfolios for user

**Response** : 200 OK

**Response body** : 

```json
{
    "portfolios": [
        {
            "all_time_gains": 0.0,
            "cash_amount": 118.1819,
            "currency": "USD",
            "frozen_amount": 0.0,
            "id": "b453a274-bc01-4110-ae6a-8a39bb7fbdae",
            "invested_amount": 9435.5181,
            "market_value": 9495.6115,
            "name": "Social media",
            "type": "TFSA",
            "user_id": "e9950a8c-1267-44ae-b4c5-abbd5fc1f4d0"
        },
        
        ...
    ],
    "total": 2
}
```



## Get portfolio by Id

[`GET` /users/:userId/portfolios/:portfolioId](#Get-portfolio-by-Id) : Get one portfolio

**Response** : 200 OK

**Response body** : 

```json
{
    "all_time_gains": 0.0,
    "cash_amount": 118.1819,
    "currency": "USD",
    "frozen_amount": 0.0,
    "id": "b453a274-bc01-4110-ae6a-8a39bb7fbdae",
    "invested_amount": 9435.5181,
    "market_value": 9495.6115,
    "name": "Social media",
    "type": "TFSA",
    "user_id": "e9950a8c-1267-44ae-b4c5-abbd5fc1f4d0"
}
```



##  Create new portfolio

[`POST` /users/:userId/portfolios](#Create-new-portfolio) : Create new portfolio

**Request body** : 

```json
{
    "currency": "CAD",
    "name": "My new portfolio",
    "type": "TFSA"
}
```

**Response** : 201 CREATED

**Response body** : 

```json
{
    "id": "4875430b-9ccc-4552-a03d-41368e611728"
}
```



## Modify portfolio

[`PATCH` /users/:userId/portfolios/:portfolioId](#Modify-portfolio) : Modify existing portfolio

**Request body** : 

```json
{
    "currency": "EUR",
    
    ...
}
```

**Response** : 204 NO CONTENT



## Delete portfolio

[`DELETE` /users/:userId/portfolios/:portfolioId](#Delete-portfolio) : Delete existing portfolio

**Response** : 204 NO CONTENT