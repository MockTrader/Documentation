# Authentication

## Available endpoints for this collection

- [`POST` /auth/login](#Login) : Get temporary Auth Token for user credentials
- [`DELETE` /auth/logout](#Logout) : Invalidate Auth Token



## Login
[`POST` /auth/login](#Login) : Get temporary Auth Token for user credentials

**Request body** : 

```json
{
    "email": "jesse.smith@gmail.com",
    "hashed_password": "4f22050b8122vad262c276921714f3f4dea31849b6383bab80603405e74aa04f"
}
```

**Response** : 201 CREATED

**Response body** : 

```json
{
    "id": "e9950a8c-1267-44ae-b4c5-abbd5fc1f4d0",
    "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE2MTc2NjAxODgsImlhdCI6MTYxNzY1NjU4OCwidXNlcklkIjoiZTk5NTBhOGMtMTI2Ny00NGFlLWI0YzUtYWJiZDVmYzFmNGQwIn0.njI2QJQwri9_diZAdNl9m18TGMDZukpPBhHbv4_clN8"
}
```



## Logout

***Requires authentication header***

Header : "AuthToken" = your_auth_token_here

[`DELETE` /auth/logout](#Logout) : Invalidate Auth Token

**Response** : 204 NO CONTENT

