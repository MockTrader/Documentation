# Companies

## Available endpoints for this collection
- [`GET` /companies](#Get-companies) : Get all companies in LUSE catalog
- [`GET` /companies/:companyId](#Get-company-by-Id) : Get one company
- [`POST` /companies](#Add-company-to-catalog) : Add a new company to catalog by ticker aggregate (admin only)
- [`PATCH` /companies/:companyId](#Modify-company) : Modify info for an existing company in catalog (admin only)
- [`DELETE` /companies/:companyId](#Delete-company-from-catalog) : Remove a company from catalog (admin only)



## Get-companies 
[`GET` /companies](#Get-companies) : Get all companies in LUSE catalog

**Response** : 200 OK

**Response body** : 

```json
{
	"total": 65,
    "companies": [
        {
            "address": "Kings Place",
            "city": "London",
            "country": "United Kingdom",
            "id": "012caddb-0edf-4570-9315-f5dde389e819",
            "industry": "Aerospace & Defense",
            "logo_url": "https://logo.clearbit.com/rolls-royce.com",
            "long_name": "Rolls-Royce Holdings plc",
            "phone": 442072229020,
            "sector": "Industrials",
            "state": "null",
            "website": "http://www.rolls-royce.com"
        },
        
        ...
    ]
}
```



## Get-company-by-Id

[`GET` /companies/:companyId](#Get-company-by-Id) : Get one company

**Response** : 200 OK

**Response body** : 

```json
{
    "address": "Kings Place",
    "city": "London",
    "country": "United Kingdom",
    "id": "012caddb-0edf-4570-9315-f5dde389e819",
    "industry": "Aerospace & Defense",
    "logo_url": "https://logo.clearbit.com/rolls-royce.com",
    "long_business_summary": "Rolls-Royce Holdings plc operates as an [...]",
    "long_name": "Rolls-Royce Holdings plc",
    "phone": 442072229020,
    "sector": "Industrials",
    "state": "null",
    "website": "http://www.rolls-royce.com"
}
```



##  Add company to catalog

***Requires admin privileges***
***Requires authentication header***

[`POST` /companies](#Add-company-to-catalog) : Add a new company to catalog by ticker aggregate

**Request body** : 

```json
{
    "id": "SYF"
}
```

**Response** : 201 CREATED

**Response body** : 

```json
{
    "id": "81abf883-6d59-4bff-9cee-f61ae064695d"
}
```



## Modify company

***Requires admin privileges***
***Requires authentication header***

[`PATCH` /companies/:companyId](#Modify-company)  : Modify info for an existing company in catalog

**Request body** : 

```json
{
    "address": "420 Montgomery Street",
    "city": "Santa Monica",
    
    ...
}
```

**Response** : 204 NO CONTENT



## Delete company from catalog

***Requires admin privileges***
***Requires authentication header***

[`DELETE` /companies/:companyId](#Delete-company-from-catalog) : Remove a company from catalog

**Response** : 204 NO CONTENT

