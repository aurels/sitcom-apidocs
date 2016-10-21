# Users

## Get all users

This endpoint retrieves all users.

### HTTP Request

`GET /api/users`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes

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

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
name      | String  | Yes
email     | String  | Yes
password  | String  | Yes

### HTTP Request

`POST /api/users`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
id        | Integer | Yes
name      | String  | Yes
email     | String  | Yes
password  | String  | Yes

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

## Delete a user

This endpoint deletes an existing user.

### HTTP Request

`DELETE /api/users/:id`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
id        | Integer | Yes
