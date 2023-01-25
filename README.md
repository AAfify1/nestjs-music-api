
## Description

The API was implemented using NestJS, and supported by a MongoDB hosted on Atlas.

> :warning: **I need to whitelist your IP to access the DB on atlas** Please email me your IP address on a.afify1995@gmail.com

Otherwise you can create and connect a local MongoDB instead.

All the required endpoints have been implemented and protected behind JWT authentication.


## Installation

```bash
$ yarn install
```

## Running the app

```bash
$ yarn run start
```
## Testing Steps

### 1- Create a user
POST `http://localhost:3000/auth/signup` with the body:

```JSON
{
    "username": "any-username",
    "password": "any-password"
}
```
### 2- Login
POST `http://localhost:3000/auth/login` with the same credentials used for sign up.

Response will look like this:
```json
{
    "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InRlc3QiLCJzdWIiOiI2M2QxMmY5NzJjNzc5YjdlZWM1NzdhNDMiLCJpYXQiOjE2NzQ2NjE0NzcsImV4cCI6MTY3NDY2NTA3N30.-lZEaz0Y1Q6KGBLs8X3_0n5-uCKdOLscCd73ADy4Atw"
}
```
### 3- All other endpoints
Use the token in the previous step in the postman `Authorization` tab and choose the type `Bearer Token`. You should now be authenticated and able to use any endpoint.

