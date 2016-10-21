# Tags

## Get all tags of a lab

This endpoint retrieves all tags of a lab.

### HTTP Request

`GET /api/labs/:lab_id/tags`

### Query Parameters

Parameter  | Type    | Required
---------  | ----    | --------
api_key    | String  | Yes
lab_id     | Integer | Yes

## Get all tags of a contact

This endpoint retrieves all tags of a specific contact.

### HTTP Request

`GET /api/labs/:lab_id/contacts/:contact_id/tags`

### Query Parameters

Parameter  | Type    | Required
---------  | ----    | --------
api_key    | String  | Yes
lab_id     | Integer | Yes
contact_id | Integer | Yes

## Add some tags to a contact

This endpoint adds one or many tags to a contact.

### HTTP Request

`POST /api/labs/:lab_id/contacts/:contact_id/tags`

### Query Parameters

Parameter  | Type     | Required
---------  | ----     | --------
api_key    | String   | Yes
lab_id     | Integer  | Yes
contact_id | Integer  | Yes
names[]    | String[] | Yes

## Delete some tags from a contact

This endpoint deletes one or many tags from a contact.

### HTTP Request

`DELETE /api/labs/:lab_id/contacts/:contact_id/tags`

### Query Parameters

Parameter  | Type     | Required
---------  | ----     | --------
api_key    | String   | Yes
lab_id     | Integer  | Yes
contact_id | Integer  | Yes
names[]    | String[] | Yes
