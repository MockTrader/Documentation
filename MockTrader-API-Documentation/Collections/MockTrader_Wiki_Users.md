# Users

## Available endpoints for this collection
- [`GET` /users](#Get-all-users) : Get basic info for all users (admin only)
- [`GET` /users/:userId](#Get-user-by-Id) : Get info for user
- [`POST` /users](#Create-use) : Create new user
- [`PATCH` /users/:userId](#Modify-user) : Modify existing user
- [`DELETE` /users/:userId](#Delete-user) : Delete existing user



## Get all users
***Requires admin privileges***

[`GET` /users](#Get-all-users) : Get basic info for all users (admin only)

**Response** : 200 OK

**Response body** : 

```json
{
    "total": 500,
    "users": [
        {
            "email": "montana.douglas@gmail.com",
            "first_name": "Montana",
            "id": "0037ce74-ef4c-24e3-b0d1-c1c7c069a859",
            "last_name": "Douglas"
        },
        
        ...
    ]
}  
```



## Get user by Id
[`GET` /users/:userId](#Get-user-by-Id) : Get info for user

**Response** : 200 OK

**Response body** : 

```json
{
    "address": "161-7079 Ac St.",
    "birth_date": "1989-02-22",
    "city": "Calmar",
    "country": "Canada",
    "email": "jesse.smith@gmail.com",
    "first_name": "Jesse",
    "id": "e9950a8c-1267-44ae-b4c5-abbd5fc1f4d0",
    "last_name": "Smith",
    "phone": "3011841732",
    "signup_date": "2020-10-15",
    "state": "Alberta",
    "zip": "T5G 5K2"
}
```



## Create user

[`POST` /users](#Create-use) : Create new user

**Request body** : 

```json
{
    "address": "349 Imperdiet St.",
    "birth_date": "1992-09-24",
    "city": "Ottawa",
    "country": "Canada",
    "email": "justine.martel@gmail.com",
    "first_name": "Justine",
    "last_name": "Martel",
    "phone": "3519201043",
    "signup_date": "2020-12-30",
    "state": "ON",
    "zip": "35023",
    "password": HASHED_PASSWORD
}
```

**Response** : 201 CREATED

**Response body** : 

```json
{
    "id": "bf9eb43c-ea4a-486a-9743-d5cfdaa65112"
}
```



## Modify user

[`PATCH` /users/:userId](#Modify-user) : Modify existing user

**Request body** : 

```json
{
    "address": "123 new street name",
    ...
}
```

**Response** : 204 NO CONTENT



### Delete user

[`DELETE` /users/:userId](#Delete-user) : Delete existing user

**Response** : 204 NO CONTENT