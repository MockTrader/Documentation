# Orders

## Available endpoints for this collection
- [`GET` /users/:userId/orders](#Get-all-orders-for-user) : Get full order history for user
- [`GET` /users/:userId/portfolios/:portfolioId/orders](#Get-all-orders-for-portfolio) : Get all orders in a given portfolio for user
- [`POST` /users/:userId/portfolios/:portfolioId/orders](#Create-new-order) : Create new order for user
- [`POST` /users/:userId/orders/:orderId/cancel](#Cancel-order) : Cancel a pending order



## Get all orders for user
***Requires authentication header***
[`GET` /users/:userId/orders](#Get-all-orders-for-user) : Get full order history for user

**Response** : 200 OK

**Response body** : 

```json
{
    "orders": [
        {
            "buy": 1,
            "expiration_time": "2021-04-04 00:04:17",
            "filled_price": 9.01,
            "id": "591c252d-75da-4cf2-bbf3-1d3be973bdf3",
            "limit_price": 9.4605,
            "nb_shares": 3,
            "placed_time": "2021-04-03 00:04:17",
            "portfolio_id": "b453a274-bc01-4110-ae6a-8a39bb7fbdae",
            "status": "filled",
            "stock_suffix": "",
            "stock_ticker": "AMC",
            "type": "market"
        },
        
        ...
    ],
    "total": 20
}
```



## Get all orders for portfolio

***Requires authentication header***
[`GET` /users/:userId/portfolios/:portfolioId/orders](#Get-all-orders-for-portfolio) : Get all orders in a given portfolio for user

**Response** : 200 OK

**Response body** : 

```json
{
    "orders": [
        {
            "buy": 1,
            "expiration_time": "2021-04-04 00:04:17",
            "filled_price": 9.01,
            "id": "591c252d-75da-4cf2-bbf3-1d3be973bdf3",
            "limit_price": 9.4605,
            "nb_shares": 3,
            "placed_time": "2021-04-03 00:04:17",
            "portfolio_id": "b453a274-bc01-4110-ae6a-8a39bb7fbdae",
            "status": "filled",
            "stock_suffix": "",
            "stock_ticker": "AMC",
            "type": "market"
        },
        
        ...
    ],
    "total": 5
}
```



##  Create new order

***Requires authentication header***
[`POST` /users/:userId/portfolios/:portfolioId/orders](#Create-new-order) : Create new order for user

**Request body** : 

```json
{
    "expiration_time": "2021-04-06 00:12:32",
    "nb_shares": 1,
    "stock_suffix": "TO",
    "stock_ticker": "ADCO",
    "type": "market",
    "buy": 0
}
```

**Response** : 201 CREATED

**Response body** : 

```json
{
    "id": "b7513134-80f4-4945-957e-a10ee6a6e043"
}
```



## Cancel order

***Requires authentication header***
[`POST` /users/:userId/orders/:orderId/cancel](#Cancel-order) : Cancel a pending order

**Response** : 204 NO CONTENT