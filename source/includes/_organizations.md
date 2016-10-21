# Organizations

## Get all organizations

This endpoint retrieves all organizations.

### HTTP Request

`GET /api/labs/:lab_id/organizations`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
lab_id    | Integer | Yes
page      | Integer | No

## Get an organization

This endpoint retrieves a specific organization.

### HTTP Request

`GET /api/labs/:lab_id/organizations/:id`

### Query Parameters

Parameter        | Type    | Required
---------        | ----    | --------
api_key          | String  | Yes
lab_id           | Integer | Yes
organization_id  | Integer | Yes

## Get all organizations of a contact

This endpoint retrieves all organizations of a specific contact.

### HTTP Request

`GET /api/labs/:lab_id/contacts/:contact_id/organizations`

### Query Parameters

Parameter  | Type    | Required
---------  | ----    | --------
api_key    | String  | Yes
lab_id     | Integer | Yes
contact_id | Integer | Yes
page       | Integer | No

## Get an organization of a contact

This endpoint retrieves a specific organization of a specific contact.

### HTTP Request

`GET /api/labs/:lab_id/contacts/:contact_id/organizations/:id`

### Query Parameters

Parameter       | Type    | Required
---------       | ----    | --------
api_key         | String  | Yes
lab_id          | Integer | Yes
contact_id      | Integer | Yes
organization_id | Integer | Yes
