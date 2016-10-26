# Projects

## Get all projects

```shell
curl -X GET https://example.com/api/labs/1/projects?api_key=XXXX"
```

```json
{
  "projects": [
    {
      "id": 11,
      "name": "Awesome Plastic Shoes",
      "description": "Facere et ea ullam aut quas.",
      "start_date": "2017-01-08",
      "end_date": "2017-01-19",
      "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=A&w=200&h=200",
      "contacts": [
        {
          "id": 18,
          "name": "Renaud Debois"
        },
        {
          "id": 18,
          "name": "Freddy Mercury"
        },
      ]
    },
    {
      "id": 14,
      "name": "Awesome Marble Hat",
      "description": "Eaque beatae expedita incidunt et vel velit et quia.",
      "start_date": "2016-11-25",
      "end_date": "2016-12-05",
      "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=A&w=200&h=200",
      "contacts": [
        {
          "id": 36,
          "name": "Sabine Dupont"
        }
      ]
    }
  ],
  "pagination": {
    "total": 21,
    "pages": 3,
    "page": 1
  }
}
```

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

```shell
curl -X GET https://example.com/api/labs/1/projects/1?api_key=XXXX"
```

```json
{
  "project": {
    "id": 11,
    "name": "Awesome Plastic Shoes",
    "description": "Facere et ea ullam aut quas.",
    "start_date": "2017-01-08",
    "end_date": "2017-01-19",
    "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=A&w=200&h=200",
    "contacts": [
      {
        "id": 18,
        "name": "Renaud Debois"
      },
      {
        "id": 18,
        "name": "Freddy Mercury"
      },
    ]
  },
}
```


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

```shell
curl -X GET https://example.com/api/labs/1/contacts/1/projects?api_key=XXXX"
```

```json
{
  "projects": [
    {
      "id": 11,
      "name": "Awesome Plastic Shoes",
      "description": "Facere et ea ullam aut quas.",
      "start_date": "2017-01-08",
      "end_date": "2017-01-19",
      "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=A&w=200&h=200",
      "contacts": [
        {
          "id": 18,
          "name": "Renaud Debois"
        },
        {
          "id": 18,
          "name": "Freddy Mercury"
        },
      ]
    },
    {
      "id": 14,
      "name": "Awesome Marble Hat",
      "description": "Eaque beatae expedita incidunt et vel velit et quia.",
      "start_date": "2016-11-25",
      "end_date": "2016-12-05",
      "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=A&w=200&h=200",
      "contacts": [
        {
          "id": 36,
          "name": "Sabine Dupont"
        }
      ]
    }
  ],
  "pagination": {
    "total": 21,
    "pages": 3,
    "page": 1
  }
}
```

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

```shell
curl -X GET https://example.com/api/labs/1/contacts/1/projects/1?api_key=XXXX"
```

```json
{
  "project": {
    "id": 11,
    "name": "Awesome Plastic Shoes",
    "description": "Facere et ea ullam aut quas.",
    "start_date": "2017-01-08",
    "end_date": "2017-01-19",
    "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=A&w=200&h=200",
    "contacts": [
      {
        "id": 18,
        "name": "Renaud Debois"
      },
      {
        "id": 18,
        "name": "Freddy Mercury"
      },
    ]
  }
}
```

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
