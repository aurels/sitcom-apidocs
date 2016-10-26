# Permissions

## Get all permissions of a user

This endpoint retrieves all permissions of a user (for all his accessible labs).

### HTTP Request

`GET /api/users/:user_id/permissions`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
user_id   | Integer | Yes

```shell
curl -X GET https://example.com/api/users/1/permissions?api_key=XXXX"
```

```json
{
  "permissions": [
    {
      "lab_id": 1,
      "lab_name": "Smart Gastronomy Lab",
      "can_read_contacts": true,
      "can_write_contacts": true,
      "can_read_organizations": true,
      "can_write_organizations": true,
      "can_read_projects": true,
      "can_write_projects": true,
      "can_read_events": true,
      "can_write_events": true
    },
    {
      "lab_id": 2,
      "lab_name": "e-Health",
      "can_read_contacts": true,
      "can_write_contacts": true,
      "can_read_organizations": true,
      "can_write_organizations": true,
      "can_read_projects": true,
      "can_write_projects": true,
      "can_read_events": true,
      "can_write_events": true
    },
    {
      "lab_id": 3,
      "lab_name": "Fake",
      "can_read_contacts": true,
      "can_write_contacts": true,
      "can_read_organizations": true,
      "can_write_organizations": true,
      "can_read_projects": true,
      "can_write_projects": true,
      "can_read_events": true,
      "can_write_events": true
    }
  ]
}
```

## Get permissions of a user on a lab

This endpoint retrieves the permissions of a user on a lab.

### HTTP Request

`GET /api/users/:user_id/permissions/:lab_id`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
user_id   | Integer | Yes
lab_id    | Integer | Yes

```shell
curl -X GET https://example.com/api/users/1/permissions/1?api_key=XXXX"
```

```json
{
  "permission": {
    "lab_id": 1,
    "lab_name": "Smart Gastronomy Lab",
    "can_read_contacts": true,
    "can_write_contacts": true,
    "can_read_organizations": true,
    "can_write_organizations": true,
    "can_read_projects": true,
    "can_write_projects": true,
    "can_read_events": true,
    "can_write_events": true
  }
}
```

## Grant a user access to a lab

This endpoint grants a user access to a lab.

### HTTP Request

`POST /api/users/:user_id/permissions/:lab_id`

### Query Parameters

Parameter                           | Type    | Required
---------                           | ----    | --------
api_key                             | String  | Yes
user_id                             | Integer | Yes
lab_id                              | Integer | Yes
permission[can_read_contacts]       | Boolean | No
permission[can_write_contacts]      | Boolean | No
permission[can_read_organizations ] | Boolean | No
permission[can_write_organizations] | Boolean | No
permission[can_read_projects]       | Boolean | No
permission[can_write_projects]      | Boolean | No
permission[can_read_events]         | Boolean | No
permission[can_write_events]        | Boolean | No

```shell

```

```json

```

## Update permissions of a user on a lab

This endpoint updates a user's permissions to a lab.

### HTTP Request

`PUT /api/users/:user_id/permissions/:lab_id`

### Query Parameters

Parameter                           | Type    | Required
---------                           | ----    | --------
api_key                             | String  | Yes
user_id                             | Integer | Yes
lab_id                              | Integer | Yes
permission[can_read_contacts]       | Boolean | No
permission[can_write_contacts]      | Boolean | No
permission[can_read_organizations ] | Boolean | No
permission[can_write_organizations] | Boolean | No
permission[can_read_projects]       | Boolean | No
permission[can_write_projects]      | Boolean | No
permission[can_read_events]         | Boolean | No
permission[can_write_events]        | Boolean | No

```shell

```

```json

```

## Revoke access of a user to a lab

This endpoint revokes a user's access to a lab.

### HTTP Request

`DELETE /api/users/:user_id/permissions/:lab_id`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
user_id   | Integer | Yes
lab_id    | Integer | Yes

```shell

```

```json

```
