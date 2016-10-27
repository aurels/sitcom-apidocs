# Contacts

## Get all contacts

```shell
curl -X GET https://example.com/api/labs/1/contacts?api_key=XXXX"
```

```json
{
  "contacts": [
    {
      "id": 1,
      "name": "Juliette Verne",
      "first_name": "Juliette",
      "last_name": "Verne",
      "active": true,
      "email": "juliettev@hotmail.com",
      "phone": "",
      "twitter_url": "",
      "linkedin_url": "",
      "facebook_url": "",
      "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=AD&w=200&h=200",
      "address": "",
      "address_street": "",
      "address_zip_code": "",
      "address_city": "",
      "address_country": "",
      "organizations": [],
      "projects": [
        {
          "id": 9,
          "name": "Practical Aluminum Bottle"
        },
        {
          "id": 14,
          "name": "Awesome Marble Hat"
        }
      ],
      "events": [
        {
          "id": 30,
          "name": "Vinegar cronut roof dreamcatcher."
        }
      ],
      "fields": [
        {
          "id": 1,
          "name": "amateur"
        },
        {
          "id": 8,
          "name": "Designeuse"
        }
      ]
    }
  ],
  "pagination": {
    "total": 1,
    "pages": 1,
    "page": 1
  }
}
```

This endpoint retrieves all contacts.

### HTTP Request

`GET /api/labs/:lab_id/contacts`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
page      | Integer | No

## Get a contact

```shell
curl -X GET https://example.com/api/labs/1/contacts/1?api_key=XXXX"
```

```json
{
  "contact": {
    "id": 1,
    "name": "Juliette Verne",
    "first_name": "Juliette",
    "last_name": "Verne",
    "active": true,
    "email": "juliettev@hotmail.com",
    "phone": "",
    "twitter_url": "",
    "linkedin_url": "",
    "facebook_url": "",
    "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=AD&w=200&h=200",
    "address": "",
    "address_street": "",
    "address_zip_code": "",
    "address_city": "",
    "address_country": "",
    "organizations": [],
    "projects": [
      {
        "id": 9,
        "name": "Practical Aluminum Bottle"
      },
      {
        "id": 14,
        "name": "Awesome Marble Hat"
      }
    ],
    "events": [
      {
        "id": 30,
        "name": "Vinegar cronut roof dreamcatcher."
      }
    ],
    "fields": [
      {
        "id": 1,
        "name": "amateur"
      },
      {
        "id": 8,
        "name": "Designeuse"
      }
    ]
  }
}
```

This endpoint retrieves a specific contact.

### HTTP Request

`GET /api/labs/:lab_id/contacts/:id`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes

## Create a contact

```shell
curl -X POST -H "Content-Type: multipart/form-data;" -F "contact[first_name]=Nucky" -F "contact[last_name]=Thompson" "http://example.com/api/labs/1/contacts?api_key=XXXX"
```

```json
{
  "contact": {
    "id": 140,
    "name": "Nucky Thompson",
    "first_name": "Nucky",
    "last_name": "Thompson",
    "active": false,
    "email": "",
    "phone": "",
    "twitter_url": "",
    "linkedin_url": "",
    "facebook_url": "",
    "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=NT&w=200&h=200",
    "address": "",
    "address_street": "",
    "address_zip_code": "",
    "address_city": "",
    "address_country": "",
    "organizations": [],
    "projects": [],
    "events": [],
    "fields": []
  }
}
```

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

```shell
curl -X PUT -H "Content-Type: multipart/form-data;" -F "contact[email]=nucky.thompson@boardwalk.net"  "http://example.com/api/labs/1/contacts/1?api_key=XXXX"
```

```json
{
  "contact": {
    "id": 140,
    "name": "Nucky Thompson",
    "first_name": "Nucky",
    "last_name": "Thompson",
    "active": false,
    "email": "nucky.thompson@boardwalk.net",
    "phone": "",
    "twitter_url": "",
    "linkedin_url": "",
    "facebook_url": "",
    "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=NT&w=200&h=200",
    "address": "",
    "address_street": "",
    "address_zip_code": "",
    "address_city": "",
    "address_country": "",
    "organizations": [],
    "projects": [],
    "events": [],
    "fields": []
  }
}
```

This endpoint updates an existing contact.

### HTTP Request

`PUT /api/labs/:lab_id/contacts/:id`

### Query Parameters

Parameter                   | Type      | Required
---------                   | ----      | --------
api_key                     | String    | Yes
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

```shell
curl -X DELETE -H "Content-Type: multipart/form-data;" "http://example.com/api/labs/1/contacts/1?api_key=XXXX"
```

This endpoint deletes an existing contact.

### HTTP Request

`DELETE /api/labs/:lab_id/contacts/:id`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes

