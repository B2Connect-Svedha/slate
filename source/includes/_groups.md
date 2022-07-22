# Groups

## List all groups

> GET /groups

```dart

```

```shell

```

```javascript
const axios = require("axios");


axios.get("/groups").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})


```

> Response for Status code: 200

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": [
    {
      "id": 0,
      "name": "string",
      "status": "string",
      "owner": "string",
      "usersCount": 0,
      "siteId": 0
    }
  ]
}

```
> Response for Status code: 400 and 500

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {}
}

```

Retrieves a list of all the groups

### Parameters

Name | Description
--------- | ------- 
status | Filter groups by given status (Available values: DRAFT/APPROVED)

### Response

<aside class="success">
Status Code 200 : Successfully retrieved groups information
</aside>

<aside class="warning">
Status Code 400 : Bad request. Wrong "status" value given
</aside>

<aside class="warning">
Status Code 500 : Server error
</aside>

## Create new group


> POST /groups

```dart

```

```shell

```

```javascript
const axios = require("axios");


axios.post("/groups").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})


```

> The above command requests a JSON structured like this:

```json

{
  "name": "string",
  "users": [
    {
      "phone": "string",
      "email": "string"
    }
  ]
}

```
> Response:

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {
    "groupId": 0,
    "notVerifiedUsers": [
      {
        "phone": "string",
        "email": "string"
      }
    ]
  }
}

```

Creates a new group for notifications

### Parameters

No parameters

### Response

<aside class="success">
Status Code 201 : Group successfully created
</aside>

<aside class="warning">
Status Code 400 : Bad request. Possible causes: group name required, both phone and email lists are empty, group with given name already exists. See "message" in response for details
</aside>

<aside class="warning">
Status Code 500 : Server error
</aside>

<aside class="warning">
Status Code 1000 : Partially success. Group has not verified contacts. Group saved as draft. To approve group use POST /groups/{id}/approve
</aside>

## Approve notification group


> POST /groups/{id}/approve

```dart

```

```shell

```

```javascript
const axios = require("axios");


axios.post("/groups/{id}/approve").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})


```

> Response:

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {}
}

```

Marks a new notification group as approved

### Parameters

Name | Description
--------- | ------- 
id(integer($int64)) | Group id to approve

### Response

<aside class="success">
Status Code 200 : Group successfully marked as approved
</aside>

<aside class="warning">
Status Code 404: Not found. No group found with given id
</aside>

<aside class="warning">
Status Code 500 : Server error
</aside>


## Add user to group


> POST /groups​/{groupId}​/users​/{userPhoneOrEmail}

```dart

```

```shell

```

```javascript
const axios = require("axios");


axios.post("​/groups​/{groupId}​/users​/{userPhoneOrEmail}").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})


```

> Response:

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {}
}

```

Adds a user to the group by given phone number or email

### Parameters

Name | Description
--------- | ------- 
groupId(integer($int64)) | Group id to add user
userPhoneOrEmail(string) | User's phone number or email address

### Response

<aside class="success">
Status Code 200 : User successfully added to the group
</aside>

<aside class="warning">
Status Code 404 : Not found. Possible causes: no group found with given id, no user found with given phone or email, user is already in group. See "message" in response for details
</aside>

<aside class="warning">
Status Code 500 : Server error
</aside>


## Delete user from group

> DELETE /groups/{groupId}/users/{userPhoneOrEmail}

```dart

```

```shell

```

```javascript
const axios = require("axios");


axios.delete("/groups/{groupId}/users/{userPhoneOrEmail}").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})


```

> Response:

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {}
}

```

Removes a user from the group

### Parameters

Name | Description
--------- | ------- 
groupId(integer($int64)) | Group id to delete user from
userPhoneOrEmail(string) | User's phone number or email address


### Response

<aside class="success">
Status Code 200 : User successfully deleted from the group
</aside>

<aside class="warning">
Status Code 404 : Not found. Possible causes: no group found with given id, no user found with given phone or email, user is not in given group. See "message" in response for details
</aside>

<aside class="warning">
Status Code 500 : Server error
</aside>


## Create new group by filter


> POST /groups/by-filter

```dart

```

```shell

```

```javascript
const axios = require("axios");


axios.post("/groups/by-filter").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})


```

> The above command requests a JSON structured like this:

```json

{
  "name": "string",
  "userFilter": {
    "userFilterItems": [
      {
        "text": "string",
        "filterField": "PROPERTY",
        "filterType": "EQUALS"
      }
    ]
  }
}

```
> Response:

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {
    "groupId": 0,
    "notVerifiedUsers": [
      {
        "phone": "string",
        "email": "string"
      }
    ]
  }
}

```

Creates a new group for notifications based on filters

### Parameters

No parameters

### Response

<aside class="success">
Status Code 201 : Group successfully created
</aside>

<aside class="warning">
Status Code 400 : Bad request. Possible causes: group name required, users count is empty, group with given name already exists. See "message" in response for details
</aside>

<aside class="warning">
Status Code 500 : Server error
</aside>

## Retrieve list of users in group


> GET /groups/{groupId}/users

```dart

```

```shell

```

```javascript
const axios = require("axios");


axios.get("/groups/{groupId}/users").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})


```

> Response for Status code: 200

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": [
    {
      "phone": "string",
      "email": "string"
    }
  ]
}
```

> Response for Status code: 400, 404 and 500

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {}
}

```

Retrieves the list of users in the group associated with the given group id

### Parameters

Name | Description
--------- | ------- 
groupId(integer($int64)) | Group id 
page(integer($int64)) | Page number to start with (Default value: 1)
per_page(integer($int64)) | Nunber of records to return in one request (Default value: 25)

### Response

<aside class="success">
Status Code 200 : Successfully retrieved group users information
</aside>

<aside class="warning">
Status Code 400 : Bad request. Possible causes: wrong "page" parameter, wrong "per_page" parameter, See "message" in response for details
</aside>

<aside class="warning">
Status Code 404 : Not found. No group found with given id
</aside>

<aside class="warning">
Status Code 500 : Server error
</aside>


## Retrieve group info


> GET /groups/{groupId}

```dart

```

```shell

```

```javascript
const axios = require("axios");


axios.get("/groups/{groupId}").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})


```
> Response if status code: 200

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {
    "id": 0,
    "name": "string",
    "owner": "string",
    "users": [
      {
        "phone": "string",
        "email": "string"
      }
    ]
  }
}

```

> Response if status code: 404 and 500

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {}
}

```

Retrieves group information of group associated with given id

### Parameters

Name | Description
--------- | ------- 
groupId(integer($int64)) | Group id to return info

### Response

<aside class="success">
Status Code 200 : 	
Successfully retrieved group information
</aside>

<aside class="warning">
Status Code 404: Not found. No group found with given id
</aside>

<aside class="warning">
Status Code 500 : Server error
</aside>


## Delete group


> DELETE /groups/{id}

```dart

```

```shell

```

```javascript
const axios = require("axios");


axios.delete("/groups/{id}").then((res) => {
  console.log(res)
}).catch(e => {
  console.log(e);
  Exit;
})


```

> Response:

```json

{
  "success": true,
  "code": 0,
  "message": "string",
  "body": {}
}

```
Deletes the group associated with the given id

### Parameters
Name | Description
--------- | ------- 
id(integer($int64)) | Group id to delete

### Response

<aside class="success">
Status Code 201 : Group successfully deleted
</aside>

<aside class="warning">
Status Code 404 : Not found. No group found with given id
</aside>

<aside class="warning">
Status Code 500 : Server error
</aside>
