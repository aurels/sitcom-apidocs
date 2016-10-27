# Users

## Get all users

```shell
curl -X GET https://example.com/api/users?api_key=XXXX"
```

```json
{
  "users": [
    {
      "id": 1,
      "name": "Aurélien Malisart",
      "email": "aurelien@phonoid.com",
      "admin": true,
      "labs": [
        {
          "id": 1,
          "name": "Smart Gastronomy Lab"
        },
        {
          "id": 2,
          "name": "e-Health"
        },
        {
          "id": 3,
          "name": "Fake"
        }
      ]
    },
    {
      "id": 4,
      "name": "Jules Verne",
      "email": "jules.verne@hotmail.com",
      "admin": false,
      "labs": [
        {
          "id": 1,
          "name": "Smart Gastronomy Lab"
        }
      ]
    },
    {
      "id": 2,
      "name": "Michaël Hoste",
      "email": "michael.hoste@gmail.com",
      "admin": false,
      "labs": [
        {
          "id": 1,
          "name": "Smart Gastronomy Lab"
        },
        {
          "id": 2,
          "name": "e-Health"
        },
        {
          "id": 3,
          "name": "Fake"
        },
        {
          "id": 4,
          "name": "fake2"
        }
      ]
    }
  ]
}
```

This endpoint retrieves all users.

### HTTP Request

`GET /api/users`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes

## Get one user

```shell
curl -X GET https://example.com/api/users/1?api_key=XXXX"
```

```json
{
  "user": {
    "id": 1,
    "name": "Aurélien Malisart",
    "email": "aurelien@phonoid.com",
    "admin": true,
    "labs": [
      {
        "id": 1,
        "name": "Smart Gastronomy Lab"
      },
      {
        "id": 2,
        "name": "e-Health"
      },
      {
        "id": 3,
        "name": "Fake"
      }
    ]
  }
}
```

This endpoint retrieves a specific user.

### HTTP Request

`GET /api/users/:id`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes

## Create a user

```shell
curl -X POST -H "Content-Type: multipart/form-data;" -F "user[name]=John Doe" -F "user[email]=john.doe@gmail.com" -F "user[password]=superpassword" "http://example.com/api/users?api_key=XXXX"
```

```json
{
  "user": {
    "id": 6,
    "name": "John Doe",
    "email": "john.doe@gmail.com",
    "admin": false,
    "labs": []
  }
}
```

This endpoint creates a new user.

### HTTP Request

`POST /api/users`

### Query Parameters

Parameter      | Type    | Required
---------      | ----    | --------
api_key        | String  | Yes
user[name]     | String  | Yes
user[email]    | String  | Yes
user[password] | String  | Yes

## Update a user

```shell
curl -X PUT -H "Content-Type: multipart/form-data;" -F "user[email]=john.doe.new@gmail.com" "http://example.com/api/users/6?api_key=XXXX"
```

```json
{
  "user": {
    "id": 6,
    "name": "John Doe",
    "email": "john.doe.new@gmail.com",
    "admin": false,
    "labs": []
  }
}
```

This endpoint updates an existing user.

### HTTP Request

`PUT /api/users/:id`

### Query Parameters

Parameter      | Type    | Required
---------      | ----    | --------
api_key        | String  | Yes
user[name]     | String  | No
user[email]    | String  | No
user[password] | String  | No

## Delete a user

```shell
curl -X DELETE -H "Content-Type: multipart/form-data;" "http://example.com/api/users/1?api_key=XXXX"
```

This endpoint deletes an existing user.

### HTTP Request

`DELETE /api/users/:id`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes

