# Projects

## Get all projects

This endpoint retrieves all projects.

### HTTP Request

`GET /api/labs/:lab_id/projects`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
lab_id    | Integer | Yes
page      | Integer | No

## Get a project

This endpoint retrieves a specific project.

### HTTP Request

`GET /api/labs/:lab_id/projects/:id`

### Query Parameters

Parameter   | Type    | Required
---------   | ----    | --------
api_key     | String  | Yes
lab_id      | Integer | Yes
project_id  | Integer | Yes

## Get all projects of a contact

This endpoint retrieves all projects of a specific contact.

### HTTP Request

`GET /api/labs/:lab_id/contacts/:contact_id/projects`

### Query Parameters

Parameter  | Type    | Required
---------  | ----    | --------
api_key    | String  | Yes
lab_id     | Integer | Yes
contact_id | Integer | Yes
page       | Integer | No

## Get a project of a contact

This endpoint retrieves a specific project of a specific contact.

### HTTP Request

`GET /api/labs/:lab_id/contacts/:contact_id/projects/:id`

### Query Parameters

Parameter  | Type    | Required
---------  | ----    | --------
api_key    | String  | Yes
lab_id     | Integer | Yes
contact_id | Integer | Yes
project_id | Integer | Yes
