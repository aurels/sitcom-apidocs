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

```shell
curl -X GET https://example.com/api/labs/1/organizations?api_key=XXXX"
```

```json
{
  "organizations": [
    {
      "id": 1,
      "name": "CETIC",
      "status": "",
      "description": null,
      "website_url": "",
      "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=C&w=200&h=200",
      "contacts": []
    },
    {
      "id": 3,
      "name": "80LIMIT",
      "status": "",
      "description": null,
      "website_url": "",
      "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=8&w=200&h=200",
      "contacts": [
        {
          "id": 95,
          "name": "Manon Roux"
        },
        {
          "id": 41,
          "name": "Mattéo Dupuy"
        },
        {
          "id": 70,
          "name": "Alice Faure"
        }
      ]
    },
    {
      "id": 4,
      "name": "Phonoid",
      "status": "",
      "description": null,
      "website_url": "",
      "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=P&w=200&h=200",
      "contacts": [
        {
          "id": 48,
          "name": "Alexandre Schneider"
        },
        {
          "id": 35,
          "name": "Serge Pampfer"
        },
        {
          "id": 23,
          "name": "Olivier wathelet"
        }
      ]
    }
  ],
  "pagination": {
    "total": 29,
    "pages": 3,
    "page": 1
  }
}
```

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

```shell
curl -X GET https://example.com/api/labs/1/organizations/4?api_key=XXXX"
```

```json
{
  "organization": {
    "id": 4,
    "name": "Phonoid",
    "status": "",
    "description": null,
    "website_url": "",
    "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=P&w=200&h=200",
    "contacts": [
      {
        "id": 1,
        "name": "Aurélien Malisart"
      }
    ]
  }
}
```

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

```shell
curl -X GET https://example.com/api/labs/1/contacts/1/organizations?api_key=XXXX"
```

```json
{
  "organizations": [
    {
      "id": 1,
      "name": "CETIC",
      "status": "",
      "description": null,
      "website_url": "",
      "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=C&w=200&h=200",
      "contacts": []
    },
    {
      "id": 3,
      "name": "80LIMIT",
      "status": "",
      "description": null,
      "website_url": "",
      "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=8&w=200&h=200",
      "contacts": [
        {
          "id": 95,
          "name": "Manon Roux"
        },
        {
          "id": 41,
          "name": "Mattéo Dupuy"
        },
        {
          "id": 70,
          "name": "Alice Faure"
        }
      ]
    },
    {
      "id": 4,
      "name": "Phonoid",
      "status": "",
      "description": null,
      "website_url": "",
      "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=P&w=200&h=200",
      "contacts": [
        {
          "id": 48,
          "name": "Alexandre Schneider"
        },
        {
          "id": 35,
          "name": "Serge Pampfer"
        },
        {
          "id": 23,
          "name": "Olivier wathelet"
        }
      ]
    }
  ],
  "pagination": {
    "total": 29,
    "pages": 3,
    "page": 1
  }
}
```

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

```shell
curl -X GET https://example.com/api/labs/1/contacts/1/organizations/1?api_key=XXXX"
```

```json
{
  "organization": {
    "id": 4,
    "name": "Phonoid",
    "status": "",
    "description": null,
    "website_url": "",
    "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=P&w=200&h=200",
    "contacts": [
      {
        "id": 1,
        "name": "Aurélien Malisart"
      }
    ]
  }
}
```
