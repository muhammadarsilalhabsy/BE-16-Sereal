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

### Kelas
#### Get All Kelas
- Method: **GET**
- Endpoint: `/kelas`
- Response:
```json
{
}
```
#### Get Kelas
- Method: **GET**
- Endpoint: `kelas/{nama_kelas}`
- Response:
```json
{
}
```
<!-- Admin -->
> bole diskusi lagi
#### Update Kelas
- Method: **POST**
- Endpoint: ``
- Response:
```json
{
}
```
#### Delete Kelas by ID


### Materi
#### Get Materi 
- Method: **POST**
- Endpoint: `kelas/{nama_kelas}/{nama materi|index materi}`
- Response:
```json
{
}
```
### Galeri