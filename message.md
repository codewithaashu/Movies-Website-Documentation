# Messages

## Create message
This endpoint will send message
## HTTP Request
`POST http://localhost:9000/message`
## Payload
|Parameter |Required | Unique | Description |
|----------|---------|--------|-------------|
|name      |true     |false   |User's name  |
|email|true|false|User's email|
|phone|false|false|User's phone number|
|purpose|true|false|Purpose either be Request Movies or Removal Request or Other|
|message|true|false|Message content|
|messageDate|false|false|By default it will set to current date and time|

```
  url: "http://localhost:9000/message",
  method: "POST",
  headers: {
 "Accept": "*/*",
 "Content-Type": "application/json" 
},
  data:{
  "name":"Ashish",
  "email":"ashishrajk1@gmail.com",
  "purpose":"Request Movies",
  "message":"Hi, this is testing message."
},
```
> The above command will return JSON as follows:
```
{
  "msge": "Message successfully sent."
}
```

## Get All Message
This endpoint will return the list of messages.
## HTTP Request
`GET http://localhost:9000/message`
```
  url: "http://localhost:9000/message",
  method: "GET",
  headers:{
     "Accept": "*/*",
      }
```
> The above command will return JSON as follows:
```
{
  "messages": [
    {
      "_id": "64a2a7090efda5ad3b62ca6b",
      "name": "Bhumi Singh",
      "email": "bhumi02@gmail.com",
      "phone": null,
      "purpose": "Other",
      "message": "I want to talk with you.",
      "messageDate": "2023-07-03T10:46:33.326Z",
      "__v": 0
    },
    {
      "_id": "64a6de2945a11742e2f56f79",
      "name": "Shreya Singh",
      "email": "neeva02singh@gmail.com",
      "phone": "9798617082",
      "purpose": "Request Movies",
      "message": "add movie conjuring 2",
      "messageDate": "2023-07-06T15:30:49.294Z",
      "__v": 0
    },
    {
      "_id": "64a6deb245a11742e2f56f80",
      "name": "Bhumi Singh",
      "email": "neeva02singh@gmail.com",
      "phone": "9798617082",
      "purpose": "Removal Request",
      "message": "remove movie adipurush",
      "messageDate": "2023-07-06T15:33:06.648Z",
      "__v": 0
    },
    {
      "_id": "64a70fdaa91a568abf545f3c",
      "name": "Ashish",
      "email": "ashishrajk1@gmail.com",
      "purpose": "Request Movies",
      "message": "Hi, this is testing message.",
      "messageDate": "2023-07-06T19:02:50.254Z",
      "__v": 0
    }
  ]
}
```

## Get message detail
This endpoint will view a specific message
## HTTP Request
`GET http://localhost:9000/message/:_id`
```
  url: "http://localhost:9000/message/64a2a7090efda5ad3b62ca6b",
  method: "GET",
  headers: {
          "Accept": "*/*",
          },
```
> The above command will return JSON as follows:
```
{
  "message": "I want to talk with you."
}
```
