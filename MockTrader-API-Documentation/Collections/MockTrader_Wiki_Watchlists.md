# Watchlists

## Available endpoints for this collection
- [`GET` /users/:userId/watchlist](#Get-user-watchlist) : Get all stocks in user watchlist
- [`POST` /users/:userId/watchlist](#Create-new-transaction) : Add stock to user watchlist
- [`DELETE` /users/:userId/watchlist/:stockTickerAggregate](#Remove-stock-from-watchlist) : Remove stock from user watchlist



## Get user watchlist
[`GET` /users/:userId/watchlist](#Get-user-watchlist) : Get all stocks in user watchlist

**Response** : 200 OK

**Response body** : 

```json
{
    "total": 3,
    "watchlist": [
        {
            "long_name": "Activision Blizzard, Inc.",
            "regular_market_price": 90.53,
            "ticker": "ATVI",
            "watch_price": 90.53
        },
        
        ...
    ]
}
```



## Add stock to watchlist

[`POST` /users/:userId/watchlist](#Create-new-transaction) : Add stock to user watchlist

**Request body** : 

```json
{
    "ticker": "AAPL",
    "watch_price": 100
}
```

**Response** : 201 CREATED



###  Remove stock from watchlist

[`DELETE` /users/:userId/watchlist/:stockTickerAggregate](#Remove-stock-from-watchlist) : Remove stock from user watchlist

**Response** : 204 NO CONTENT