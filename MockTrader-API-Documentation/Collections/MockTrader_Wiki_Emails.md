# Emails

## Available endpoints for this collection
- [`GET` /accounts/confirm/:userId](#Confirm-account) : Confirm user email
- [`POST` /accounts/reset/:userEmail](#Request-password-reset-email) : Request password reset email
- [`GET` /accounts/reset/:userEmail/:resetId](#Reset-password) : Access password reset resource



## Confirm account 
[`GET` /accounts/confirm/:userId](#Confirm-account) : Confirm user email

**Response** : 200 OK



## Request password reset email

[`POST` /accounts/reset/:userEmail](#Request-password-reset-email) : Request password reset email

**Response** : 201 CREATED



##  Reset password

[`GET` /accounts/reset/:userEmail/:resetId](#Reset-password) : Access password reset resource

**Response** : 302 FOUND