# Movies
## Add Movies
### HTTP Request
`POST http://localhost:5000/api/movies`
This endpoint add movies
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

```shell
curl --location --request PUT 'https://api.omnifront.cloudsnob.com/paymentmanager/cc_123456789' \
--header 'customerToken: cs_987654321' \
--header 'token: site_AbCd' \
--header 'Content-Type: application/json' \
--data '{
    "cardNumbers": "11111111111111111",
    "cvv": "1234",
    "nameOnCard": "My Name Is John",
    "billingAddress": "20 Maple Ave",
    "billingAddress2": "",
    "billingZip": "123456",
    "billingCity": "Bala Cynwyd",
    "billingState": "Pennsylvania",
    "billingCountry": "United States",
    "billingPhone": "1234567890",
    "billingMobile": "",
    "isDefault": true,
    "expMonth": "01",
    "expYear": "11"
}'
```

> The Above command return JSON as follows:
```json
{
    "cardToken": "cc_123456789",
    "cardTokenStripe": "",
    "numbers": "11111111111111111",
    "lastFour": "6789",
    "expMonth": "01",
    "expYear": "11",
    "cvv": "1234",
    "nameOnCard": "My Name Is John",
    "billingAddress": "20 Maple Ave",
    "billingAddress2": "",
    "billingCity": "Bala Cynwyd",
    "billingState": "Pennsylvania",
    "billingZip": "123456",
    "billingPhone": "1234567890",
    "billingMobile": "",
    "billingCountry": "United States",
    "zipMatched": null,
    "avsMatched": null,
    "companyToken": "",
    "customerToken": "",
    "isDefault": 1,
    "archived": 0,
    "createdAt": "2023-04-20 21:17:19",
    "editedAt": "2023-04-20 22:31:19"
}
```




