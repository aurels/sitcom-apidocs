# Labs

## Get all labs

```shell
curl -X GET https://example.com/api/labs?api_key=XXXX"
```

```json
{
  "labs": [
    {
      "id": 2,
      "name": "e-Health",
      "url": "http://sitcom.dev/e-health"
    },
    {
      "id": 3,
      "name": "Fake",
      "url": "http://sitcom.dev/fake"
    },
    {
      "id": 4,
      "name": "fake2",
      "url": "http://sitcom.dev/fake2"
    },
    {
      "id": 1,
      "name": "Smart Gastronomy Lab",
      "url": "http://sitcom.dev/smart-gastronomy-lab"
    }
  ]
}
```
This endpoint retrieves all labs.

### HTTP Request

`GET /api/labs`

### Query Parameters

Parameter | Type   | Required
--------- | ------ | --------
api_key   | String | Yes

## Get one lab

```shell
curl -X GET https://example.com/api/labs/1?api_key=XXXX"
```

```json
{
  "lab": {
    "id": 1,
    "name": "Smart Gastronomy Lab",
    "url": "http://sitcom.dev/smart-gastronomy-lab"
  }
}
```

This endpoint retrieves a specific lab.

### HTTP Request

`GET /api/labs/:id`

### Query Parameters

Parameter | Type    | Required
--------- | ----    | --------
api_key   | String  | Yes
