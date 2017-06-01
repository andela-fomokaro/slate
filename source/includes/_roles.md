# Roles

## List Roles
> Response:

```javascript
[
  {
    "id": 1,
    "name": "admin"
  },
  {
    "id": 2,
    "name": "regular"
  }
]
```

### Request
- Endpoint: GET: `/roles`
- Requires: Authentication

### Response
- Status: `200: OK`
- Body `(application/json)`



## Create Role

> Request:

```javascript
{
  "name": "Publisher",
}
```

> Response:

```javascript
{
  "read": false,
  "write": false,
  "delete": false,
  "id": 5,
  "title": "Publisher",
  "updatedAt": "2017-05-31T10:12:08.032Z",
  "createdAt": "2017-05-31T10:12:08.032Z"
}
```

### Request
- Endpoint: POST: `/roles`
- Requires: Authentication
- Body `(application/json)`


### Response
- Status: `201: Created`
- Body `(application/json)`


## Get Role

> Response:

```javascript
{
  "id": 2,
  "name": "regular"
}
```

### Request
- Endpoint: GET: `/roles/:id`

### Response
- Status: `200: OK`
- Body `(application/json)`


## Edit Role

> Request:

```javascript
{
  "name": "subscriber",
}
```

> Response:

```javascript
{
  "id": 3,
  "name": "subscriber"
}
```

### Request
- Endpoint: PUT: `/roles/:id`
- Requires: Authentication
- Body `(application/json)`

### Response
- Status: `200: OK`
- Body `(application/json)`


## Delete Role

> Response:

```javascript
{
  "message": "Role deleted"
}
```

### Request
- Endpoint: DELETE: `/roles/:id`
- Requires: Authentication

### Response
- Status: `200: OK`
- Body `(application/json)`