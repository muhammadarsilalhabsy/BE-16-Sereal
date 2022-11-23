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


### Kelas
#### Get All Kelas
- Method: **GET**
- Endpoint: `/kelas`
- Response:
```json
{
}
```
#### Get Kelas by ID
- Method: **GET**
- Endpoint: `kelas/{id}`
- Response:
```json
{
}
```
### Get Kelas by categories
> pake req.query
<!-- Admin -->
#### Update Kelas by ID
- Method: **POST**
- Endpoint: ``
- Response:
```json
{
}
```
#### Delete Kelas by ID

### Materi 
### Galeries
### Challenges
### Categories
### Users
