# Events

## Get all events

```shell
curl -X GET https://example.com/api/labs/1/events?api_key=XXXX"
```

```json
{
  "events": [
    {
      "id": 1,
      "name": "Post-ironic bicycle rights flannel.",
      "description": "Provident rem molestias et quam.",
      "happens_on": "2016-12-24",
      "place": "Issy-les-Moulineaux",
      "website_url": "http://www.post-ironic-bicycle-rights-flannel.com",
      "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=P&w=200&h=200",
      "contacts": [
        {
          "id": 69,
          "name": "Josiane Vreux"
        },
      ]
    },
    {
      "id": 2,
      "name": "Venmo fixie taxidermy.",
      "description": "Animi recusandae dolores quidem incidunt dolorem.",
      "happens_on": "2016-09-12",
      "place": "Villejuif",
      "website_url": "http://www.venmo-fixie-taxidermy.com",
      "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=V&w=200&h=200",
      "contacts": [
        {
          "id": 31,
          "name": "Christian Blopp"
        },
        {
          "id": 68,
          "name": "Raphaël Dumichix"
        },
      ]
    },
  "pagination": {
    "total": 19,
    "pages": 2,
    "page": 1
  }
}
```

This endpoint retrieves all events.

### HTTP Request

`GET /api/labs/:lab_id/events`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
page      | Integer | No

## Get an event

```shell
curl -X GET https://example.com/api/labs/1/events/1?api_key=XXXX"
```

```json
{
  "event": {
    "id": 1,
    "name": "Post-ironic bicycle rights flannel.",
    "description": "Provident rem molestias et quam.",
    "happens_on": "2016-12-24",
    "place": "Issy-les-Moulineaux",
    "website_url": "http://www.post-ironic-bicycle-rights-flannel.com",
    "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=P&w=200&h=200",
    "contacts": [
      {
        "id": 69,
        "name": "Josiane Vreux"
      },
    ]
  }
}
```

This endpoint retrieves a specific event.

### HTTP Request

`GET /api/labs/:lab_id/events/:id`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
event_id  | Integer | Yes

## Get all events of a contact

```shell
curl -X GET https://example.com/api/labs/1/contacts/1/events/1?api_key=XXXX"
```

```json
{
  "events": [
    {
      "id": 1,
      "name": "Post-ironic bicycle rights flannel.",
      "description": "Provident rem molestias et quam.",
      "happens_on": "2016-12-24",
      "place": "Issy-les-Moulineaux",
      "website_url": "http://www.post-ironic-bicycle-rights-flannel.com",
      "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=P&w=200&h=200",
      "contacts": [
        {
          "id": 69,
          "name": "Josiane Vreux"
        },
      ]
    },
    {
      "id": 2,
      "name": "Venmo fixie taxidermy.",
      "description": "Animi recusandae dolores quidem incidunt dolorem.",
      "happens_on": "2016-09-12",
      "place": "Villejuif",
      "website_url": "http://www.venmo-fixie-taxidermy.com",
      "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=V&w=200&h=200",
      "contacts": [
        {
          "id": 31,
          "name": "Christian Blopp"
        },
        {
          "id": 68,
          "name": "Raphaël Dumichix"
        },
      ]
    },
  "pagination": {
    "total": 19,
    "pages": 2,
    "page": 1
  }
}
```

This endpoint retrieves all events of a specific contact.

### HTTP Request

`GET /api/labs/:lab_id/contacts/:contact_id/events`

### Query Parameters

Parameter  | Type    | Required
---------  | ----    | --------
api_key    | String  | Yes
page       | Integer | No

## Get an event of a contact

```shell
curl -X GET https://example.com/api/labs/1/contacts/1/events/1?api_key=XXXX"
```

```json
{
  "event": {
    "id": 1,
    "name": "Post-ironic bicycle rights flannel.",
    "description": "Provident rem molestias et quam.",
    "happens_on": "2016-12-24",
    "place": "Issy-les-Moulineaux",
    "website_url": "http://www.post-ironic-bicycle-rights-flannel.com",
    "picture_url": "https://placeholdit.imgix.net/~text?txtsize=68&txt=P&w=200&h=200",
    "contacts": [
      {
        "id": 69,
        "name": "Josiane Vreux"
      },
    ]
  }
}
```

This endpoint retrieves a specific event of a specific contact.

### HTTP Request

`GET /api/labs/:lab_id/contacts/:contact_id/events/:id`

### Query Parameters

Parameter  | Type    | Required
---------  | ----    | --------
api_key    | String  | Yes
