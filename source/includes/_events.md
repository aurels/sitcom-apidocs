# Events

## Get all events

This endpoint retrieves all events.

### HTTP Request

`GET /api/labs/:lab_id/events`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
lab_id    | Integer | Yes
page      | Integer | No

## Get an event

This endpoint retrieves a specific event.

### HTTP Request

`GET /api/labs/:lab_id/events/:id`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
lab_id    | Integer | Yes
event_id  | Integer | Yes

## Get all events of a contact

This endpoint retrieves all events of a specific contact.

### HTTP Request

`GET /api/labs/:lab_id/contacts/:contact_id/events`

### Query Parameters

Parameter  | Type    | Required
---------  | ----    | --------
api_key    | String  | Yes
lab_id     | Integer | Yes
contact_id | Integer | Yes
page       | Integer | No

## Get an event of a contact

This endpoint retrieves a specific event of a specific contact.

### HTTP Request

`GET /api/labs/:lab_id/contacts/:contact_id/events/:id`

### Query Parameters

Parameter  | Type    | Required
---------  | ----    | --------
api_key    | String  | Yes
lab_id     | Integer | Yes
contact_id | Integer | Yes
event_id   | Integer | Yes
