# Contacts

## Get all contacts

This endpoint retrieves all contacts.

### HTTP Request

`GET /api/labs/:lab_id/contacts`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
lab_id    | Integer | Yes
page      | Integer | No

## Get a contact

This endpoint retrieves a specific contact.

### HTTP Request

`GET /api/labs/:lab_id/contacts/:id`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
lab_id    | Integer | Yes
id        | Integer | Yes

## Create a contact

This endpoint creates a new contact.

### HTTP Request

`POST /api/labs/:lab_id/contacts`

### Query Parameters

Parameter                   | Type      | Required
---------                   | ----      | --------
api_key                     | String    | Yes
lab_id                      | Integer   | Yes
contact[first_name]         | String    | Yes
contact[last_name]          | String    | Yes
contact[active]             | Boolean   | No
contact[email]              | String    | No
contact[phone]              | String    | No
contact[address_street]     | String    | No
contact[address_zip_code]   | String    | No
contact[address_city]       | String    | No
contact[address_country]    | String    | No
contact[twitter_url]        | String    | No
contact[linkedin_url]       | String    | No
contact[facebook_url]       | String    | No
contact[picture]            | File      | No
contact[organization_ids][] | Integer[] | No
contact[project_ids][]      | Integer[] | No
contact[event_ids][]        | Integer[] | No

## Update a contact

This endpoint updates an existing contact.

### HTTP Request

`PUT /api/labs/:lab_id/contacts/:id`

### Query Parameters

Parameter                   | Type      | Required
---------                   | ----      | --------
api_key                     | String    | Yes
lab_id                      | Integer   | Yes
contact[first_name]         | String    | Yes
contact[last_name]          | String    | Yes
contact[active]             | Boolean   | No
contact[email]              | String    | No
contact[phone]              | String    | No
contact[address_street]     | String    | No
contact[address_zip_code]   | String    | No
contact[address_city]       | String    | No
contact[address_country]    | String    | No
contact[twitter_url]        | String    | No
contact[linkedin_url]       | String    | No
contact[facebook_url]       | String    | No
contact[picture]            | File      | No
contact[organization_ids][] | Integer[] | No
contact[project_ids][]      | Integer[] | No
contact[event_ids][]        | Integer[] | No

## Delete a contact

This endpoint deletes an existing contact.

### HTTP Request

`DELETE /api/labs/:lab_id/contacts/:id`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
lab_id    | Integer | Yes
id        | Integer | Yes
