---
title: Sitcom API Reference

language_tabs:
  - shell
  - ruby

toc_footers:
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Kittn API! You can use our API to access Kittn API endpoints, which can get information on various cats, kittens, and breeds in our database.

We have language bindings in Shell, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Slate](https://github.com/tripit/slate). Feel free to edit it and use it as a base for your own API's documentation.

# Authentication

> To authorize, use this code:

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```

> Make sure to replace `meowmeowmeow` with your API key.

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://example.com/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

# Kittens

## Get All Kittens

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let kittens = api.kittens.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all kittens.

### HTTP Request

`GET http://example.com/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

# Labs

## Get all

### HTTP Request

`GET /api/labs`

## Get one

### HTTP Request

`GET /api/labs/:id`

# Users

## Get all users

### HTTP Request

`GET /api/users`

## Get one user

### HTTP Request

`GET /api/users/:id`

## Create a user

### HTTP Request

`POST /api/users`

## Update a user

### HTTP Request

`PUT /api/users/:id`

## Delete a user

### HTTP Request

`DELETE /api/users/:id`

# Permissions

## Get all permissions of a user

### HTTP Request

`GET /api/users/:user_id/permissions`

## Get permissions of a user on a lab

### HTTP Request

`GET /api/users/:user_id/permissions/:lab_id`

## Grant a user access to a lab

### HTTP Request

`POST /api/users/:user_id/permissions/:lab_id`

## Update permissions of a user on a lab

### HTTP Request

`PUT /api/users/:user_id/permissions/:lab_id`

## Remove access of a user to a lab

### HTTP Request

`DELETE /api/users/:user_id/permissions/:lab_id`

# Contacts

## Get all contacts

### HTTP Request

`GET /api/labs/:lab_id/contacts`

page

## Get a contact

### HTTP Request

`GET /api/labs/:lab_id/contacts/:id`

## Create a contact

### HTTP Request

`POST /api/labs/:lab_id/contacts`

## Update a contact

### HTTP Request

`PUT /api/labs/:lab_id/contacts/:id`

## Delete a contact

### HTTP Request

`DELETE /api/labs/:lab_id/contacts/:id`

# Tags

## Get all tags

### HTTP Request

`GET /api/labs/:lab_id/tags`

## Get all tags of a contact

### HTTP Request

`GET /api/labs/:lab_id/contacts/:contact_id/tags`

## Add some tags to a contact

### HTTP Request

`POST /api/labs/:lab_id/contacts/:contact_id/tags`

## Remove some tags from a contact

### HTTP Request

`DELETE /api/labs/:lab_id/contacts/:contact_id/tags`

# Organizations

## Get all organizations

### HTTP Request

`GET /api/labs/:lab_id/organizations`

page

## Get an organization

### HTTP Request

`GET /api/labs/:lab_id/organizations/:id`

## Get all organizations of a contact

### HTTP Request

`GET /api/labs/:lab_id/contacts/:contact_id/organizations`

page

## Get an organization of a contact

### HTTP Request

`GET /api/labs/:lab_id/contacts/:contact_id/organizations/:id`

# Projects

## Get all projects

### HTTP Request

`GET /api/labs/:lab_id/projects`

page

## Get a project

### HTTP Request

`GET /api/labs/:lab_id/projects/:id`

## Get all projects of a contact

### HTTP Request

`GET /api/labs/:lab_id/contacts/:contact_id/projects`

page

## Get a project of a contact

### HTTP Request

`GET /api/labs/:lab_id/contacts/:contact_id/projects/:id`

# Events

## Get all events

### HTTP Request

`GET /api/labs/:lab_id/events`

page

## Get an event

### HTTP Request

`GET /api/labs/:lab_id/events/:id`

## Get all events of a contact

### HTTP Request

`GET /api/labs/:lab_id/contacts/:contact_id/events`

page

## Get an event of a contact

### HTTP Request

`GET /api/labs/:lab_id/contacts/:contact_id/events/:id`
