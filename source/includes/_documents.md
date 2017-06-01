# Documents

## List Documents
> Response:

```javascript
{
  "pagination": {
    "page_count": 7,
    "page": 1,
    "page_size": 6,
    "total_count": 39
  },
  "documents": [
    {
      "id": 4,
      "title": "Profound non-volatile extranet",
      "content": "Consequuntur in natus sed assumenda et suscipit aut explicabo explicabo. Sequi sint consequatur facere asperiores corporis sit aut. Neque qui voluptatem nulla accusantium voluptatibus dolor odio dolorum quasi.",
      "access": "private",
      "createdAt": "2017-05-23T09:24:47.456Z",
      "updatedAt": "2017-05-23T09:24:47.456Z"
    },
    {
      "id": 5,
      "title": "Fully-configurable logistical concept",
      "content": "Quidem eum repellat vel et eos totam. Delectus quas officiis at voluptas quas. Dolores et non corporis itaque dolore delectus omnis dolores praesentium. Unde explicabo tenetur ea facilis in fuga distinctio. Et ea officiis. Necessitatibus voluptates dolorem recusandae ipsam et.",
      "access": "public",
      "createdAt": "2017-05-23T09:24:47.456Z",
      "updatedAt": "2017-05-23T09:24:47.456Z"
    },
    {
      "id": 7,
      "title": "Enhanced context-sensitive structure",
      "content": "Doloremque consequuntur similique. Nihil eum sunt ut reiciendis quam dignissimos ex quia quos. Ut ea voluptate quas quia voluptates culpa doloribus. Reprehenderit ad et beatae eligendi maiores at aliquam qui asperiores. Voluptatem quos harum necessitatibus officiis vitae ratione asperiores architecto voluptate. Dolores odio reiciendis dignissimos nam et ut a.",
      "access": "public",
      "createdAt": "2017-05-23T09:24:47.457Z",
      "updatedAt": "2017-05-23T09:24:47.457Z"
    },
    {
      "id": 8,
      "title": "Enterprise-wide mission-critical success",
      "content": "Qui quis ea praesentium cupiditate voluptatibus delectus. Ullam nam explicabo consequatur. Ducimus mollitia nobis.",
      "access": "private",
      "createdAt": "2017-05-23T09:24:47.457Z",
      "updatedAt": "2017-05-23T09:24:47.457Z"
    },
    {
      "id": 9,
      "title": "Team-oriented radical parallelism",
      "content": "Sunt nisi dolores quisquam necessitatibus tenetur. Adipisci asperiores nihil. Labore voluptas laborum ut. Et omnis et. Commodi officiis quos nostrum cupiditate quod numquam qui corrupti inventore.",
      "access": "public",
      "createdAt": "2017-05-23T09:24:47.457Z",
      "updatedAt": "2017-05-23T09:24:47.457Z"
    },
    {
      "id": 11,
      "title": "Future-proofed well-modulated projection",
      "content": "Aperiam sit error aperiam sunt laudantium qui et. Recusandae assumenda natus qui velit et non. Doloremque optio qui et quod eos cupiditate facere. Consequatur provident est error ipsum. Dolore et aut veniam magni ipsum amet in.",
      "access": "public",
      "createdAt": "2017-05-23T09:24:47.458Z",
      "updatedAt": "2017-05-23T09:24:47.458Z"
    }
  ]
}
```

### Request
- Endpoint: GET: `/documents`

### Query Parameters
Parameter | Default | Description
--------- | ------- | -----------
limit | 6 | Sets the limit.
offset | 0 | Sets the offset.

### Response
- Status: `200: OK`
- Body `(application/json)`



## Create Document

> Request:

```javascript
{
  "title": " blaze of glory ",
    "content": "glory....",
  "access": "public"
}
```

> Response:

```javascript
{
  "message": "Your Document Has Been Created",
  "document": {
    "access": "public",
    "id": 42,
    "title": " blaze of glory ",
    "content": "glory....",
    "ownerId": 1,
    "updatedAt": "2017-05-31T09:58:50.303Z",
    "createdAt": "2017-05-31T09:58:50.303Z"
  }
}
```

### Request
- Endpoint: POST: `/documents`
- Requires: Authentication
- Body `(application/json)`


### Response
- Status: `201: Created`
- Body `(application/json)`


## Get Document

> Response:

```javascript
{
  "document": {
    "id": 1,
    "title": "Title",
    "content": "Cumque dolorum laborum sint id. Error cumque ipsa\n      culpa est delectus dolores consequatur et laudantium.\n      Est enim facilis ad occaecati iusto qui. Et rerum tempora eius et\n      quae eveniet. Ut adipisci ut occaecati id assumenda nihil.\n      Eos repudiandae est sed qui est sapiente temporibus dolorem.",
    "access": "public",
    "ownerId": 1,
    "createdAt": "2017-05-23T09:24:47.454Z",
    "updatedAt": "2017-05-29T15:05:16.096Z"
  }
}
```

### Request
- Endpoint: GET: `/documents/:id`

### Response
- Status: `200: OK`
- Body `(application/json)`


## Edit Document

> Request:

```javascript
{
  "content": "Magical document manager"
}
```

> Response:

```javascript
{
  "id": 1,
  "title": "Title",
  "content": "Magical document manager",
  "access": "public",
  "authorId": 1,
  "createdAt": "2017-05-28T22:19:08.870Z",
  "updatedAt": "2017-05-28T22:58:17.249Z",
  "User": {
    "username": "admin",
    "roleId": 1
  }
}
```

### Request
- Endpoint: PUT: `/documents/:id`
- Requires: Authentication
- Body `(application/json)`

### Response
- Status: `200: OK`
- Body `(application/json)`


## Delete Document

> Response:

```javascript
{
  "message": {
  "message": "Document Successfully Deleted"
}
}
```

### Request
- Endpoint: DELETE: `/documents/:id`
- Requires: Authentication

### Response
- Status: `200: OK`
- Body `(application/json)`


## Search Documents

> Response:

```javascript
{
  "pagination": {
    "page_count": 1,
    "page": 1,
    "page_size": 1,
    "total_count": 1
  },
  "documents": [
    {
      "access": "public",
      "ownerId": 1,
      "title": "Title",
      "content": "Cumque dolorum laborum sint id. Error cumque ipsa\n      culpa est delectus dolores consequatur et laudantium.\n      Est enim facilis ad occaecati iusto qui. Et rerum tempora eius et\n      quae eveniet. Ut adipisci ut occaecati id assumenda nihil.\n      Eos repudiandae est sed qui est sapiente temporibus dolorem.",
      "createdAt": "2017-05-23T09:24:47.454Z",
      "updatedAt": "2017-05-29T15:05:16.096Z"
    }
  ]
}
```

### Request
- Endpoint: GET: `/search/documents`

### Query Parameters
Parameter | Default | Description
--------- | ------- | -----------
Title | "" | Search query.

### Response
- Status: `200: OK`
- Body `(application/json)`