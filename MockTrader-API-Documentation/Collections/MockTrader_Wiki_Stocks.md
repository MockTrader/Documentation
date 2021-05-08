# Stocks

## Available endpoints for this collection
- [`GET` /stocks](#Get-all-stocks) : Get all available stocks in LUSE catalog
- [`GET` /stocks/:tickerAggregate](#Get-stock-by-ticker-aggregate) : Refresh and get stock data with ticker aggregate 
- [`GET` /stocks/analytics/:tickerAggregate?period=period](#Get-stock-analytics) : Refresh and get stock analytics for ticker aggregate and given period
- [`POST` /stocks](#Add-new-stock-to-catalog) : Add new stock to catalog (admin only)
- [`DELETE` /stocks/:tickerAggregate](#Remove-stock-from-catalog) : Delete stock from catalog (admin only)



## Get all stocks
[`GET` /stocks](#Get-all-stocks) : Get all available stocks in LUSE catalog

**Response** : 200 OK

**Response body** : 

```json
{
    "total": 65,
    "stocks": [
        {
            "200_day_average": 15.75235,
            "52_week_high": 26.09,
            "52_week_low": 8.25,
            "ask": 21.98,
            "ask_size": 1800.0,
            "bid": 21.94,
            "bid_size": 1300.0,
            "company_id": "775c58de-e1d0-48f1-bf99-973e4b6ee0da",
            "currency": "USD",
            "day_change": -2.043107319,
            "dividend_yield": 0.0,
            "held_percent_insiders": 0.93,
            "held_percent_institutions": 45.42,
            "long_company_name": "American Airlines Group Inc.",
            "market_cap": 13951334400.0,
            "regular_market_day_high": 23.18,
            "regular_market_day_low": 21.76,
            "regular_market_open": 22.79,
            "regular_market_previous_close": 22.27,
            "regular_market_price": 21.815,
            "regular_market_volume": 44703867.0,
            "suffix": "",
            "ticker": "AAL"
        },
        
        ...
    ]
}
```



## Get stock by Id

[`GET` /stocks/:tickerAggregate](#Get-stock-by-ticker-aggregate) : Refresh and get stock data with ticker aggregate 

**Response** : 200 OK

**Response body** : 

```json
{
    "stock": {
        "200_day_average": 123.25287,
        "52_week_high": 145.09,
        "52_week_low": 62.345,
        "ask": 125.83,
        "ask_size": 1200.0,
        "bid": 125.82,
        "bid_size": 1200.0,
        "company_id": "70a04662-2501-440f-b4b6-5ab7af0df219",
        "currency": "USD",
        "day_change": 2.332845528,
        "dividend_yield": 0.67,
        "held_percent_insiders": 0.08,
        "held_percent_institutions": 59.77,
        "long_company_name": "Apple Inc.",
        "market_cap": 2113108049920.0,
        "regular_market_day_high": 125.96,
        "regular_market_day_low": 123.07,
        "regular_market_open": 123.87,
        "regular_market_previous_close": 123.0,
        "regular_market_price": 125.8694,
        "regular_market_volume": 49691231.0,
        "suffix": "",
        "ticker": "AAPL"
    },
    "series": [
        {
            "data": [
                {
                    "x": "Mon, 05 Apr 2021 09:30:00 GMT",
                    "y": [
                        123.5001,
                        124.5477,
                        123.07,
                        124.54
                    ]
                },
                
                ...
            ]
        }
    ]
}
```



## Get stock analytics

[`GET` /stocks/analytics/:tickerAggregate?period=period](#Get-stock-analytics) : Refresh and get stock analytics for ticker aggregate and given period

**Available periods** :

- **1d** : 1 day (15 minute intervals)
- **5d** : 5 days (1 hour intervals)
- **1mo** : 1 month (1 day intervals)
- **6mo **: 6 months (1 day intervals)
- **1y** : 1 year (1 day intervals)

**Response** : 200 OK

**Response body** : 

```json
{
    "series": {
        "data": [
            {
                "x": "Mon, 05 Apr 2021 09:30:00 GMT",
                "y": [ 705.13, 705.4, 695.925, 696.36 ]
            },
           
            ...
        ]
    }
}
```

The **data object** is a list of coordinates that can be fed into an [APEXCHARTS candlestick chart](https://apexcharts.com/docs/chart-types/candlestick/). 

- **x** : date and time for the entry
- **y** : [open, high, low, close]



##  Add new stock to catalog

***Requires admin privileges***

[`POST` /stocks](#Add-new-stock-to-catalog) : Add new stock to catalog

**Request body** : 

With compound ticker aggregate

```json
{
    "id": "AC.TO"
}
```

With simple ticker aggregate

```json
{
    "id": "SYF"
}
```

**Response** : 201 CREATED

**Response body** : 

```json
{
    "company_id": "81abf883-6d59-4bff-9cee-f61ae064695d",
    "id": "AC.TO"
}
```



## Remove stock from catalog

***Requires admin privileges***

[`DELETE` /stocks/:tickerAggregate](#Remove-stock-from-catalog) : Delete stock from catalog

**Response** : 204 NO CONTENT