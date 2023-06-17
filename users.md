# Users
## Create User
This endpoint wll create user.
### HTTP Request
`POST http://localhost:5000/user`
### Payload
|Parameter|Required|Unique|Description|
|---------|--------|------|-----------|
|firstName|true|false|User first name|
|lastName|false|false|User last name|
|email|false|false|User email id|
|phoneNumber|false|false|User Phone number|
|avatar|false|false|User Profile Picture|
|password|true|false|User Password|
|username|true|false|User Username|
|comments|false|false|User Comments|
|notifications|false|false|User Notification|
|wishlist|false|false|User wishlist movies|
|watchLater|false|false|User watch-later movies|

## Get Specific User
This endpoint wll get user's details.
### HTTP Request
`GET http://localhost:5000/user`
> The above command will return JSON as follows:

## Delete Specific User
This endpoint wll delete user.
### HTTP Request
`DELETE http://localhost:5000/user`
> The above command will return JSON as follows:


