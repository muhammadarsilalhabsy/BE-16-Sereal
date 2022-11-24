# Web Service & RESTful API Sereal Application by BE-16

## Built using:
- Express JS
- MongoDB
- Mongoose
- jsonwebtoken(JWT)
- bcrypt

## ERD
![]()
 
## Deploy Site
- [.up.railway.]()

## API Documentation
- swagger hub

## APIs Specification
- **Base URL API** : https://www
### Register
- Method: **POST**
- Endpoint: `/register`
- Body :
```json
{
    "name": "string",
    "email": "string, must have @",
    "password": "string"
}
```
- Response:
```json
{
    "message": "data has been created!!"
}
```

### Login 
- Method: **POST**
- Endpoint: `/login`
- Body :
```json
{
    "email": "string, must have @",
    "password": "string"
}
```
- Response:
```json
{
    "message": "Anda berhasil login",
    "token": "<your unique jwt token>"
}
```

### Logout
- Method: **POST**
- Endpoint: `/logout`
- Body :
```json
{
}
```
- Response:
```json
{
}
```
### Profile
#### Get Profile
- Method: **GET**
- Endpoint: `/profile`
- Response:
```json
{
}
```

#### Update Profile
- Method: **POST**
- Endpoint: `/profile/edit`
- Body :
```json
{
}
```
- Response:
```json
{
}
```

### Dashboard
- Method: **GET**
- Endpoint: `/dashboard`
- Response:
```json
{
}
```

### Galeri


### Materi

#### Get All Materi

Request :

- Method: **GET**
- Endpoint: `/materi `
- Header:
  - accept:application/json

Response :

- Status code: **200**

```json
{
    "massage":"string",
    "data":[
        {
            "id":"string, unique",
            "title":"string",
            "body":"string",
            "content":{
                "image":"[string]",
                "video":"[string]"
            },
            "status":boolean
        },
        {
            "id":"string, unique",
            "title":"string",
            "body":"string",
            "content":{
                "image":"[string]",
                "video":"[string]"
            },
            "status":boolean
        }
    ]
}
```

- Status code: **500**

```json
{
  "message": "string",
  "error": "string"
}
```

#### Get Materi by ID

Request :

- Method: **GET**
- Endpoint: `/materi/{materi_id}`
- Header:

  - accept:application/json

- Response:
- Status code: **200**

```json
{
    "massage":"string",
    "data":{
            "id":"string, unique",
            "title":"string",
            "body":"string",
            "content":{
                "image":"[string]",
                "video":"[string]"
            },
            "status":boolean
    }

}
```

- Status code: **400**

```json
{
  "message": "string"
}
```

#### Create Materi

Request :

- Method: **POST**
- Endpoint: `/materi`
- Header:
  - Content-type:application/json
  - accept:application/json
- Body:

```json
{
    "id":"string, unique",
    "title":"string",
    "body":"string",
    "content":{
        "image":"[string]",
        "video":"[string]"
    },
    "status":boolean
}
```

Response:

- Status code: **201**

```json
{
  "message": "string"
}
```

- Status code: **500**

```json
{
  "message": "string",
  "error": "string"
}
```

#### Update Materi

Request :

- Method: **PATCH**
- Endpoint: `/materi/{materi_id}`
- Header:
  - Content-type:application/json
  - accept:application/json
- Body:

```json
{
    "title":"string",
    "body":"string",
    "content":{
        "image":"[string]",
        "video":"[string]"
    },
    "status":boolean
}
```

Responses:

- Status code: **201**

```json
{
  "message": "string"
}
```

- Status code: **500**

```json
{
  "message": "string",
  "error": "string"
}
```

#### Delete Materi

Request :

- Method: **Delete**
- Endpoint: `/materi/{materi_id}`
- Header:
  - accept:application/json

Response:

- Status code: **200**

```json
{
  "message": "string"
}
```

- Status code: **404**

```json
{
  "message": "string",
  "error": "string"
}
```

### Kelas

#### Get All Kelas

Request :

- Method: **GET**
- Endpoint: `/kelas `
- Header:
  - accept:application/json

Response :

- Status code: **200**

```json
{
    "massage":"string",
    "data":[
        {
            "id":"string, unique",
            "title":"string",
            "description":"string",
            "materi":[
              {
                  "id":"string, unique",
                  "title":"string",
                  "body":"string",
                  "content":{
                      "image":"[string]",
                      "video":"[string]"
                  },
                  "status":boolean
              },
              {
                  "id":"string, unique",
                  "title":"string",
                  "body":"string",
                  "content":{
                      "image":"[string]",
                      "video":"[string]"
                  },
                  "status":boolean
              }
            ],
            "categories":[
              {
                "id":"string, unique",
                "name":"string"
              },
              {
                "id":"string, unique",
                "name":"string"
              }
            ],
            "status":boolean
        },
        {
            "id":"string, unique",
            "title":"string",
            "description":"string",
            "materi":[
              {
                  "id":"string, unique",
                  "title":"string",
                  "body":"string",
                  "content":{
                      "image":"[string]",
                      "video":"[string]"
                  },
                  "status":boolean
              },
              {
                  "id":"string, unique",
                  "title":"string",
                  "body":"string",
                  "content":{
                      "image":"[string]",
                      "video":"[string]"
                  },
                  "status":boolean
              }
            ],
            "categories":[
              {
                "id":"string, unique",
                "name":"string"
              },
              {
                "id":"string, unique",
                "name":"string"
              }
            ],
            "status":boolean
        }
    ]
}
```

- Status code: **500**

```json
{
  "message": "string",
  "error": "string"
}
```

#### Get Kelas by ID

Request :

- Method: **GET**
- Endpoint: `/kelas/{kelas_id}`
- Header:

  - accept:application/json

- Response:
- Status code: **200**

```json
{
    "massage":"string",
    "data":{
            "id":"string, unique",
            "title":"string",
            "description":"string",
            "materi":[
              {
                  "id":"string, unique",
                  "title":"string",
                  "body":"string",
                  "content":{
                      "image":"[string]",
                      "video":"[string]"
                  },
                  "status":boolean
              },
              {
                  "id":"string, unique",
                  "title":"string",
                  "body":"string",
                  "content":{
                      "image":"[string]",
                      "video":"[string]"
                  },
                  "status":boolean
              }
            ],
            "categories":[
              {
                "id":"string, unique",
                "name":"string"
              },
              {
                "id":"string, unique",
                "name":"string"
              }
            ],
            "status":boolean
        }

}
```

- Status code: **400**

```json
{
  "message": "string"
}
```

#### Create Kelas

Request :

- Method: **POST**
- Endpoint: `/kelas`
- Header:
  - Content-type:application/json
  - accept:application/json
- Body:

```json
{
    "title":"string",
    "description":"string",
    "materi":[objectID],
    "categories":[objectID],
    "status":boolean
}
```

Response:

- Status code: **201**

```json
{
  "message": "string"
}
```

- Status code: **500**

```json
{
  "message": "string",
  "error": "string"
}
```

#### Update Kelas

Request :

- Method: **PATCH**
- Endpoint: `/kelas/{kelas_id}`
- Header:
  - Content-type:application/json
  - accept:application/json
- Body:

```json
{
    "title":"string",
    "description":"string",
    "materi":[objectID],
    "categories":[objectID],
    "status":boolean
}
```

Responses:

- Status code: **201**

```json
{
  "message": "string"
}
```

- Status code: **500**

```json
{
  "message": "string",
  "error": "string"
}
```

#### Delete Kelas

Request :

- Method: **Delete**
- Endpoint: `/kelas/{kelas_id}`
- Header:
  - accept:application/json

Response:

- Status code: **200**

```json
{
  "message": "string"
}
```

- Status code: **404**

```json
{
  "message": "string",
  "error": "string"
}
```
