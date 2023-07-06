# Data of Website

## Get data of website
This endpoint will return total movies,comments,message and user
## HTTP Request
`GET http://localhost:9000/data`
```
  url: "http://localhost:9000/data",
  method: "GET",
  headers: {
 "Accept": "*/*",
},
```
> This will return JSON as follows:
```
{
  "totalMovies": 31,
  "totalMessage": 4,
  "totalComments": 4,
  "totalUsers": 5
}
```
