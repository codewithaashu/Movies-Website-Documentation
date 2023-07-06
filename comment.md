# Comments

## Create comment
This endpoint will create a comment of the movie
## HTTP Request
`POST http://localhost:9000/comment/:id`
## Payload
|Parameter |Required | Unique | Description |
|----------|---------|--------|-------------|
|name      |true     |false   |User's name  |
|email|true|false|User's email|
|phone|false|false|User's phone number|
|comment|true|false|Comment content|

```
  url: http://localhost:9000/comment/64921491396b1005c6a86b6b,
  method: "POST",
  headers: {
 "Accept": "*/*",
 "Content-Type": "application/json" 
},
  data:{
  "name":"Ashish",
  "email":"ashishrajk1@gmail.com",
  "comment":"Hi, this is testing2 message."
},
```
> The above command will return JSON as follows:
```
{
  "movie": {
    "_id": "64921491396b1005c6a86b6b",
    "category": "Web-Series",
    "director": "Sahir Raza",
    "downloadingLink": [
      "https://linkmake.in/view2/z3kTL7HnGd",
      "https://linkmake.in/view2/9VFtT4RaC4",
      "https://linkmake.in/view2/XgrjbjU1KO"
    ],
    "duration": "2h 11min",
    "genre": [
      "Family",
      "Romantic"
    ],
    "language": "Hindi",
    "name": "Highway Love 2023 S01 Hindi ORG 720p 480p WEB-DL",
    "posterImg": "https://fs1.extraimage.org/picupto/2023/06/16/Highway-Love-2023-Hindi-S01-AMZN-Web-Series-1080p-HDRip-2GB.jpg",
    "quality": [
      "480p",
      "720p",
      "1080p"
    ],
    "rating": 7.9,
    "releasedDate": "2023-05-28",
    "screenshot": "https://filmy4cab.cloud/wp-content/uploads/2023/06/Highway-Love-Season-1.jpg",
    "size": [
      "450MB",
      "700MB",
      "2.1GB"
    ],
    "starCast": "Ritvik Sahore, Gayatri Bhardwaj, Anshuman Malhotra, Vvansh S Sethi, Gunit Cour, Kanupriya Pandit, Max Fernandes, Aviral Gupta, And Sumiet Subash Arora",
    "storyLine": "When a confident and feisty girl fixes an awkward but endearing guy’s car on the expressway, a warm-hearted love story starts to take life. As the guy finds himself smitten by this enigmatic girl, he learns to come out of his shell. Meanwhile, the girl learns to believe in the existence of true, unconditional love as they navigate the diversions, detours and pit-stops of their romantic journey.",
    "subCategory": "Amazon Prime",
    "subtitle": "No",
    "__v": 16,
    "uploadedDate": "2023-06-20T20:54:28.182Z",
    "comments": [
      {
        "comment": "nice love story movie",
        "name": "Bhumi Singh",
        "email": "",
        "phone": null,
        "commentTime": "2023-07-03T09:59:57.163Z",
        "_id": "64a29c1dcf0ba574e3ff0166"
      },
      {
        "comment": "Ok ok movie",
        "name": "Shreya",
        "email": null,
        "phone": null,
        "commentTime": "2023-07-03T10:00:23.987Z",
        "_id": "64a29c37cf0ba574e3ff0176"
      },
      {
        "comment": "Hi, this is testing2 message.",
        "name": "Ashish",
        "email": "ashishrajk1@gmail.com",
        "commentTime": "2023-07-06T19:26:35.673Z",
        "_id": "64a7156ba91a568abf545f5e"
      }
    ]
  },
  "message": "Comment added successfully."
}
```

## Get All Comments
This endpoint will return the list of comments.
## HTTP Request
`GET http://localhost:9000/comment`
```
  url: "http://localhost:9000/comment",
  method: "GET",
  headers:{
     "Accept": "*/*",
      }
```
> The above command will return JSON as follows:
```
{
  "comments": [
    {
      "name": "Highway Love 2023 S01 Hindi ORG 720p 480p WEB-DL",
      "category": "Web-Series",
      "uploadedDate": "2023-06-20T20:54:28.182Z",
      "comments": [
        {
          "comment": "nice love story movie",
          "name": "Bhumi Singh",
          "email": "",
          "phone": null,
          "commentTime": "2023-07-03T09:59:57.163Z",
          "_id": "64a29c1dcf0ba574e3ff0166"
        },
        {
          "comment": "Ok ok movie",
          "name": "Shreya",
          "email": null,
          "phone": null,
          "commentTime": "2023-07-03T10:00:23.987Z",
          "_id": "64a29c37cf0ba574e3ff0176"
        }
      ]
    },
    {
      "name": "August 16 1947 (2023) South UnCut Dual Audio [Hindi + Tamil] Full Movie HD ESub",
      "category": "Movies",
      "uploadedDate": "2023-06-21T19:01:14.930Z",
      "comments": [
        {
          "comment": "Ok ok movie",
          "name": "Raj arayan",
          "email": "",
          "phone": null,
          "commentTime": "2023-07-05T18:42:02.111Z",
          "_id": "64a5b97a0b7eaf31571f1787"
        }
      ]
    }
  ]
}
```

## Get comments of a specific movie
This endpoint will return the all comments of a movie.
## HTTP Request
`GET http://localhost:9000/comment/:_id`
```
  url: http://localhost:9000/comment/64921491396b1005c6a86b6b,
  method: "GET",
  headers: {
          "Accept": "*/*",
          },
```
> The above command will return JSON as follows:
```
{
  "comments": [
    {
      "comment": "nice love story movie",
      "name": "Bhumi Singh",
      "email": "",
      "phone": null,
      "commentTime": "2023-07-03T09:59:57.163Z",
      "_id": "64a29c1dcf0ba574e3ff0166"
    },
    {
      "comment": "Ok ok movie",
      "name": "Shreya",
      "email": null,
      "phone": null,
      "commentTime": "2023-07-03T10:00:23.987Z",
      "_id": "64a29c37cf0ba574e3ff0176"
    }
  ]
}
```
