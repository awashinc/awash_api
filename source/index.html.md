---
title: API Reference

language_tabs:
  - Javascript
  - Android
  - Ios

toc_footers:
  - Published By <a href='http://awash.co.kr'>Awash Inc.</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Awash API! 
You can use our API to access Awash API endpoints.

We have language bindings in Android, Ios! 

# Authentication

> To authorize, use this code:


```Javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```

```Ios
require 'kittn'

api = Awash::APIClient.authorize!('meowmeowmeow')
```

```Android
# With Android, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

> Make sure to replace `meowmeowmeow` with your API key.

Awash uses API keys to allow access to the API. You can register a new Awash API key at our [developer portal](http://example.com/developers).

Awash expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

# AwashComponets

## Get All AwashComponets

```Ios
require 'kittn'

api = Awash::APIClient.authorize!('meowmeowmeow')
api.awash_components.get
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.awash_components.get()
```

```Android
curl "http://example.com/api/awash_components"
  -H "Authorization: meowmeowmeow"
```

```Javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let awash_components = api.awash_components.get();
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

This endpoint retrieves all awash_components.

### HTTP Request

`GET http://example.com/api/awash_components`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include awash_components that have already been adopted.

<aside class="success">
Remember — a happy awash is an authenticated awash!
</aside>

## Get a Specific awash

```Ios
require 'kittn'

api = Awash::APIClient.authorize!('meowmeowmeow')
api.awash_components.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.awash_components.get(2)
```

```Android
curl "http://example.com/api/awash_components/2"
  -H "Authorization: meowmeowmeow"
```

```Javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.awash_components.get(2);
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

This endpoint retrieves a specific awash.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/awash_components/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the awash to retrieve

