# Positions

## Available endpoints for this collection
- [`GET` /users/:userId/positions](#Get-all-positions-for-user) : Get all positions for user
- [`GET` /users/:userId/positions/:portfolioId](#Get-positions-in-portfolio) : Get all positions in given portfolio



## Get all positions for user
[`GET` /users/:userId/positions](#Get-all-positions-for-user) : Get all positions for user

**Response** : 200 OK

**Response body** : 

```json
{
    "total": 15,
    "positions": [
        {
            "avg_price": 120.07,
            "nb_shares": 11,
            "portfolio_id": "b453a274-bc01-4110-ae6a-8a39bb7fbdae",
            "portfolio_name": "Social media",
            "suffix": "",
            "ticker": "AAPL",
            "unrealized_gain": 5.7994
        },
        
        ...
    ]
}
```



## Get positions in portfolio

[`GET` /users/:userId/positions/:portfolioId](#Get-positions-in-portfolio) : Get all positions in given portfolio

**Response** : 200 OK

**Response body** : 

```json
{
    "total": 8,
    "positions": [
        {
            "avg_price": 120.07,
            "nb_shares": 11,
            "portfolio_id": "b453a274-bc01-4110-ae6a-8a39bb7fbdae",
            "portfolio_name": "Social media",
            "suffix": "",
            "ticker": "AAPL",
            "unrealized_gain": 5.7994
        },
        
        ...
    ]
}
```