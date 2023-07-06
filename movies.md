# Movies

## Add Movies
This endpoint add movies
### HTTP Request
`POST http://localhost:9000/movies`
### Payload
|Parameter |Required | Unique | Description |
|----------|---------|--------|-------------|
|name      |true     |false   |Movies Name  |
|posterImg |true     |true    |Movies Poster Image/URL |
|downloadLink|true   |true    |Movies Download URL  |
|uploadedDate|true  |false |Movies uploaded date|
|category|true|false|Choose one of them web series or movies. |
|sub-category|false|false|Choose category of web series or movies.|
|genre|true|false|Choose the genre of web series or movie.|
|year|true|false|Movies Release year|
|imdbRating|false|false|IMDB Rating|
|userRating|false|false|User Rating|
|language|true|false|Movies Audio language|
|quality|false|false|Movies Quality|
|size|false|false|Movies size in all quality|
|duration|false|false|Movies Duration|
|subtitle|false|false|Movies have subtitle or not|
|releaseDate|true|false|Movies Release Date|
|director|false|false|Movies Director Name|
|starCast|true|false|Movie Starcast name|
|storyLine|false|false|Movies Story Description|
|screenshot|false|true|Movies Screenshoot Image /URL|
|downloadingLink|true|true|Movies Downloading Link in All Quality|
|comments|false|false|All comments of users.|

```
url: "http://localhost:9000/movies/",
  method: "POST",
  headers:{
 "Accept": "*/*",
 "Content-Type": "application/json" 
}
  data: {
"category": "Movies",
"director": "Koichi Sasaki,Ram Mohan,Yugo Sako",
"downloadingLink": [ "https://linkmake.in/view2/IHE6AKvxub", "https://linkmake.in/view2/PDSx4QfCNC", "https://linkmake.in/view2/ctEEqS3x1c"],
"duration": "2h 11min",
"genre": [ "Animation" ],
"language": "Hindi + English",
"name": "Adir The Legend of Prince Rama (1992) Dual Audio [Hindi + English] Full Movie DvdRip ESub",
"posterImg": "https://postimg.cc/2q93MXdV",
"quality": [ "480p", "720p", "1080p" ],
"rating": 9.2,
"screenshot": "https://st1.latestly.com/wp-content/uploads/2023/06/177-380x214.jpg",
"size": [ "400MB", "1.4GB", "3.8GB" ],
"starCast": "Amrish Puri, Arun Govil, Namrata Sawney, Nikhil Kapoor, Raell Padamsee, Shakti singh, Uday Mathan",
"storyLine": "Ramayana: The Legend of Prince Rama is a 1992 anime film co-produced by Japan and India; produced and directed by Yugo Sako. It is based on the Indian epic Ramayana.",
"subCategory": "Hollywood",
"subtitle": "Yes"
},
```

> The Above command return JSON as follows:
```json
{
  "movie": {
    "category": "Movies",
    "director": "Koichi Sasaki,Ram Mohan,Yugo Sako",
    "downloadingLink": [
      "https://linkmake.in/view2/IHE6AKvxub",
      "https://linkmake.in/view2/PDSx4QfCNC",
      "https://linkmake.in/view2/ctEEqS3x1c"
    ],
    "duration": "2h 11min",
    "genre": [
      "Animation"
    ],
    "language": "Hindi + English",
    "name": "Adir The Legend of Prince Rama (1992) Dual Audio [Hindi + English] Full Movie DvdRip ESub",
    "posterImg": "https://postimg.cc/2q93MXdV",
    "quality": [
      "480p",
      "720p",
      "1080p"
    ],
    "rating": 9.2,
    "uploadedDate": "2023-07-06T18:58:24.348Z",
    "releasedDate": "2023",
    "screenshot": "https://st1.latestly.com/wp-content/uploads/2023/06/177-380x214.jpg",
    "size": [
      "400MB",
      "1.4GB",
      "3.8GB"
    ],
    "starCast": "Amrish Puri, Arun Govil, Namrata Sawney, Nikhil Kapoor, Raell Padamsee, Shakti singh, Uday Mathan",
    "storyLine": "Ramayana: The Legend of Prince Rama is a 1992 anime film co-produced by Japan and India; produced and directed by Yugo Sako. It is based on the Indian epic Ramayana.",
    "subCategory": "Hollywood",
    "subtitle": "Yes",
    "_id": "64a70ed0a91a568abf545f32",
    "comments": [],
    "__v": 0
  },
  "message": "Movie Added Successfully"
}
```

## Get All Movies
This enpoint will return the list of all movies.
## HTTP Request
`GET http://localhost:9000/movies`

```
  url: "http://localhost:9000/movies",
  method: "GET",
  headers:{
           "Accept": "*/*",
           "Content-Type": "application/json" 
           },
```
> The above command will return JSON as follows:
```
{
"movies":[
    {
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
      "__v": 15,
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
      "_id": "649218da0d503b9d0e8ae485",
      "category": "Web-Series",
      "director": "Mahi v Raghav",
      "downloadingLink": [
        "https://linkmake.in/view2/A2OXaRN6DE",
        "https://linkmake.in/view2/oxcaFZz4zf",
        "https://linkmake.in/view2/20Ng2htzCG",
        "https://linkmake.in/view2/1cnHnxqlbM"
      ],
      "duration": "4h 05min",
      "genre": [
        "Action",
        "Crime",
        "Drama"
      ],
      "language": "Hindi",
      "name": "Shaitan S1 (2023) Hindi Completed Web Series HD ESub",
      "posterImg": "https://i.postimg.cc/Wzn5SL8y/Shaitan.jpg",
      "quality": [
        "480p",
        "720p HEVC",
        "720p",
        "1080p"
      ],
      "rating": 8.3,
      "releasedDate": "2023-06-15",
      "screenshot": "https://filmy4cab.cloud/wp-content/uploads/2023/06/Shaitan-Season-1.jpg",
      "size": [
        "700Mb",
        "1.5Gb",
        "2.6Gb",
        "3.5Gb"
      ],
      "starCast": "Jaffer Sadiq, Manikandan K., Lena, Aneesha Dama, Deviyani Sharma, Deviyani Sharma, Shelly Kishore, Nithin Prasanna, Manish Rishi, Ravi Kale, Kamakshi Bhaskarla",
      "storyLine": "A group of people kill those who threaten their existence, but consider themselves the victims and not the criminals.",
      "subCategory": "Disney+ Hotstar",
      "subtitle": "No",
      "__v": 0,
      "uploadedDate": "2023-06-20T19:54:28.182Z",
      "comments": []
    },
    {
      "_id": "64928fd50d58efdb39ddd8fc",
      "category": "Web-Series",
      "director": " Abbas Dalal, Hussain Dalal, Arunima Sharma",
      "downloadingLink": [
        "https://linkmake.in/view2/N0fNP1HXsY",
        "\nhttps://linkmake.in/view2/XEcZbq2KMb",
        "\nhttps://linkmake.in/view2/ukTA0XxiGX",
        "\nhttps://linkmake.in/view2/UbUC7yyO8C\n"
      ],
      "duration": "4h 28min",
      "genre": [
        "Drama",
        "Romantic"
      ],
      "language": "Hindi",
      "name": "Jee Karda S1 (2023) Hindi Completed Web Series HD ESub",
      "posterImg": "https://i.postimg.cc/YSxrq5Yv/Jee-Karda.jpg",
      "quality": [
        "480P HEVC",
        " 480P",
        " 720P HEVC",
        " 720P HEVC 10BIT"
      ],
      "rating": 8.4,
      "releasedDate": "2023-06-15",
      "screenshot": "https://filmy4cab.cloud/wp-content/uploads/2023/06/Jee-Karda-Season-1.jpg",
      "size": [
        "600Mb",
        " 950Mb",
        " 1.6Gb",
        " 1.8Gb"
      ],
      "starCast": "Tamannah Bhatia, Aashim Gulati, Suhail Nair, Anya Singh, Simone Singh, Sayan Banerjee, And Hussain Dalal",
      "storyLine": "Convaincus qu'à 30 ans, ils auraient tout compris à la vie, sept amis d'enfance se retrouvent confrontés à la réalité : la trentaine, c'est le bazar. Ils vivent, ils rient, il aiment, ils font des erreurs, ils ont le cœur brisé, ils évoluent, mais surtout, ils découvrent que les belles amitiés ne seront jamais parfaites et que la vie est en fait une belle et lumineuse nuance de gris.",
      "subCategory": "Amazon Prime",
      "subtitle": "No",
      "__v": 0,
      "uploadedDate": "2023-06-20T19:54:28.182Z",
      "comments": []
    },
]
}
```

## Get movie detail
This endpont will return the specific movie details.
## HTTP Request
`GET http://localhost:9000/movies/:_id`
```
  url: "http://localhost:9000/movies/64928fd50d58efdb39ddd8fc",
  method: "GET",
  headers:{
             "Accept": "*/*",
         },
```
> The above command will return JSON as follows:
```
{
  "movie": {
    "_id": "64928fd50d58efdb39ddd8fc",
    "category": "Web-Series",
    "director": " Abbas Dalal, Hussain Dalal, Arunima Sharma",
    "downloadingLink": [
      "https://linkmake.in/view2/N0fNP1HXsY",
      "\nhttps://linkmake.in/view2/XEcZbq2KMb",
      "\nhttps://linkmake.in/view2/ukTA0XxiGX",
      "\nhttps://linkmake.in/view2/UbUC7yyO8C\n"
    ],
    "duration": "4h 28min",
    "genre": [
      "Drama",
      "Romantic"
    ],
    "language": "Hindi",
    "name": "Jee Karda S1 (2023) Hindi Completed Web Series HD ESub",
    "posterImg": "https://i.postimg.cc/YSxrq5Yv/Jee-Karda.jpg",
    "quality": [
      "480P HEVC",
      " 480P",
      " 720P HEVC",
      " 720P HEVC 10BIT"
    ],
    "rating": 8.4,
    "releasedDate": "2023-06-15",
    "screenshot": "https://filmy4cab.cloud/wp-content/uploads/2023/06/Jee-Karda-Season-1.jpg",
    "size": [
      "600Mb",
      " 950Mb",
      " 1.6Gb",
      " 1.8Gb"
    ],
    "starCast": "Tamannah Bhatia, Aashim Gulati, Suhail Nair, Anya Singh, Simone Singh, Sayan Banerjee, And Hussain Dalal",
    "storyLine": "Convaincus qu'à 30 ans, ils auraient tout compris à la vie, sept amis d'enfance se retrouvent confrontés à la réalité : la trentaine, c'est le bazar. Ils vivent, ils rient, il aiment, ils font des erreurs, ils ont le cœur brisé, ils évoluent, mais surtout, ils découvrent que les belles amitiés ne seront jamais parfaites et que la vie est en fait une belle et lumineuse nuance de gris.",
    "subCategory": "Amazon Prime",
    "subtitle": "No",
    "__v": 0,
    "uploadedDate": "2023-06-20T19:54:28.182Z",
    "comments": []
  }
}
```

## Update Movie Detail
This endpoint will update the movie detail
## HTTP Request
`PUT http://localhost:9000/movies/:_id`
## Payload
|Parameter |Required | Unique | Description |
|----------|---------|--------|-------------|
|name      |false     |false   |Movies Name  |
|posterImg |false     |true    |Movies Poster Image/URL |
|downloadLink|false   |true    |Movies Download URL  |
|uploadedDate|false  |false |Movies uploaded date|
|category|true|false|Choose one of them web series or movies. |
|sub-category|false|false|Choose category of web series or movies.|
|genre|true|false|Choose the genre of web series or movie.|
|year|true|false|Movies Release year|
|imdbRating|false|false|IMDB Rating|
|userRating|false|false|User Rating|
|language|true|false|Movies Audio language|
|quality|false|false|Movies Quality|
|size|false|false|Movies size in all quality|
|duration|false|false|Movies Duration|
|subtitle|false|false|Movies have subtitle or not|
|releaseDate|false|false|Movies Release Date|
|director|false|false|Movies Director Name|
|starCast|false|false|Movie Starcast name|
|storyLine|false|false|Movies Story Description|
|screenshot|false|true|Movies Screenshoot Image /URL|
|downloadingLink|false|true|Movies Downloading Link in All Quality|
|comments|false|false|All comments of users.|

```
  url: "http://localhost:9000/movies/64928fd50d58efdb39ddd8fc",
  method: "PUT",
  headers: {
         "Accept": "*/*",
         "Content-Type": "application/json" 
           },
  data: {
  "category":"Movies"
},
```
> The above command will return JSON as follows:
```
{
  "movies": {
    "_id": "64928fd50d58efdb39ddd8fc",
    "category": "Movies",
    "director": " Abbas Dalal, Hussain Dalal, Arunima Sharma",
    "downloadingLink": [
      "https://linkmake.in/view2/N0fNP1HXsY",
      "\nhttps://linkmake.in/view2/XEcZbq2KMb",
      "\nhttps://linkmake.in/view2/ukTA0XxiGX",
      "\nhttps://linkmake.in/view2/UbUC7yyO8C\n"
    ],
    "duration": "4h 28min",
    "genre": [
      "Drama",
      "Romantic"
    ],
    "language": "Hindi",
    "name": "Jee Karda S1 (2023) Hindi Completed Web Series HD ESub",
    "posterImg": "https://i.postimg.cc/YSxrq5Yv/Jee-Karda.jpg",
    "quality": [
      "480P HEVC",
      " 480P",
      " 720P HEVC",
      " 720P HEVC 10BIT"
    ],
    "rating": 8.4,
    "releasedDate": "2023-06-15",
    "screenshot": "https://filmy4cab.cloud/wp-content/uploads/2023/06/Jee-Karda-Season-1.jpg",
    "size": [
      "600Mb",
      " 950Mb",
      " 1.6Gb",
      " 1.8Gb"
    ],
    "starCast": "Tamannah Bhatia, Aashim Gulati, Suhail Nair, Anya Singh, Simone Singh, Sayan Banerjee, And Hussain Dalal",
    "storyLine": "Convaincus qu'à 30 ans, ils auraient tout compris à la vie, sept amis d'enfance se retrouvent confrontés à la réalité : la trentaine, c'est le bazar. Ils vivent, ils rient, il aiment, ils font des erreurs, ils ont le cœur brisé, ils évoluent, mais surtout, ils découvrent que les belles amitiés ne seront jamais parfaites et que la vie est en fait une belle et lumineuse nuance de gris.",
    "subCategory": "Amazon Prime",
    "subtitle": "No",
    "__v": 0,
    "uploadedDate": "2023-06-20T19:54:28.182Z",
    "comments": []
  },
  "message": "Movie Detail exist"
}
```

## Delete movie
This endpoint will delete movie.
## HTTP Request
`DELETE http://localhost:9000/movies/:_id`

```
  url: "http://localhost:9000/movies/64928fd50d58efdb39ddd8fc",
  method: "DELETE",
  headers: {
         "Accept": "*/*"
            },
```
> The above command will return JSON as follows:
```
{
message:"Movie Deleted Successfully"
}
```


