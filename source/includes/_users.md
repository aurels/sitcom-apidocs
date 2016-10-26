# Users

## Get all users

This endpoint retrieves all users.

### HTTP Request

`GET /api/users`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes

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

## Get one user

This endpoint retrieves a specific user.

### HTTP Request

`GET /api/users/:id`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
id        | Integer | Yes

## Create a user

This endpoint creates a new user.

### HTTP Request

`POST /api/users`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
name      | String  | Yes
email     | String  | Yes
password  | String  | Yes

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

## Update a user

This endpoint updates an existing user.

### HTTP Request

`PUT /api/users/:id`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
id        | Integer | Yes
name      | String  | Yes
email     | String  | Yes
password  | String  | Yes

```shell

```

```json

```

## Delete a user

This endpoint deletes an existing user.

### HTTP Request

`DELETE /api/users/:id`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
id        | Integer | Yes

```shell

```

```json

```
