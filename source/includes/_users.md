# Users

## List All Users
> Sample JSON structured response:

```javascript
{
  "rows": [
      {
        "id": 3,
        "username": "gaye",
        "fullNames": "gaye",
        "email": "gaye@gmail.com",
        "roleId": 2,
        "password": "$2a$10$rrfP24A.JInpljqaj.y7DO2/YbCf3.LQ0XU0QVWyieOM0EpRYcUoy",
        "createdAt": "2017-05-28T21:26:12.290Z",
        "updatedAt": "2017-05-29T12:27:02.451Z"
      },
      {
        "id": 2,
        "username": "Paley",
        "fullNames": "Bakare Kehinde",
        "email": "noxyblaze@gmail.com",
        "roleId": 2,
        "password": "$2a$08$VlWprHmJC9K7wNgVuPkQmO/Yxw7akPdpu/psaiJq5J/p5otQ3rL/O",
        "createdAt": "2017-05-23T09:24:46.840Z",
        "updatedAt": "2017-05-29T12:27:03.745Z"
      },
      {
        "id": 1,
        "username": "Faith",
        "fullNames": "Omokaro Faith",
        "email": "omokarofaith@gmail.com",
        "roleId": 1,
        "password": "$2a$10$sglZbIRAvMbwA53NK70LpeW8fOVupbMp3NyZdUMxT6WNvZVD4/TL.",
        "createdAt": "2017-05-23T09:24:46.784Z",
        "updatedAt": "2017-05-29T12:27:36.816Z"
      }
  ],
  "pagination": {
    "page_count": 1,
    "page": 1,
    "page_size": 5,
    "total_count": 5
  }
}
```

### Request
- Endpoint: GET: `/users`
- Requires: Authentication

### Query Parameters
Parameter | Default | Description
--------- | ------- | -----------
limit | 6 | Sets the limit.
offset | 0 | Sets the offset.

### Response
- Status: `200: OK`
- Body `(application/json)`



## Create User

> Request:

```javascript
{
  "username": "kenpachi",
  "fullNames": "Kenpachi Zaraki",
  "email": "bosskp@bleach.com",
  "password": "bankai!"
}
```

> Response:

```javascript
{
  "id": 6,
  "username": "kenpachi",
  "fullName": "Kenpachi Zaraki",
  "email": "bosskp@bleach.com",
  "roleId": 2,
  "message": "User Has Been Successfully Created",
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6NCwidXNlcm5hbWUiOiJrZW5wYWNoaSIsInJvbGVJZCI6MiwiaWF0IjoxNDk2MDAxNTE4LCJleHAiOjE0OTY2MDYzMTh9.GjmEBd_9LH9b_Gdabgdfit2HfkFBZfPshquUnAmRXV8"
}
```

### Request
- Endpoint: POST: `/users`
- Body `(application/json)`


### Response
- Status: `201: Created`
- Body `(application/json)`


## Get User

> Response:

```javascript
{
  "username": "Paley",
  "fullNames": "Bakare Kehinde",
  "email": "noxyblaze@gmail.com",
  "roleId": 2,
  "password": "$2a$08$VlWprHmJC9K7wNgVuPkQmO/Yxw7akPdpu/psaiJq5J/p5otQ3rL/O",
  "createdAt": "2017-05-23T09:24:46.840Z",
  "updatedAt": "2017-05-29T12:27:03.745Z"
}
```

### Request
- Endpoint: GET: `/users/:id`
- Requires: Authentication

### Response
- Status: `200: OK`
- Body `(application/json)`


## Edit User

> Request:

```javascript
{
  "roleId": 1,
}
```

> Response:

```javascript
{
  "id": 2,
  "username": "Paley",
  "fullNames": "Bakare Kehinde",
  "email": "noxyblaze@gmail.com"
}
```

### Request
- Endpoint: PUT: `/users/:id`
- Requires: Authentication
- Body `(application/json)`

### Response
- Status: `200: OK`
- Body `(application/json)`


## Delete User

> Response:

```javascript
{
  "message": "User deleted successfully"
}
```

### Request
- Endpoint: DELETE: `/users/:id`
- Requires: Authentication

### Response
- Status: `200: OK`
- Body `(application/json)`



## Login User

> Request:

```javascript
{
  "username": "Faith",
  "password": "omokarofaith@gmail.com"
}
```

> Response:

```javascript
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOjEsInJvbGVJZCI6MSwiaWF0IjoxNDk2MjIxOTU5LCJleHAiOjE0OTY4MjY3NTl9.cEMNsEzFLwV9D2ui6pBMMZUT6i_0v4_ZwEp9cVYvm1M",
  "message": "You have sucessfully logged in"
}
```

### Request
- Endpoint: POST: `/users/login`

### Response
- Status: `200: OK`
- Body `(application/json)`




## List User Documents

> Response:

```javascript
{
  "pagination": {
    "page_count": 1,
    "page": 1,
    "page_size": 2,
    "total_count": 2
  },
  "documents": [
    {
      "access": "public",
      "ownerId": 3,
      "title": "Lovely Document",
      "content": "My document is lovely yaay!",
      "createdAt": "2017-05-28T21:32:37.263Z",
      "updatedAt": "2017-05-28T21:32:37.263Z",
      "id": 33
    },
    {
      "access": "public",
      "ownerId": 3,
      "title": "Lovely Document paapy",
      "content": "My document is lovely pappy!",
      "createdAt": "2017-05-28T21:33:03.267Z",
      "updatedAt": "2017-05-28T21:33:03.267Z",
      "id": 34
    }
  ]
}
```

### Request
- Endpoint: GET: `/users/:id/documents`
- Requires: Authentication

### Response
- Status: `200: OK`
- Body `(application/json)`


## Search Users

> Response:

```javascript
{
  "message": "Your search was successful",
  "users": {
    "count": 1,
    "rows": [
      {
        "id": 1,
        "username": "Faith",
        "fullNames": "Omokaro Faith",
        "email": "omokarofaith@gmail.com",
        "roleId": 1,
        "password": "$2a$10$sglZbIRAvMbwA53NK70LpeW8fOVupbMp3NyZdUMxT6WNvZVD4/TL.",
        "createdAt": "2017-05-23T09:24:46.784Z",
        "updatedAt": "2017-05-29T12:27:36.816Z"
      }
    ]
  },
  "pagination": {
    "page_count": 1,
    "page": 1,
    "page_size": 1,
    "total_count": 1
  }
}
```

### Request
- Endpoint: GET: `/search/users`
- Requires: Authentication

### Query Parameters
Parameter | Default | Description
--------- | ------- | -----------
faith | "" | Search query.

### Response
- Status: `200: OK`
- Body `(application/json)`
