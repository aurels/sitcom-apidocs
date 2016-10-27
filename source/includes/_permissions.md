# Permissions

## Get all permissions of a user

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

This endpoint retrieves all permissions of a user (for all his accessible labs).

### HTTP Request

`GET /api/users/:user_id/permissions`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes

## Get permissions of a user on a lab

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

This endpoint retrieves the permissions of a user on a lab.

### HTTP Request

`GET /api/users/:user_id/permissions/:lab_id`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes

## Grant a user access to a lab

```shell
curl -X POST -H "Content-Type: multipart/form-data;" -F "permission[can_read_contacts]=true" -F "permission[can_write_contacts]=false" -F "permission[can_read_organizations ]=true" -F "permission[can_write_organizations]=false" -F "permission[can_read_projects]=true" -F "permission[can_write_projects]=false" -F "permission[can_read_events]=false" -F "permission[can_write_events]=false" "http://example.com/api/users/2/permissions/2?api_key=XXXX"
```

```json
{
  "permission": {
    "lab_id": 2,
    "lab_name": "e-Health",
    "can_read_contacts": true,
    "can_write_contacts": false,
    "can_read_organizations": true,
    "can_write_organizations": false,
    "can_read_projects": true,
    "can_write_projects": false,
    "can_read_events": false,
    "can_write_events": false
  }
}
```

This endpoint grants a user access to a lab.

### HTTP Request

`POST /api/users/:user_id/permissions/:lab_id`

### Query Parameters

Parameter                           | Type    | Required
---------                           | ----    | --------
api_key                             | String  | Yes
permission[can_read_contacts]       | Boolean | No
permission[can_write_contacts]      | Boolean | No
permission[can_read_organizations ] | Boolean | No
permission[can_write_organizations] | Boolean | No
permission[can_read_projects]       | Boolean | No
permission[can_write_projects]      | Boolean | No
permission[can_read_events]         | Boolean | No
permission[can_write_events]        | Boolean | No

## Update permissions of a user on a lab

```shell
curl -X PUT -H "Content-Type: multipart/form-data;" -F "permission[can_read_contacts]=false" -F "permission[can_read_organizations ]=false" -F "permission[can_read_projects]=false" "http://example.com/api/users/2/permissions/2?api_key=XXXX"
```

```json
{
  "permission": {
    "lab_id": 2,
    "lab_name": "e-Health",
    "can_read_contacts": false,
    "can_write_contacts": false,
    "can_read_organizations": false,
    "can_write_organizations": false,
    "can_read_projects": false,
    "can_write_projects": false,
    "can_read_events": false,
    "can_write_events": false
  }
}
```

This endpoint updates a user's permissions to a lab.

### HTTP Request

`PUT /api/users/:user_id/permissions/:lab_id`

### Query Parameters

Parameter                           | Type    | Required
---------                           | ----    | --------
api_key                             | String  | Yes
permission[can_read_contacts]       | Boolean | No
permission[can_write_contacts]      | Boolean | No
permission[can_read_organizations ] | Boolean | No
permission[can_write_organizations] | Boolean | No
permission[can_read_projects]       | Boolean | No
permission[can_write_projects]      | Boolean | No
permission[can_read_events]         | Boolean | No
permission[can_write_events]        | Boolean | No

## Revoke access of a user to a lab

```shell
curl -X DELETE -H "Content-Type: multipart/form-data;" "http://example.com/api/users/1/permissions/1?api_key=XXXX"
```

This endpoint revokes a user's access to a lab.

### HTTP Request

`DELETE /api/users/:user_id/permissions/:lab_id`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
