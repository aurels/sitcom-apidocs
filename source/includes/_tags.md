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

```shell
curl -X GET https://example.com/api/labs/1/tags?api_key=XXXX"
```

```json
{
  "tags": [
    {
      "name": "groupe 1",
      "color": "#e59599"
    },
    {
      "name": "groupe 3",
      "color": "#95b0e5"
    },
    {
      "name": "groupe 5",
      "color": "#c8e595"
    },
    {
      "name": "groupe 2",
      "color": "#e595df"
    },
    {
      "name": "groupe 4",
      "color": "#95e5d4"
    },
    {
      "name": "XXXXXX",
      "color": "#a695e5"
    }
  ]
}
```

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

```shell
curl -X GET https://example.com/api/labs/1/contacts/1/tags?api_key=XXXX"
```

```json
{
  "tags": [
    {
      "name": "groupe 2",
      "color": "#e595df"
    }
  ]
}
```

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

```shell

```

```json

```

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

```shell

```

```json

```
