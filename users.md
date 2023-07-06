# Users
## Create User
This endpoint wll create user.
### HTTP Request
`POST http://localhost:9000/user`
### Payload
|Parameter|Required|Unique|Description|
|---------|--------|------|-----------|
|name|true|false|User's name|
|email|true|true|User's email id|
|mobileNumber|false|false|User's mobile number|
|password|true|false|User's Password|
|verified|false|false|User's is verified or not. By default it is false.|
|userType|false|false|User type. It takes two values 'Admin' and 'Super-Admin'. By default it is 'Admin'.|

```shell
  url: "http://localhost:9000/user",
  method: "POST",
  headers: {
 "Accept": "*/*",
 "Content-Type": "application/json" 
},
data: '{
  "name":"test",
  "email":"test12345@gmail.com",
  "mobileNumber":1234567890,
  "password":"Test@123"
}',


```
> The above command returns JSON structured like this
```
{
  "user": {
    "name": "test",
    "email": "test12345@gmail.com",
    "mobileNumber": 1234567890
  },
  "message": "User successfully registered."
}
```

## Login User
This endpoint will login the user
### HTTP Request
`POST http://localhost:9000/user/login`
## Payload
|Parameter|Required|Unique|Description|
|---------|--------|------|-----------|
|email|true|true|User's email id|
|password|true|false|User's Password|
```
  url: "http://localhost:9000/user/login",
  method: "POST",
  headers:{
           "Accept": "*/*",
           "Content-Type": "application/json" 
           },
  data: {
  "email":"test12345@gmail.com",
  "password":"Test@123"
  },
```
> The above command will return JSON as follows:
```
{
  "user": {
    "email": "test12345@gmail.com",
    "password": "Test@123",
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE3MDEzN2E5MWE1NjhhYmY1NDVmMDAiLCJpYXQiOjE2ODg2NjgwNjF9.tluvqWQr5QxJ1v4x6oamFmHpXZYhvPlCSoETAp6mAJk",
    "verified": true
  },
  "message": "Login successfully"
}
```

## Get All Users
This endpoint will return all the users details
### HTTP Request
`GET http://localhost:9000/user`

```
  url: "http://localhost:9000/user",
  method: "GET",
  headers: {
    "Accept": "*/*",
     "Content-Type": "application/json" 
    },
```
> The above command will return JSON as follows:
```
{
  "users": [
    {
      "_id": "64a3f814ece4ad9cc6ea4ad9",
      "name": "Ashish Ranjan",
      "email": "ashishrajk123@gmail.com",
      "password": "$2b$10$/b5RbghJvNHbO1qMwOLn8u5/FzMX1wYX29s85wrhMRIl8BEby.iB6",
      "verified": true,
      "userType": "Super-Admin",
      "tokens": [
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGEzZjgxNGVjZTRhZDljYzZlYTRhZDkiLCJpYXQiOjE2ODg0Njc0Nzd9._bqU09ctQzbeOUYJyE4-idMNPYPV-0g0rZabmSIUzoA",
          "_id": "64a3f815ece4ad9cc6ea4adb"
        },
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGEzZjgxNGVjZTRhZDljYzZlYTRhZDkiLCJpYXQiOjE2ODg1NzA4OTl9.dlRjF30DoM0cmWyHOGHGylGtHpRBKKknXsJSCkIIjIU",
          "_id": "64a58c13490413f8bef5f97c"
        },
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGEzZjgxNGVjZTRhZDljYzZlYTRhZDkiLCJpYXQiOjE2ODg1NzczOTh9.lAVDo2GFsftXGb6-AkujWCbghTBdLaeWAK9bPZsbf3Y",
          "_id": "64a5a5762cdb765208609470"
        },
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGEzZjgxNGVjZTRhZDljYzZlYTRhZDkiLCJpYXQiOjE2ODg1ODE4NDR9.DGhTnC4IqE8likXG2xhceD4K8J7cnzqvYASJpBRj7tY",
          "_id": "64a5b6d40b7eaf31571f1668"
        },
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGEzZjgxNGVjZTRhZDljYzZlYTRhZDkiLCJpYXQiOjE2ODg1ODIzMTV9.MBhcSCzTlPxNdYkTZeEdyePZZJgIikarsV7I1B2ZXTU",
          "_id": "64a5b8ab0b7eaf31571f16a8"
        },
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGEzZjgxNGVjZTRhZDljYzZlYTRhZDkiLCJpYXQiOjE2ODg1ODIzNzl9.YM7K5qJjbX32ZwH29fInCLyq1vObS3KwSjxdDJiv_Gc",
          "_id": "64a5b8eb0b7eaf31571f16fb"
        },
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGEzZjgxNGVjZTRhZDljYzZlYTRhZDkiLCJpYXQiOjE2ODg2NTg5NzV9.IUHaeEDD1Je5HjVWsKwF7RKIHMIuotXlAseXwLiWgH8",
          "_id": "64a6e41f45a11742e2f570f2"
        }
      ],
      "__v": 7
    },
    {
      "_id": "64a40200d0fc3a6d5d1668b3",
      "name": "Bhumi Singh",
      "email": "bhumi05@gmail.com",
      "password": "$2b$10$Q2xdkjIzDzbIh4YrKiIdpORsbUS2YyarYBBlWQqqqGGa9rzw9EqaS",
      "verified": false,
      "userType": "Admin",
      "tokens": [
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE0MDIwMGQwZmMzYTZkNWQxNjY4YjMiLCJpYXQiOjE2ODg0NzAwMTZ9.EJ7vWEM7EME8AKwsjMQR9TxnRgWzib8FVM6M7YR8qRU",
          "_id": "64a40200d0fc3a6d5d1668b5"
        },
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE0MDIwMGQwZmMzYTZkNWQxNjY4YjMiLCJpYXQiOjE2ODg1Nzc0MzJ9.ZdaQlQ8ncHYfRPuF-qtxu2oltQ8yFYhY1lHWfGwgwSY",
          "_id": "64a5a5982cdb765208609492"
        },
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE0MDIwMGQwZmMzYTZkNWQxNjY4YjMiLCJpYXQiOjE2ODg1Nzc1NjV9.dlVeIxx7TkNgBAJS7X1VelTVOS8_xEKbpVBteQ8bSvs",
          "_id": "64a5a61d2cdb7652086094b2"
        },
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE0MDIwMGQwZmMzYTZkNWQxNjY4YjMiLCJpYXQiOjE2ODg1Nzc2MzZ9.bPBs4EeVASCc0SwlojiGguk9KqH-1HeLBgG2Bq8iT-g",
          "_id": "64a5a6642cdb7652086094f2"
        }
      ],
      "__v": 4
    },
    {
      "_id": "64a40408bc7f6fb579f13953",
      "name": "Shreya Singh",
      "email": "shreya@gmail.com",
      "password": "$2b$10$svWRjjNCDIjZr7KbXasR0O7AvlzvMziLB4bLnrV8S0ySEf/bgDCtu",
      "verified": true,
      "userType": "Admin",
      "tokens": [
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE0MDQwOGJjN2Y2ZmI1NzlmMTM5NTMiLCJpYXQiOjE2ODg0NzA1MzZ9.RfXgChb1F21p0UgOanBZEocwuDtQHSyX73nvu4ynO6o",
          "_id": "64a40408bc7f6fb579f13955"
        }
      ],
      "__v": 1
    },
    {
      "_id": "64a5a6852cdb7652086094f8",
      "name": "Raj Aryan",
      "email": "rajaryan123@gmail.com",
      "password": "$2b$10$PjoEOR6KZp9zmy0yRK8/QOD7MzJuCXOMrn/hBa1kUJaBIDE.nnxt.",
      "verified": true,
      "userType": "Admin",
      "tokens": [
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE1YTY4NTJjZGI3NjUyMDg2MDk0ZjgiLCJpYXQiOjE2ODg1Nzc2Njl9.LcVAX37--PpJDPArRA2-267d9N3Sjj8oUUNIGNTqmZI",
          "_id": "64a5a6852cdb7652086094fa"
        },
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE1YTY4NTJjZGI3NjUyMDg2MDk0ZjgiLCJpYXQiOjE2ODg1Nzc2OTl9.W8SQQcX93F1Ensvu6m29eyh4NT8I7Nky1JP0No6kc_c",
          "_id": "64a5a6a32cdb76520860950f"
        },
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE1YTY4NTJjZGI3NjUyMDg2MDk0ZjgiLCJpYXQiOjE2ODg1NzgyODh9.pBOHmbP2WEmhpwdixA-fgHjf_IqJZ7bvK-9eYN8saFg",
          "_id": "64a5a8f0b6dfa013e6a43045"
        },
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE1YTY4NTJjZGI3NjUyMDg2MDk0ZjgiLCJpYXQiOjE2ODg1NzgzMTh9.bgYuVUFqtWE5zXiEWl0-7q3NYGRxlegVFRGBF_TZWUU",
          "_id": "64a5a90eb6dfa013e6a43063"
        }
      ],
      "__v": 4
    },
    {
      "_id": "64a6e22845a11742e2f56f98",
      "name": "Neetu",
      "email": "neetuvishwakarma555@gmail.com",
      "password": "$2b$10$o5kWitSOJR/HP6V4MwBUyuNcUebQ3ssi9CtNf9aJq547.QfLLEjxW",
      "verified": true,
      "userType": "Admin",
      "tokens": [
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE2ZTIyODQ1YTExNzQyZTJmNTZmOTgiLCJpYXQiOjE2ODg2NTg0NzJ9.hGGKxYYIEt0iBDnTKqoamktZ_2s7gTPM1e3oIHis8qE",
          "_id": "64a6e22845a11742e2f56f9a"
        },
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE2ZTIyODQ1YTExNzQyZTJmNTZmOTgiLCJpYXQiOjE2ODg2NTg3Njh9.ZNC0rMjc9NGFY6XbpdvnC2z4zsYf3wJO4VDMTvNCMCc",
          "_id": "64a6e35045a11742e2f57028"
        },
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE2ZTIyODQ1YTExNzQyZTJmNTZmOTgiLCJpYXQiOjE2ODg2NTg3Njl9.MVt6XEIbcAWFtD5Eir-VaIagqkdJo9IRNBjMH-OFWIs",
          "_id": "64a6e35145a11742e2f57031"
        }
      ],
      "__v": 3
    },
    {
      "_id": "64a70137a91a568abf545f00",
      "name": "test",
      "email": "test12345@gmail.com",
      "mobileNumber": 1234567890,
      "password": "$2b$10$0epR1ErkdQMhaCmBU3IktuOncMok3rjHmGRVQs/8xUZrLIhmuzbWe",
      "verified": false,
      "userType": "Admin",
      "tokens": [
        {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE3MDEzN2E5MWE1NjhhYmY1NDVmMDAiLCJpYXQiOjE2ODg2NjY0MjV9.eOHQYxtwUzbW8JMFEp1PJyx-C1oFkVcVoDt7R0f8ykY",
          "_id": "64a70139a91a568abf545f02"
        }
      ],
      "__v": 1
    }
  ]
}
```

## Get Specific User
This endpoint wll get specific user's details.
### HTTP Request
`GET http://localhost:9000/user/:_id`

```
  url: "http://localhost:9000/user/64a70137a91a568abf545f00",
  method: "GET",
  headers:{
           "Accept": "*/*",
           "Content-Type": "application/json" 
           },
```
> The above command will return JSON as follows:
```
{
  "user": {
    "_id": "64a70137a91a568abf545f00",
    "name": "test",
    "email": "test12345@gmail.com",
    "mobileNumber": 1234567890,
    "password": "$2b$10$0epR1ErkdQMhaCmBU3IktuOncMok3rjHmGRVQs/8xUZrLIhmuzbWe",
    "verified": false,
    "userType": "Admin",
    "tokens": [
      {
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE3MDEzN2E5MWE1NjhhYmY1NDVmMDAiLCJpYXQiOjE2ODg2NjY0MjV9.eOHQYxtwUzbW8JMFEp1PJyx-C1oFkVcVoDt7R0f8ykY",
        "_id": "64a70139a91a568abf545f02"
      }
    ],
    "__v": 1
  }
}
```

## Update Specific User Details
This endpoint will  update specific user details.
### HTTP Request
`PUT http://localhost:9000/user/:_id`
### Payload
|Parameter|Required|Unique|Description|
|---------|--------|------|-----------|
|name|false|false|User's name|
|email|false|true|User's email id|
|mobileNumber|false|false|User's mobile number|
|password|false|false|User's Password|
|verified|false|false|User's is verified or not. By default it is false.|
|userType|false|false|User type. It takes two values 'Admin' and 'Super-Admin'. By default it is 'Admin'.|

```
  url: "http://localhost:9000/user/64a70137a91a568abf545f00",
  method: "PUT",
  headers:{
           "Accept": "*/*",
           "Content-Type": "application/json" 
         },
  data:{
  "verified":"true",
  "userType":"Admin",
  "name":"Raj Aryan"
}
```
> The above command will return JSON as follows:
```
{
  "user": {
    "_id": "64a70137a91a568abf545f00",
    "name": "Raj Aryan",
    "email": "test12345@gmail.com",
    "mobileNumber": 1234567890,
    "password": "$2b$10$0epR1ErkdQMhaCmBU3IktuOncMok3rjHmGRVQs/8xUZrLIhmuzbWe",
    "verified": true,
    "userType": "Admin",
    "tokens": [
      {
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE3MDEzN2E5MWE1NjhhYmY1NDVmMDAiLCJpYXQiOjE2ODg2NjY0MjV9.eOHQYxtwUzbW8JMFEp1PJyx-C1oFkVcVoDt7R0f8ykY",
        "_id": "64a70139a91a568abf545f02"
      }
    ],
    "__v": 1
  }
}
```

## Delete Specific User
This endpoint wll delete user.
### HTTP Request
`DELETE http://localhost:9000/user/:_id`

```
  url: "http://localhost:9000/user/64a5a6852cdb7652086094f8",
  method: "DELETE",
  headers:{
           "Accept": "*/*",
           "Content-Type": "application/json" 
           },
```
> The above command will return JSON as follows:
```
{
  "user": {
    "_id": "64a5a6852cdb7652086094f8",
    "name": "Raj Aryan",
    "email": "rajaryan123@gmail.com",
    "password": "$2b$10$PjoEOR6KZp9zmy0yRK8/QOD7MzJuCXOMrn/hBa1kUJaBIDE.nnxt.",
    "verified": true,
    "userType": "Admin",
    "tokens": [
      {
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE1YTY4NTJjZGI3NjUyMDg2MDk0ZjgiLCJpYXQiOjE2ODg1Nzc2Njl9.LcVAX37--PpJDPArRA2-267d9N3Sjj8oUUNIGNTqmZI",
        "_id": "64a5a6852cdb7652086094fa"
      },
      {
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE1YTY4NTJjZGI3NjUyMDg2MDk0ZjgiLCJpYXQiOjE2ODg1Nzc2OTl9.W8SQQcX93F1Ensvu6m29eyh4NT8I7Nky1JP0No6kc_c",
        "_id": "64a5a6a32cdb76520860950f"
      },
      {
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE1YTY4NTJjZGI3NjUyMDg2MDk0ZjgiLCJpYXQiOjE2ODg1NzgyODh9.pBOHmbP2WEmhpwdixA-fgHjf_IqJZ7bvK-9eYN8saFg",
        "_id": "64a5a8f0b6dfa013e6a43045"
      },
      {
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2NGE1YTY4NTJjZGI3NjUyMDg2MDk0ZjgiLCJpYXQiOjE2ODg1NzgzMTh9.bgYuVUFqtWE5zXiEWl0-7q3NYGRxlegVFRGBF_TZWUU",
        "_id": "64a5a90eb6dfa013e6a43063"
      }
    ],
    "__v": 4
  },
  "message": "User deleted successfully."
}
```


